# bashcrypto
## Usage

### Options
```bash
Usage: bashcrypt [OPTION] -i INPUT -o OUTPUT
-p	use public/privatekey for encryption/decryption
-e	encrypt
-d	decrypt
-i	input
-o	output
-s	create shasum
-t  tarmode
-h	help message
```
### Create public/private key
```bash
# Create public/private key
openssl req -x509 -nodes -newkey rsa:4096 -keyout privatekey.pem -out publickey.pem
# Create public/private key with password protection
openssl req -x509 -newkey rsa:4096 -keyout privatekey.pem -out publickey.pem
```
### Encrypt
```bash
# encrypt with a password:
./bashcrypto -e -i test.txt -o test.txt.enc
# encrypt all files in a folder
./bashcrypto -e -i dir -o enc
# encrypt with your public key:
./bashcrypto -e -p public.pem -i test.txt -o ultrasecret.dat
# encrypt all files in a folder
./bashcrypto -e -p public.pem -i dir -o ultrasecret.dat
```
### Decrypt
```bash
# decrypt with password:
./bashcrypto -d -i test.txt.enc -o plain.txt
# decrypt with private key:
./bashcrypto -d -p private.pem -i ultrasecret.dat -o plain.txt
```

## To-Do
- ?

### Example

apple@apple-virtual-machine:~/Desktop/maplestory/aa/bashcrypto$ ./bashcrypto -e -p publickey.pem -i /home/apple/Desktop/maplestory/aa/terraform-provider-azurerm/ -o holy

[+] directory found!


[+] ENCRYPT
[+] INPUT:  /home/apple/Desktop/maplestory/aa/terraform-provider-azurerm/
[+] OUTPUT: holy


[!] Your file will be encypted now!

      
[+] Done!
apple@apple-virtual-machine:~/Desktop/maplestory/aa/bashcrypto$ 

