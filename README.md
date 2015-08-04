Cary-fortunecommand
-------------------

A simple cary command to run the unix `cowsay` and `fortune` commands.

Configuration
-------------

In your configuration (usually a `local_conf.py` file), have the following:

```
FORTUNE_CONFIG = dict(COWSAY_PATH="/path/to/cowsay/program",
                      FORTUNE_PATH="/path/to/fortune/program",
                      FORTUNES_PATH="/path/to/fortunes/directory")
					  ...
from cary_fortunecommand import FortuneCommand
COMMANDS = {..."fortune": (FortuneCommand, FORTUNE_CONFIG)...}
```
