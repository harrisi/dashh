# dash h

An attempt to standardize `-h`|`--help`

# WWSED (What Would Someone Else Do)

Write tests for a parser.

- does `-h` include:
  - usage
    - verbiage?
    - syntax (optional, required, etc.)
    - env vars?
  - options
    - short or long? both?
    - arguments for options?
    - env vars?
    - can description be on new line?
    - ordering?
    - follows single/double dash practices?
  - commands
    - colon format for commands?
    - sectioning commands
    - ?
  - ?

- does the program work for `-h` and `--help`?
- is the output the same for `-h` and `--help`?
  - may the output differ, so long as `--help` has strictly more data than `-h`?
- are the option descriptions aligned?
  - does tab vs space matter?
- is there extra info?
  - example(s)
  - see also
  - bugs
  - author(s)
  - copyright
  - more
- examples?
  - as in examples for how to execute the command to do common tasks for that command
  - format?
- output width
  - max line length?
- flag length/max flag length?
  - if flags exceed some width, should description be on next line?
  - can flags extend multiple lines?
- return code?
  - `npm`, for example, returns 0 when passed `help`, but returns `1` when passed `-h` or `--help`
- is `help` acceptable?
  - maybe with a specific format, implying it's a command and not a flag?
  - maybe it should be identical to `-h`/`--help`
  - I'm not a big fan of this.
- along with `help`, may `-h`/`--help` accept additional flags and/or arguments?
  - `rustc` outputs additional information when `-h`/`--help` is passed `-v`
  - should any work?
- footer
  - version
  - date

# reference implementation(s)

How should it be used? It's really just a linter. Creating linting software for multiple build systems seems nice.

Ability to output some AST? The whole reason for thinking about this is to consume `-h`/`--help` output to generate a manpage. Consider [pandoc](https://pandoc.org)??
