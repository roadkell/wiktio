## Simple and memory-efficient word extractor for Wiktionary ##

```
  // ___  ___ __   __   \\
 //   \\   \\ /    /     \\
//     \\   \\    /       \\
\\      \\  /\\  /        //
 \\      \\/  \\/iktion  //
  \\                    //
```

[![Hippocratic License HL3-CORE](https://img.shields.io/static/v1?label=Hippocratic%20License&message=HL3-CORE&labelColor=5e2751&color=bc8c3d)](https://firstdonoharm.dev/version/3/0/core.html)

This is a small tool for extracting a list of all words from Wiktionary dumps, with optional regexp filtering.

It is not a full-featured parser/extractor for Wiktionary data. It doesn't extract definitions, translations, synonyms, etc. If you need that, check out [other projects](#other-projects).

Currently, only [ru-wiktionary](https://ru.wiktionary.org/) dumps are supported. More languages will (hopefully) follow.

### Usage ###

```
python3 wiktion.py [-h] [-l LANG] [-p POS] [-r REGEX] infile [outfile]

positional arguments:
	infile                      Wiktionary XML dump file (bz2-compressed), e.g.,
	                            'ruwiktionary-latest-pages-articles.xml.bz2'
	outfile                     list of extracted words (plain text)

options:
	-h, --help                  show this help message and exit
	-l LANG, --lang LANG        filter words by language, e.g., 'ru', 'en'
	-p POS, --pos POS           filter by part of speech, e.g.,
	                            'сущ', 'гл', 'adv' (sic), 'прил'
	-r REGEX, --regex REGEX     optional regex string to filter page text by
```

Dumps can be downloaded at https://dumps.wikimedia.org/.

The required dumps are named as
`[lang]wiktionary-[date|latest]-pages-articles[-multistream].xml.bz2`
(e.g., `ruwiktionary-latest-pages-articles.xml.bz2`
or `ruwiktionary-20220720-pages-articles-multistream.xml.bz2`)

### Other projects ###

- https://github.com/tatuylonen/wiktextract
- https://github.com/wswu/yawipa
- https://github.com/slowwavesleep/RuWiktionaryParser
- https://github.com/benreynwar/wiktionary-parser
- https://github.com/dkpro/dkpro-jwktl
- https://github.com/componavt/wikokit
- https://github.com/gambolputty/wiktionary-de-parser

Even more:

- https://github.com/topics/wiktionary-parser
- https://github.com/topics/wiktionary-dump
- https://github.com/topics/wiktionary
- https://github.com/search?q=wiktionary

### License ###

[Hippocratic License 3.0](https://github.com/roadkell/wiktion/blob/main/LICENSE.md)

[lxml](https://lxml.de/): [BSD](https://github.com/lxml/lxml/blob/master/doc/licenses/BSD.txt)

[tqdm](https://github.com/tqdm/tqdm): [MIT](https://github.com/tqdm/tqdm/blob/master/LICENCE)
