# gapass
Command line wrapper for auto submit TOTP/HOTP verification code and password

## Quick Start
- [Download](https://github.com/yavitalic/gapass.git) the current release of `gapass`
- Copy to `$HOME/bin/gapass` or wherever you want
- Make it executable: `chmod 755 $HOME/bin/gapass`
- Create `$HOME/.gapass`
- Set the configuration file permissions: `chmod 600 $HOME/.gapass`
- ...and execute: `gapass <command> <params>`

### Configuration File
The general format is:
```
name=key
```
An example file would be
```
[gapass]
secret=1234567890123
password=9876543210
```

### Using
```
$ gapass ssh myhost
```

### Command Line Flags

#### Help

Use the `--help` or `-h` flag to show the help of `gapass`.
```
$ gapass --help
Usage: gapass [options] <command> <parameters>
    -d, --decode                     decode secret key and password from base64
    -e, --env                        secret key and password is passed as env var GA_KEY and AD_PASS
    -f, --file=FILENAME              take secret key, password and prompt from INI file (~/.gapass by default)
    -s, --secret=SECRET              provide secret key as argument (security unwise)
    -p, --password=PASSWORD          provide password as argument (security unwise)
    -C, --code-prompt=PROMPT         which string should search for to detect a verification code prompt
    -P, --password-prompt=PROMPT     which string should search for to detect a password prompt
    -I, --interactive-prompt=PROMPT  which string should search for to detect a interactive prompt
    -h                               show help
    -v                               verbose messages
```
