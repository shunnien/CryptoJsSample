
## [Crypto-JS][1]
我主要採用 code.google 上的資料說明為主，此 Library 支援
* Hashers
	* MD5
	* SHA-1
	* SHA-2
	* SHA-3
	* RIPEMD-160
  * HMAC
	  * HMAC-MD5
		* HMAC-SHA1
		* HMAC-SHA256
		* HMAC-SHA512
	* PBKDF2
* Ciphers
	* AES
  * DES, Triple DES
  * Rabbit
  * RC4, RC4Drop
  
除了上述支持的算法之外，尚有許多功能，此篇著重在 [CryptoJS][1] 中的 [AES][2] 加解密部分，順便弄了簡單的加解密 sample 看之後有時間來慢慢將他把功能完善；好了，閒話不多說，還是趕快把此次範例中的注意事項與 code 展示吧。

以下為官方所展示的的 AES 範例
```
<script src="http://crypto-js.googlecode.com/svn/tags/3.1.2/build/rollups/aes.js"></script>
<script>
    var encrypted = CryptoJS.AES.encrypt("Message", "Secret Passphrase");

    var decrypted = CryptoJS.AES.decrypt(encrypted, "Secret Passphrase");
</script>
```
CryptoJS 在 The Advanced Encryption Standard (AES) 支援了
* AES-128
* AES-192
* AES-256

另外，像這個官方範例其實預設了很多預設值，假如沒有指定 key 長度的話，預設是使用 256-bit。

<iframe width="100%" height="300" src="//jsfiddle.net/wiamyu/7t32w98f/13/embedded/" allowfullscreen="allowfullscreen" frameborder="0"></iframe>

比較需要注意一下解碼，解碼出來的資料預設是經過編碼轉換過的，所以你要得到你原來的資料，要在編碼轉換一次。

最後提供二個線上加解密資源，有一個其實是 Demo 

* [在线工具 - 开源中国](http://tool.oschina.net/encrypt)
* [LJavaScript Cryptography](http://cryptojs.altervista.org/api/demo.html)
* [crypto-js 的 Github](https://github.com/brix/crypto-js)

[1]: https://code.google.com/p/crypto-js/ "crypto-js"
[2]: http://www.codedata.com.tw/social-coding/aes/ "AES 對稱式加解密法 - CodeData"
