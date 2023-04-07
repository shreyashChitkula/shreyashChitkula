---
title: "The reason why a char occupies 1 byte in  C/C++ but 2 bytes in java"
datePublished: Fri Apr 07 2023 05:05:33 GMT+0000 (Coordinated Universal Time)
cuid: clg632vt1000209mp3ptad2ov
slug: the-reason-why-a-char-occupies-1-byte-in-cc-but-2-bytes-in-java
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/70Rir5vB96U/upload/c1463ef07dd5d10cfc44e9f09e4465e9.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1680855102982/d969ceb3-aa83-425b-afc7-463e820d7086.jpeg
tags: java, java-programming, javaprogramming, wemakedevs

---

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680855455607/c2da8c17-4c9e-4cd7-8000-aae57631c6eb.jpeg align="center")

When it comes to programming languages, every language has its unique features and characteristics. One of the differences between Java and C/C++ that often confuses beginners is the difference in the amount of memory used for storing characters. In Java, a character takes up two bytes of memory, while in C/C++, a character only takes up one byte. But why is that?

Java was designed to be platform-independent, meaning that Java programs can run on any machine that has a Java Virtual Machine (JVM) installed. To make this possible, Java uses Unicode encoding to represent characters, which means that each character is represented by a 16-bit code value. This allows Java to support a wide range of characters from different languages and scripts.

On the other hand, C/C++ were designed to be low-level languages, giving the programmer more control over the machine's memory and performance. In these languages, a character is typically represented using ASCII encoding, which uses a single byte to represent each character.

While using two bytes for characters in Java may seem like a waste of memory compared to the one-byte representation used in C/C++, there are several benefits to using Unicode and two-byte characters. For one, it allows Java to support a much wider range of characters and scripts, making it a more versatile language for internationalization and localization. Additionally, using Unicode ensures that the same character will be represented consistently across different platforms and systems.

However, it's important to note that the amount of memory used for characters is not the only difference between Java and C/C++. There are many other differences in the way these languages handle memory, data types, and other programming concepts. So while it's important to understand why Java uses two bytes for characters, it's just one of many factors that differentiate these languages.

## ASCII encoding:

The ASCII (American Standard Code for Information Interchange) character set includes a total of 128 characters, including control characters, printable characters, and non-printable characters. The ASCII character set is often used as a basis for other character sets, such as the extended ASCII character set and Unicode.

![ASCII ](https://cdn.hashnode.com/res/hashnode/image/upload/v1680841633286/22d0fe8d-020f-4bd6-b4e1-59299d07ed6a.webp align="center")

## Unicode encoding:

* Unicode currently includes more than 143,000 characters, with a plan to add more characters in the future. The characters are divided into several planes, each of which contains up to 65,536 characters.
    
* Java supports the full Unicode character set, which currently includes over 143,000 characters from a wide range of languages, scripts, and symbols. Java represents Unicode characters using the UTF-16 encoding, which uses two bytes to represent most characters and four bytes to represent certain characters that are outside of the "basic multilingual plane" (BMP) of Unicode.
    
    The BMP includes the most commonly used characters in Unicode, and it spans the first 65,536 code points of the Unicode character set. Characters outside of the BMP are represented using two consecutive 16-bit code units in the UTF-16 encoding.
    

### Conclusion:

In conclusion, Java's support for Unicode makes it a popular choice for developing multilingual applications that need to handle text in different languages and scripts. It also enables developers to use a wide range of symbols and other characters in their applications, including emojis and other special characters.

### A fun thing to try out:)

```java
 public class EmojiPrinter {
  public static void main(String[] args) {
    System.out.print("\uD83D\uDE00"); // grinning face
    System.out.print("\uD83D\uDE02"); // face with tears of joy
    System.out.print("\uD83D\uDE0A"); // smiling face with smiling eyes
    System.out.print("\uD83D\uDC4D"); // thumbs up sign
    System.out.print("\uD83C\uDF89"); // party popper
  }
}
```

Output:

😀 😂 😊 👍 🎉