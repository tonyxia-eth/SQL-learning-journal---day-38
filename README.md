# SQL-learning-journal---day-38

# CS50 Introduction to Databases with SQL — Book Cipher Assignment

**Date:** 2025-06-02  
**Assignment:** Decode a hidden message using a Book Cipher and SQL

---

### Problem Overview

I was tasked with decoding a secret message encoded as triplets referencing sentences in *The Adventures of Sherlock Holmes*. Each triplet gave:

- Sentence number
- Starting character position in the sentence
- Number of characters to extract

Using these triplets, the goal was to extract substrings from each sentence and reveal the hidden message.

---

### Key SQL Concepts Used

- `substr()` function: Extracts substring from sentences based on position and length.
- Views: Created a view named `message` that shows each extracted phrase as a separate row.

---

### Solution Highlights

- Created a helper table `cipher` with the triplets.
- Joined `cipher` with `sentences` on sentence ID.
- Applied `substr()` on the sentence using the start position and length from the cipher.
- Built the `message` view to display the decoded phrases.

---

### Terminal Commands Used

```bash
sqlite3 private.db < private.sql
sqlite3 private.db
SELECT * FROM message;


Result
phrase
find
me in
the place
you
least
expect.
behind the
books

Reflection
This assignment was a brilliant demonstration of how SQL’s string functions like substr() can be applied beyond typical data querying — here, to solve a fun cryptography puzzle. SQL is truly powerful for text manipulation as well as data retrieval.

#100DaysOfSQL #SQLLearning #DataEngineering #CS50 #menInTech
