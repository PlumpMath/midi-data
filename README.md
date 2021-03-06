[![Clojars Project](http://clojars.org/org.clojars.triss/midi-data/latest-version.svg)](http://clojars.org/org.clojars.triss/midi-data)

# midi-data

Handles parsing of MIDI data tuples to maps containing friendly representations
of the events they represent.

## Rationale

To my knowledge all of Clojure's existing MIDI related namespaces complect the
representation of MIDI messages with the mechanism for sending them.

This library concerns its self only with the representation of MIDI data and
conversion to and from tuples of 3 values utilised by the vast majority of
back ends, for example [WebMIDI](http://www.w3.org/TR/webmidi/) 
and [javax.sound.midi](http://docs.oracle.com/javase/7/docs/api/javax/sound/midi/package-summary.html)
both communicate using these.

## Documentation

Documentation for this project can be found here: http://triss.github.io/midi-data/ 

It's been written in a literate style and can be generated using
[Marginalia](https://github.com/gdeer81/marginalia) and can be recompiled
with:
```
lein marg ./src/midi_data/core.cljc ./test/midi_data/core_test.clj
```
## Testing

The project uses [Midje](https://github.com/marick/Midje/) for testing.

### How to run the tests

`lein midje` will run all tests.

`lein midje namespace.*` will run only tests beginning with "namespace.".

`lein midje :autotest` will run all the tests indefinitely. It sets up a
watcher on the code files. If they change, only the relevant tests will be
run again.

## Copyright

Copyright © 2015 Tristan Strange <tristan.strange@gmail.com>

This work is free. You can redistribute it and/or modify it under the
terms of the Do What The Fuck You Want To Public License, Version 2,
as published by Sam Hocevar. See http://www.wtfpl.net/ for more details.
