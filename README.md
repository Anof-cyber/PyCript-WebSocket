> [!Warning]  
> PyCript Websocket was created as seperate extension due to main PyCript was created using old burp suite APIs in Python. Main PyCript Extension now rewritten from scratch with Web Socket support directly inbuilt.

Use: https://github.com/Anof-cyber/PyCript


> [!Warning]  
> This Repository is not valid anymore and Websocket extension is no moved to main PyCript extension directly.

# PyCript WebSocket
<p align="center">
  <img src="https://i.ibb.co/KqGXSq0/Py-Cript-Banner.png" />
</p>


PyCript WebSocket is a Burp Suite extension that enables users to encrypt and decrypt WebSocket messages. Built with the same logic as the original PyCript, this extension provides a separate solution specifically for WebSockets. It allows users to implement custom encryption and decryption logic using languages like Python, Go, Node.js, C, Bash, etc., ensuring flexibility for unique testing needs.



> [!Note]  
> This is another version of Original PyCript Extension for WebSocket Messages



[![Java CI with Gradle](https://github.com/Anof-cyber/PyCript-WebSocket/actions/workflows/build.yml/badge.svg)](https://github.com/Anof-cyber/PyCript-WebSocket/actions/workflows/build.yml)
![GitHub](https://img.shields.io/github/license/Anof-cyber/PyCript-WebSocket)
![GitHub closed issues](https://img.shields.io/github/issues-closed/Anof-cyber/PyCript-WebSocket)
[![](https://img.shields.io/static/v1?label=Sponsor&message=%E2%9D%A4&logo=GitHub&color=%23fe8e86)](https://github.com/sponsors/Anof-cyber)
![GitHub Release Date](https://img.shields.io/github/release-date/anof-cyber/PyCript-WebSocket?style=plastic)
![GitHub release (latest by date including pre-releases)](https://img.shields.io/github/v/release/anof-cyber/PyCript-WebSocket?include_prereleases)
![GitHub last commit](https://img.shields.io/github/last-commit/Anof-cyber/PyCript-WebSocket)
[![](https://i.ibb.co/qsV4mb9/twitter-2.png)](https://twitter.com/ano_f_)[![](https://i.ibb.co/89LKTrL/linkedin-1.png)](https://www.linkedin.com/in/sourav-kalal/)


## Support

<a href="https://www.buymeacoffee.com/AnoF"><img src="https://img.buymeacoffee.com/button-api/?text=Buy me a coffee&emoji=&slug=AnoF&button_colour=FF5F5F&font_colour=ffffff&font_family=Arial&outline_colour=000000&coffee_colour=FFDD00" /></a>

<a href="https://github.com/sponsors/Anof-cyber"><img src="https://img.shields.io/static/v1?label=Sponsor&message=%E2%9D%A4&logo=GitHub&color=%23fe8e86" alt="Sponsor Anof-cyber" width="230" height="50"></a>


## Reference
- [Original PyCript Extension](https://github.com/Anof-cyber/PyCript)



## Features

- [X] Encrypt & Decrypt Web Socket Messages for both To Server and To Client
- [X] View and Modify the encrypted Messages in plain text
- [X] Complete freedom for encryption and decryption logic


### Image


![PyCript](https://i.ibb.co/yB0bgPF0/Animation2.gif)


## Demo Code

- Demo Code for Encryption Decryption in PyCript WebSocket


> [!Note]  
> **PyCript WebSocket** has a separate logic for handling encryption and decryption, making it incompatible with the demo code from the original **PyCript**. While both extensions share the same core concept, they differ in implementation. **Do not use** [PyCript-Template](https://github.com/Anof-cyber/PyCript-Template) for **PyCript WebSocket**.
 


Below Example is in JavaScript, You can use any language including Bash, C, Python, Java, Go etc.

##### Decryption Code
```javascript
// String Decryption with AES 128 UTF8
const fs = require('fs');
const path = require('path');
var CryptoJS = require("crypto-js");
const { program } = require('commander');
const { Buffer } = require('buffer');

program
  .option('-d, --data <file_path>', 'Path to JSON file containing base64 encoded + encrypted data');
  
program.parse(process.argv);
const options = program.opts();
 
const filePath = options.data;
const absoluteFilePath = path.resolve(filePath);
var data = fs.readFileSync(absoluteFilePath, 'utf8')
// call the functions to handle decryption, 
const originalText = decryptMessage(data);

// write decrypt data to same temp file.
fs.writeFileSync(absoluteFilePath,originalText)

function decryptMessage(encryptedMessage) {
    // your decryption logic
      return decrypted_data;
  }

```

##### Encryption Code

```javascript
// String Decryption with AES 128 UTF8
const fs = require('fs');
const path = require('path');
var CryptoJS = require("crypto-js");
const { program } = require('commander');
const { Buffer } = require('buffer');

program
  .option('-d, --data <file_path>', 'Path to JSON file containing base64 encoded + encrypted data');
  
program.parse(process.argv);
const options = program.opts();
 
const filePath = options.data;
const absoluteFilePath = path.resolve(filePath);
var data = fs.readFileSync(absoluteFilePath, 'utf8')
// call the functions to handle encryption, 
const originalText = encryptMessage(data);

// write encrypted data to same temp file.
fs.writeFileSync(absoluteFilePath,originalText)

function encryptMessage(message) {
    // your encryption logic
    return encrypted_message;
  }

```
