# test-music

testing out [abcjs](https://github.com/paulrosen/abcjs), rendering and playing music written in ABC notation.

abc music data from [ABC version of the Nottingham Music Database](http://abc.sourceforge.net/NMD/)

Also interesting:
- [How to understand ABC](http://abcnotation.com/blog/2010/01/31/how-to-understand-abc-the-basics/)
- [abcbot](http://ecf-guest.mit.edu/~jc/music/bot/abcbot)
- [An ABC Library of Morris Tunes](http://www.ucolick.org/~sla/morris/music/abclib.html)
- [JC's ABC music collection](http://ecf-guest.mit.edu/~jc/music/abc/)
- Get [soundfonts](https://github.com/gleitz/midi-js-soundfonts)

Basic ABC notation template:

```
X:1 [reference #, can be any number]
T:Paddy O'Rafferty [title]
C:Trad. [composer]
M:6/8 [meter, *required]
L:1/4 [base note length, can be in header or in tune]
K:D [key, required, always last header field, always followed by the notes of the tune]
dff cee|def gfe|dff cee|dfe dBA|dff cee|def gfe|faf gfe|1 dfe dBA:|2 dfe dcB|]
~A3 B3|gfe fdB|AFA B2c|dfe dcB|~A3 ~B3|efe efg|faf gfe|1 dfe dcB:|2 dfe dBA|]
fAA eAA|def gfe|fAA eAA|dfe dBA|fAA eAA|def gfe|faf gfe|dfe dBA:|
```

Notes:
- `CDEFGAB` = bottom octave, `C` = middle C, (with no spaces notes will have beams)
- `cdefgab` = top octave 
- `,` = down an octave, `'` = up an octave
- a number after the note = the length * the base length
- `|` = bar line; `|]` double bar; `|:` repeat `:|`
- `~` = ornament, roll; `{c}`

Example, four octaves:

```
X:1
T:Notes
M:C
L:1/4
K:C
C, D, E, F,|G, A, B, C|D E F G|A B c d|e f g a|b c' d' e'|f' g' a' b'|]
```
