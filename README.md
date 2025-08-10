# SqliteSEECLI
[SQLite Encryption Extension (SEE)](https://sqlite.org/com/see.html) is a proprietary,
paid add-on to SQLite that add RC4, AES-128 (OFB, CCM), AES-256 (OFB) support.
Note that libraries such as SQLCipher encrypts database differently with SQLite SEE,
hence it is impossible to open database encrypted with SQLite SEE using FOSS programs and
libraries (e.g. SQLCipher, DB Browser for SQLite). Programs that can open SQLite encrypted
by SEE (e.g. [SQLiteManager](https://sqlabs.com/sqlitemanager)) almost always cost money.

[Xojo](https://www.xojo.com/) is a proprietary, paid cross-platform app development tool
that happens to use SQLite SEE for encrypting / decrypting database.
This allows me to build a program to encrypt / decrypt SQLite SEE database.
However it only supports AES-128 (OFB) and AES-256 (OFB)

[MBS plugin](https://www.monkeybreadsoftware.de/) provides proprietary plugin to Xojo
that add support of SQLiteSEE AES-128, AES-256 and RC4.

With SqliteSEECLI, you can encrypt / decrypt databases with SQLite SEE using
AES-128 (OFB) and AES-256 (OFB). The `mbs` branch also adds RC4 support.
**Note that AES-128 (CCM) is not supported**

## Download
See [releases page](https://github.com/laggykiller/SqliteSEECLI/releases)

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
