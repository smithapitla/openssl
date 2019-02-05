# openssl

openssl enc -aes-128-cbc -a -salt -pass pass:crcd_acct_note &gt; encryption.txt

-a, -A, -base64
These flags tell OpenSSL to apply Base64-encoding before or after the cryptographic operation. The -a and -base64 are equivalent. If you want to decode a base64 file it is necessary to use the -d option. By default the encoded file has a line break every 64 characters. To suppress this you can use in addition to -base64 the -A flag. This will produce a file with no line breaks at all. You can use these flags just for encoding Base64 without any ciphers involved.

-salt, -nosalt, -S salt
These options allow to switch salting on or off. With -S salt it is possible to explicitly give its value (in hexadecimal).

-pass arg
This specifies the password source. Possible values for arg are pass:password or file:filename, where password is your password and filename file containing the password.

