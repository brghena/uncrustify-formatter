# Uncrustify Formatter

Uncrustify is a code formatting tool: https://github.com/uncrustify/uncrustify

This is partially based on the template from https://github.com/61c-teach and the
configuration from https://github.com/tock/libtock-c/tree/master/tools/uncrustify

I like using Uncrustify to format all code given to students for two reasons.
First and most importantly, it ensures a consistent code style. Secondarily, it
is a part of the process of providing students with examples of well-written C
code. Any new code written for projects or labs that will be provided to
students should be formatted with this configuration.

## Installation

Uncrustify can be installed with `brew` or `apt`.

```
 $ apt install uncrustify
```

```
 $ brew install uncrusitfy
```


## Usage

To format a file:

```
 $ uncrustify -c /path/to/uncrustify-formatter/uncrustify.cfg --replace --no-backup FILENAME.c
```


## Configuration


To see documentation for all configurations:

```
 $ uncrustify --show-config
```

Or read a config with comments
[here](https://github.com/uncrustify/uncrustify/blob/master/documentation/htdocs/config.txt)
which is at least mostly up to date.

To see documentation only for the existing configuration, I recommend opening
the file in a web viewer:
[UncrustifyConfig](https://cdanu.github.io/uncrustify_config_preview/index.html)

The particular formatting rules selected here are less important than providing
consistency. The basic formatting configuration we are using was copied from
the [Tock](https://tockos.org) project and is the configuration they use for
formatting embedded systems applications written in C
([libtock-c](https://github.com/tock/libtock-c/tree/master/tools/uncrustify)).
Some additional rules have been added on top of this base configuration.

You may disagree with one stylistic choice or another that is applied. First,
remember that the point is consistency, not any particular style. There are
many valid ways to format C code. If after that you still feel strongly, it's
fine to make changes to the configuration file here as long as you are also
willing to apply them to all of the code in labs and projects and test that the
changes didn't break anything.

