> First draft

Primary Key
    - Certification -> private key used to certify sub keys
                    -> share public key with others
    => Local, usb stick

Sub Keys
    - Encrypt       -> public key email/files encryption ==> private key decrypt (emails/files encrypt)
                    -> only accessible for private key owner
    - Sign          -> private key sign ==> public key verifyn (git commit/email/files sign)
                    -> verify sender/owner
    - Certification -> "copy" of primary key
    => Smartcard (eg. YubiKey, Nitrokey)

Best practice: 2 Smartcards (both certified by primary key)

Real world application:
- Git commit signen                     -> configure fingerprint
- Emails signen (Outlook, Thunderbird)  -> multiple email addresses (alias)
- SSH Authentication                    -> putty and git

List of contents:
- Key generation -> Overview of files (primary key: private key -> lock, public key -> share; sub keys: smartcard; revoke)
  => gpg4win, cygwin, kleopatra
- Real world applications
    - Git commit sign
    - Emails sign
        - Thunderbird
        - Outlook
    - SSH Authentication
