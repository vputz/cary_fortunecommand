Cary-fortunecommand
-------------------

A simple cary command to run the unix `cowsay` and `fortune` commands.

Configuration
-------------

In your configuration (usually a `local_conf.py` file), have the following:

```
FORTUNE_CONFIG = dict(COWSAY_PATH="/path/to/cowsay/program",
                      FORTUNE_PATH="/path/to/fortune/program",
                      RANDOM_COWS=dict(cowfile, "short-cow-description"...)
                      FORTUNES_PATH="/path/to/fortunes/directory")
					  ...
from cary_fortunecommand import FortuneCommand
COMMANDS = {..."fortune": (FortuneCommand, FORTUNE_CONFIG)...}
```

the RANDOM_COWS config variable allows you to use a random sampling of cows from
cowsay; the `cowfile` parameter is the prefix of the cow file, while
`short-cow-description` is the textual description that will be sent to the
user.

The email message will be sent in plaintext and HTML versions.
