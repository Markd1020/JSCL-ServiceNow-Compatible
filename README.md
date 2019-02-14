# SJCL-ServiceNow-Compatible Encryption library to perform AES (Rijndael) encryption.

(Works only in Scoped App) Everything is packed into a single file. 
Made modifications to make CBC mode available for use. By defult CBC mode is disabled. 
Save the code from SJCL.js to a script include.

HOW TO USE guide with an example code



```
// you can choose any format like sjcl.codec.base32 or sjcl.codec.hex or sjcl.codec.bytes

key = sjcl.codec.base64.toBits(" Your Secret Key in Base64 Format "); 

iv = sjcl.codec.base64.toBits(" Initialization Vector in Base64 Format ");

message = sjcl.codec.utf8String.toBits("Message to be encrypted");

aes = new sjcl.cipher.aes(key);

var cipher = sjcl.mode["cbc"].encrypt(aes, message, iv); // pass aes, message, iv. choose one of the three modes
```
