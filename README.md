# Multi-platform-AES-Encryption
Ready-To-Use AES-256 bit encryption library. Encryption method is AES with CBC mode and PCKS7 padding (aka. PCKS5).

## Coding Language Support 
Right now library written in C#, Java (Android) and NodeJS. Objective-C and Swift will coming soon.

## Encryption Input
2 parameters
* plain text string (string MUST be able to be converted into UTF-8 encoding).
* key string in hexadecimal format (64 characters length).

## Encryption Output
encrypted string in hexadecimal format.

## Decryption Input
2 parameters
* encrypted string in hexadecimal format.
* key string in hexadecimal format (64 characters length).

## Decryption Output
plaintext in UTF-8 encoding.

# Sample Usage
## C#
* Class ```\CSharp\Encryption.cs```
* Unit Test ```\CSharp\AESUnitTest\UnitTest1.cs```

```csharp
string text = "  Hello World  ";
string key = "44 52 d7 16 87 b6 bc 2c 93 89 c3 34 9f dc 17 fb 3d fb ba 62 24 af fb 76 76 e1 33 79 26 cd d6 02";

string encryptedText = AES.Encryption.encryptData(text, key);
string decryptedText = AES.Encryption.decryptData(encryptedText, key);
```

## Java, Android
* Class ```\Java_or_Android\app\src\main\java\com\piyapan039285\java_or_android\Encryption.java```
* Unit Test ```\Java_or_Android\app\src\test\java\com\piyapan039285\java_or_android\AESUnitTest.java```

**Important** : If you want to run unit test, you have to download "unlimited strength file" (link below). Then, install file to ${java.home}/jre/lib/security/. In Android Studio, you can find JDK path from ```Files -> Project Structure -> SDK Location.```
* unlimited strength file - Java 7 : http://www.oracle.com/technetwork/java/javase/downloads/jce-7-download-432124.html
* unlimited strength file - Java 8 : http://www.oracle.com/technetwork/java/javase/downloads/jce8-download-2133166.html

```java
string text = "  Hello World  ";
string key = "44 52 d7 16 87 b6 bc 2c 93 89 c3 34 9f dc 17 fb 3d fb ba 62 24 af fb 76 76 e1 33 79 26 cd d6 02";

string encryptedText = AES.Encryption.encryptData(text, key);
string decryptedText = AES.Encryption.decryptData(encryptedText, key);
```


## NodeJS
* Module ```\NodeJS\encryption.js```
* Unit Test ```\NodeJS\unitTest.js```
```js
var text = "  Hello World  ";
var key = "44 52 d7 16 87 b6 bc 2c 93 89 c3 34 9f dc 17 fb 3d fb ba 62 24 af fb 76 76 e1 33 79 26 cd d6 02";

var encryptedText = encryptor.encryptData(text, key);
var decryptedText = encryptor.decryptData(encryptedText, key);
```
