Here’s a standalone **student-friendly primer on identifying hash types** that you can link in a separate Markdown file:

---

# Primer: How to Identify Hash Types

When we see a hash (like a long string of random-looking letters and numbers), the first step before trying to crack it is figuring out **what kind of hash it is**. Different hashing algorithms look different — and each requires different approaches.

---

## 1. Look at the length

Most hash algorithms always produce outputs of the same length.
Examples (in hexadecimal):

* **MD5** → 32 characters

  ```
  5f4dcc3b5aa765d61d8327deb882cf99
  ```
* **SHA-1** → 40 characters

  ```
  a94a8fe5ccb19ba61c4c0873d391e987982fbbd3
  ```
* **SHA-256** → 64 characters

  ```
  9d5e3ecdeb373b2cfc6b5fc94b8e8f9b24c7a91e3267e6cdb5f44c34b884bba5
  ```
* **SHA-512** → 128 characters

👉 First trick: **count the characters.** That’s your first clue.

---

## 2. Check the alphabet (which characters appear?)

* If the hash uses only **0-9 and a-f**, it’s probably hexadecimal (MD5, SHA family, NTLM, etc.).
* If it also has characters like **./ or $**, it might be encoded differently (bcrypt, crypt, or base64-based).
* Example bcrypt hash (note the `$2b$` at the start):

  ```
  $2b$12$KIXlZ8Rp1Cw.XfEwl1hhxe3/98DF2tiAoA0f4F.WgQ7r0Q5i8X5k6
  ```

---

## 3. Look for identifying prefixes

Some hashes “tag” themselves:

* `$1$` → MD5 (Unix crypt format)
* `$2a$`, `$2b$`, `$2y$` → bcrypt
* `$5$` → SHA-256 (crypt format)
* `$6$` → SHA-512 (crypt format)

These prefixes are like name tags that give away the hash type.

---

## 4. Context clues

Where did the hash come from?

* **Windows systems** often use NTLM or LM hashes.
* **Linux / Unix** systems often use SHA-crypt (with prefixes).
* **Web apps** might use bcrypt, Argon2, or PBKDF2.

The source system narrows the possibilities.

---

## 5. Use hash identification tools (safely, in the lab)

Security professionals often use **hash ID tools** that guess the hash type for you by length and pattern.
Examples: `hashid`, `hash-identifier`, or websites like “Identify Hash.”

> ⚠️ Only use these in a safe classroom or lab setting. Never paste real-world hashes into random online tools.

---

## 6. Remember salts

If the hash is longer than expected, it might include a **salt** (random data). Salts make the same password produce different hashes. You may see a hash + extra characters separated by `$` or `:`.

---

## Summary

* **Count the length** → quick first clue.
* **Look at characters** → hex only or extra symbols?
* **Check prefixes** → `$2b$` means bcrypt, `$6$` means SHA-512, etc.
* **Use context** → where the hash came from often tells you the algorithm.
* **Salt awareness** → extra randomness means rainbow tables won’t work.

---

### Quick student takeaway:

Identifying a hash type is like being a detective:

* Length = how tall they are.
* Characters = what clothes they wear.
* Prefix = their name tag.
* Context = where they were found.

Once you know the type, you can understand **how strong it is** and **how an attacker might try to break it** — which helps defenders choose the best protections.

---

Would you like me to also make a **“hash type cheat sheet” table** (length + common formats + examples) that students can use as a quick reference?
