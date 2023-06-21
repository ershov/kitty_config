# Config kitten

Full config 'kitten' for Kitty terminal

(based on original [debug_config](https://github.com/kovidgoyal/kitty/blob/master/kitty/debug_config.py))

## Installation

Copy config.py to your Kitten config (`~/.config/kitty/`).

## Running

Add a mapping to your `kitty.conf`:

```
map shift+cmd+,    kitten config.py
```

or

```
map shift+cmd+,    kitten config.py --info --config --actions --no-deleted
```

... and press your hotley in your Kitten terminal

Or alternatively, use it from the command line:

```bash
$ kitty +kitten config.py | less -R
```

## Useful tips

By default, it will show all config options, all assigned (and default deleted) key and mouse mappings,
and all possible actions with mapped keys and mouse events.
This should encourage the users to learn what actions exist out there and make use of them.

Flags like `--no-empty` and `--no-deleted` will hide these things.

A set of options like `--no-colors --no-deleted --no-empty` or
`--mouse --keys --actions --no-deleted --no-empty`
can be paticularly useful in everyday life.

I myself ended up with just `--no-colors`.

The `--debug` option sets a combination of flags so that the output is the closest to `debug_config`.

## Command line flags:

```
usage: kitty +kitten config.py [options]

Print kitty config.

optional arguments:
  -h, --help                    show this help message and exit
  -d, --diff, --no-diff         Print only the diff vs defaults
  -a, --all, --no-all           Print all parts (default behavior)
  -i, --info, --no-info         Print common info section
  -c, --config, --no-config     Print regular config options section
  -m, --mouse, --no-mouse       Print mouse bindings section
  -k, --keys, --no-keys         Print keyboard shortcuts section
  -l, --colors, --no-colors     Print colors section
  -e, --env, --no-env           Print environment variables section
  -t, --actions, --no-actions   Print actions section
  --deleted, --no-deleted       Print deleted keys
  --empty, --no-empty, --unassigned, --no-unassigned
                                Print unassigned actions
  --debug_config, --no-debug_config, --debug, --no-debug
                                Make output closest to "debug_config"
  --links, --no-links           Use terminal codes for hyperlinks
  --plain, --no-plain, --plaintext, --no-plaintext
                                Disable ansi colors

Notes:
 * Using only --{ARG}'s will include only those parts.
 * Using only --no-{ARG}'s will exclude those part from all.
 * For example, --colors will print only colors,
   while --no-colors will print everything but colors.
 * --all and --no-all will explicitly include or exclude all parts
   which then can be further refined with --{ARG}'s and --no-{ARG}'s.
```

## Screenshots

<img width="685" alt="image" src="https://github.com/ershov/kitty_config/assets/449936/d1c5f7e4-9aba-4693-be78-a0e3430bed7f"><BR>
<img width="714" alt="image" src="https://github.com/ershov/kitty_config/assets/449936/95625fea-0533-4312-bbd6-caf47479990f"><BR>
<img width="899" alt="image" src="https://github.com/ershov/kitty_config/assets/449936/b2416091-8eb1-40cd-90a1-8052ce7bbbf8"><BR>
<img width="930" alt="image" src="https://github.com/ershov/kitty_config/assets/449936/82a88560-fe7c-4674-9647-8232661b1cb5"><BR>

#### `kitten config.py --debug` output
<img width="1498" alt="" src="https://github.com/ershov/kitty_config/assets/449936/e2f42391-7643-45ac-aa51-221530d8ec72">

#### Original `debug_config` output
<img width="1499" alt="image" src="https://github.com/ershov/kitty_config/assets/449936/af2232ef-b658-4061-b9cb-e9c0fd5f904c">

