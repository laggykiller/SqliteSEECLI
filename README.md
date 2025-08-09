# SqliteSEECLI
[SQLite Encryption Extension (SEE)](https://sqlite.org/com/see.html) is a proprietary,
paid add-on to SQLite that add RC4, AES-128 (OFB, CCM), AES-256 (OFB) support.
Note that libraries such as SQLCipher encrypts database differently with SQLite SEE,
hence it is impossible to open database encrypted with SQLite SEE with FOSS programs and
libraries (e.g. SQLCipher, DB Browser for SQLite)

[Xojo](https://www.xojo.com/) is a propiretary, paid cross-platform app development tool
that happens to use SQLite SEE for encrypting / decrypting database.
This allows me to build a program to encrypt / decrypt SQLite SEE database.

With SqliteSEECLI, you can encrypt / decrypt databases with SQLite SEE using
AES-128 (OFB) and AES-256 (OFB). **Note that RC4 and AES-128 (CCM) are not supported**

## Usage
```
  SqliteSEECLI - Encrypt / Decrypt SQLite database with SQLite Encryption Extension

Help:
  -h, --help           Show help
  -f FILE, --file=FILE Path to SQLite file
  -m STR, --mode=STR   Encryption or Decryption [can be: `encrypt',
                       `decrypt']
  -a STR, --algo=STR   Algorithm [can be: `aes128', `aes256']
  -k STR, --key=STR    Key
Example: SqliteSEECLI -f secret.sqlite3 -m decrypt -a aes128 -k A1B2C3D4E5F6
```

## Credits
https://github.com/jcowgar/xojo-option-parser