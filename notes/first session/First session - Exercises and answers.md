## Book

**Ch 1 - Q 10: Describe a concrete example where improving the security of a system against one type of attack can increase the likelihood of other attacks.**

**Answer:** In the book, they mention the example of if you for example strengthen security by issuing new, strong and long passwords (complex passwords to remember for the user), every week the probability increases that users will write down the password at the computer. This can increase the chance that someone physically enters e.g. the office and thus gain access to the password and thus the system.

**Ch 2 - Q3. Consider a group of 30 people who wish to establish pair-wise secure communications using symmetric-key cryptography. How many keys need to be exchanged in total.**

**Answer:** There are 30 people in the group. That means that each member of the group have to give their key to 29 members. By using n:th triangle number, (n^2 + n) / 2, we get how many times each member need to give their key. (29^2 + 29) / 2 = 435 times.

**Ch 2 - Q4. Suppose Bob receives a messages signed using a digital signature scheme with Alice’s secret signing key. Does it prove that Alice saw the message and chose to sign.**

**Answer:** No, there is nothing that proves that just Alice saw the message. For example her key could be compromised and someone else saw and signed the message.

**Ch 2 - Q6. Suppose a chosen-ciphertext attacker cannot recover the secret decryption key for an encryption scheme. Does this mean the encryption scheme is secure?**

**Answer:** No, there are other ways to attack the encryption scheme

**Ch 2 - Q7. Consider a symmetric-key cryptosystem in which cryptographic keys are randomly selected from the set of all n-bit strings. Approximately what should n be in order to provide 128 bits of security against a birthday attack.**

**Answer:** (<u>Not totally sure about this one, please correct me if my thought process is off</u>) If you want to  ensure a 128 bits of security against a birthday attack n should be 256.

My thought process:

Birthday bound = 2^n/2
n = number of bits of security we want

Due to the birthday bound we know that n will be n/2. Therefore we need n * 2 (128*2=256) to ensure 128 bits of security against a birthday attack.

(approximations, not exact math)

## General

**Q:Suppose you read about RSA encryption and wanted to find it’s standard specification. Where would you look?**

**Answer:** Would start by reading the wikipedia page on RSA encryption and also use the reference links at the bottom of the page. Should this not be enough, I would turn to Google to find a more specific answer to my question.

**Q: Find two libraries for each of RSA, TLS/SSL, and AEAD. Evaluate the maturity each library, and skim the code. What about the library structure makes sense? How is their documentation? These links may help https://cryptography.rs/, https://lib.rs/ (librs is equivalent to [crates.io](http://crates.io/), with a different interface)**

### RSA

> **Context:** RSA (Rivest-Shamir-Adleman) is a public-key cryptosystem that is widely used for secure data transmission. [(Wikipedia)](https://en.wikipedia.org/wiki/RSA_%28cryptosystem%29 "https://en.wikipedia.org/wiki/RSA_(cryptosystem)")

**RSA ([Github](https://github.com/RustCrypto/RSA))**
Seems that the code have been [audited](https://delta.chat/assets/1907-otf-deltachat-rpgp-rustrsa-gb-reportv1.pdf) by a 3rd party. Noted a warning though on their README.md page that another (not deltachat?) 3rd party have done an audit and the result have not been released yet. Either way, it seems to be very used package with almost 400,000 downloads each month and a active Github with over 30 contributors. The [documentation](https://docs.rs/rsa/0.7.2/rsa/) is great with many examples.

**rsa-oaep-pss ([Github](https://github.com/Hakhenaton/rsa-oaep-pss))**
The code have not been audited "by any peer" and it's clearly stated that the code are not production-ready. Under 200 downloads all time. The project on Github have only 2 contributors. Seems to be a new project that is currently is under heavy development. The documentation is fairly straight forward. Good with examples.  

### TLS/SSL

> **Context:** TLS/SSL (Transport Layer Security/Secure Socket Layer). TLS is a cryptographic protocol designed to provide communications security over a computer network. The protocol is widely used in applications such as email, instant messaging, HTTPS. TLS builds on the now-deprecated SSL. ([Wikipedia](https://en.wikipedia.org/wiki/Transport_Layer_Security))

**async-rustls ([Github](https://github.com/smol-rs/async-rustls))**
Can't find any information that the project/code have been audited by any 3rd party. The project have over 300,000 downloads, fairly active Github with recent commits and a few contributors. Pretty good documentation, missing some examples though.

**async-tls ([Github](https://github.com/async-rs/async-tls))**
Can't find any information here either that the project have been audited by any 3rd party. But, the different between async-rustls and this project, async-tls, is that it seems that async-tls is being the project to use. Awesome documentation with good examples, over 10+ github contributors and over 1,000,000+ downloads in total.   

### AEAD

> **Context:** AEAD (Authenticated Encryption with Associated Data) are form of encryption which simultaneously assure the confidentiality and authenticity of data. ([Wikipedia](https://en.wikipedia.org/wiki/Authenticated_encryption))



**Q: Benchmark the speed of an algorithm in the two different implementations with [Criterion](https://lib.rs/crates/criterion).**

**Q: You’re implementing a [Tweakable Encryption](https://en.wikipedia.org/wiki/Disk_encryption_theory) scheme. You need to know what standard API users will expect. Find a reference for the standard API and write the function signatures for encryption and decryption.**

**Q: You want to understand a paper on a new polynomial commitment scheme, but you’ve been trying for more than an hour, and the math is over your head. What do you do?**

**Q: Implement the [Vignère cipher](https://en.wikipedia.org/wiki/Vigen%C3%A8re_cipher) in 100 lines or less.**

**Q: What is a side channel attack? Is your cipher implementation constant time?**

**Q: Extra: Read [New Directions in Cryptography](https://ieeexplore.ieee.org/document/1055638).**

**Q: Extra: Consider ways to contribute what you learned this week to the [Uncloak](https://uncloak.org/) knowledge graph.**
