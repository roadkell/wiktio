## Simple and memory-efficient word extractor for Wiktionary ##

```
   //  ___  ___ __   __  \\
  //    \\   \\ /    /    \\
 //      \\   \\    /      \\
 \\       \\  /\\  /       //
  \\       \\/  \\/       //
   \\  w  i  k  t  i  o  //
```

This is a small tool for extracting a list of all words from Wiktionary dumps, with optional regexp filtering.

It is not a full-blown general purpose parser/extractor for Wiktionary data. It doesn't extract definitions, translations, synonyms, etc. If you need that, check out [Other projects](#other-projects).

Currently, only [ru-wiktionary](https://ru.wiktionary.org/) dumps are supported. More languages will follow.

### Usage ###

```
python3 wiktio.py [-h] [-l LANGUAGE] [-p PARTOFSPEECH] [-r REGEX] infile [outfile]

positional arguments:
	infile                                          Wiktionary XML dump file (bz2-compressed), e.g.,
	                                                'ruwiktionary-latest-pages-articles.xml.bz2'
	outfile                                         list of extracted words (plain text)

options:
	-h, --help                                      show this help message and exit
	-l LANGUAGE, --language LANGUAGE                filter words by language, e.g., 'ru', 'en'
	-p PARTOFSPEECH, --partofspeech PARTOFSPEECH    filter by part of speech, e.g.,
	                                                'сущ', 'гл', 'adv' (sic), 'прил'
	-r REGEX, --regex REGEX                         optional regex string to filter page text by
```

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

[Hippocratic License 3.0](https://firstdonoharm.dev/)
