> This guide is in the making. Get notified when its done by watching the repository.

# PGP for Windows

This is a practical guide on how to use **P**retty **G**ood **P**rivacy (PGP) under windows. This guide was created to introduce security aware people to this complex topic. It is different to other guides, because it tries to give context to every step you take. You will need approximately **??** minutes to set up your keys.

Collaboration between [nottheend](https://github.com/nottheend) and [stephan-strate](https://github.com/stephan-strate).

## Key generation

Primary key vs. Sub keys

## Real world applications

### Sign git commits

### SSH authentication

### Sign Emails

### Encrypt Emails

## Resources / Credits

- https://blogs.itemis.com/en/openpgp-on-the-job-part-1-what-is-it (8-part blog series about PGP on the job)
- https://medium.com/@ryanmillerc/use-gpg-signing-keys-with-git-on-windows-10-github-4acbced49f68
- https://github.com/drduh/YubiKey-Guide

---

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
