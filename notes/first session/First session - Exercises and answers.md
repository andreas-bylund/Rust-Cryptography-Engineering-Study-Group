## Book 
**Ch 1 - Q 10: Describe a concrete example where improving the security of a system against one type of attack can increase the likelihood of other attacks.**

**Answer:** In the book, they mention the example of if you strengthen security by issuing new, strong and long passwords, every week the probability increases that users will write down the password at the computer. This can increase the chance that someone physically enters e.g. the office and thus gain access to the password and thus the system.

**Ch 2 - Q3. Consider a group of 30 people who wish to establish pair-wise secure communications using symmetric-key cryptography. How many keys need to be exchanged in total.**

**Ch 2 - Q4. Suppose Bob receives a messages signed using a digital signature scheme with Alice’s secret signing key. Does it prove that Alice saw the message and chose to sign.**

**Ch 2 - Q6. Suppose a chosen-ciphertext attacker cannot recover the secret decryption key for an encryption scheme. Does this mean the encryption scheme is secure?**

**Ch 2 - Q7. Consider a symmetric-key cryptosystem in which cryptographic keys are randomly selected from the set of all n-bit strings. Approximately what should n be in order to provide 128 bits of security against a birthday attack.**

## General
**Q:Suppose you read about RSA encryption and wanted to find it’s standard specification. Where would you look?** 

**Q: Find two libraries for each of RSA, TLS/SSL, and AEAD. Evaluate the maturity each library, and skim the code. What about the library structure makes sense? How is their documentation? These links may help [https://cryptography.rs/](https://cryptography.rs/), [https://lib.rs/](https://lib.rs/) (librs is equivalent to [crates.io](http://crates.io/), with a different interface)**

**Q: Benchmark the speed of an algorithm in the two different implementations with Criterion or iai. You may use this code snippet for reference.**

**Q: You’re implementing a [Tweakable Encryption](https://en.wikipedia.org/wiki/Disk_encryption_theory) scheme. You need to know what standard API users will expect. Find a reference for the standard API and write the function signatures for encryption and decryption.**

**Q: You want to understand a paper on a new polynomial commitment scheme, but you’ve been trying for more than an hour, and the math is over your head. What do you do?**

**Q: Implement the [Vignère cipher](https://en.wikipedia.org/wiki/Vigen%C3%A8re_cipher) in 100 lines or less.**
**Q: What is a side channel attack? Is your cipher implementation constant time?**

**Q: Extra: Read [New Directions in Cryptography](https://ieeexplore.ieee.org/document/1055638).**

**Q: Extra: Consider ways to contribute what you learned this week to the [Uncloak](https://uncloak.org/) knowledge graph.**
