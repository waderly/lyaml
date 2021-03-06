# lyaml NEWS - User visible changes

## Noteworthy changes in release ?.? (????-??-??) [?]


## Noteworthy changes in release 5.1.4 (2015-01-01) [stable]

  - This release is functionally identical to the last.


## Noteworthy changes in release 5.1.3 (2015-01-01) [stable]

  - This release is functionally identical to the last.


## Noteworthy changes in release 5.1.2 (2014-12-27) [stable]

### Bugs Fixed

  - No more spurious .travis.yml is out of date warnings during
    `luarocks install lyaml`.


## Noteworthy changes in release 5.1.1 (2014-12-19) [stable]

### Bugs Fixed

  - When using `sudo make install` instead of LuaRocks, `lyaml.so`
    is now correctly installed to `$luaexecdir`.


## Noteworthy changes in release 5.1.0 (2014-12-17) [stable]

### New Features

  - Lua 5.3.0 compatibility.


## Noteworthy changes in release 5 (2014-09-25) [beta]

### Build

  - Significantly reduced pointer mismatch warnings from modern GNU
    compilers.

### New Features

  - `lyaml.dump` now takes a second argument containing a table of
    potential anchor values in `ANCHOR_NAME = { "match", "elements" }`
    pairs format.  The first time any are matched in the table being
    dumped, they are preceded by `&ANCHOR_NAME` in the output YAML
    document; subsequent matches are not written out in full, but
    shortened to the appropriate `*ANCHOR_NAME` alias.

### Bugs Fixed

  - `yaml.emitter` no longer emits numbers in SINGLE_QUOTE style by
    default.

  - `yaml.emitter ().emit` returns error strings correctly for invalid
    STREAM_START encoding, and MAPPING_START, SEQUENCE_START & SCALAR
    style fields.


## Noteworthy changes in release 4 (2013-09-11) [beta]

### New Features

  - New yaml.emitter API returns an object with an emit method for
    adding events using yaml_*_event_initialize() calls.

  - New yaml.parser API returns a Lua iterator that fetches the next
    event using yaml_parser_parse().

  - New yaml.scanner API returns a Lua iterator that fetches the next
    token using yaml_parser_scan().

  - Beginnings of Specl specs, starting with a reasonably comprehensive
    specifications for the new APIs above.

  - C implementation of lyaml.dump has moved to Lua implementation as
    yaml.dump.

  - C implementation of lyaml.load has moved to Lua implementation as
    yaml.load.

  - The new Lua implementation of lyaml.load () handles multi-document
    streams, and returns a table of documents when the new second
    argument is `true`.


## Noteworthy changes in release 3 (2013-04-27) [beta]

  - This release is functionally identical to the last.

### New Features

  - lyaml builds are now made against Lua 5.1, Lua 5.2 and luajit 2.0.0
    automatically, with every commit.

  - move to a cleaner, automated release system.


## Noteworthy changes in release 2 (2013-03-18) [beta]

  - This release is functionally identical to the last.

  - Use correct MIT license attribution, relicensing build files to match
    Andrew Danforth''s MIT licensed lyaml.c too.


## Noteworthy changes in release 1 (2013-03-17) [beta]

### New Features

  - A binding for libYAML, by Andrew Danforth:  Updated for Lua 5.1 and
    5.2, and packaged as a luarock.

  - I spun this out of Specl (http://github.com/gvvaughan/specl) so that
    other projects may use it, and to simplify the Specl build.

### Known Issues

  - There's not really any documentation, sorry.  Contributions welcome!
