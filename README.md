# yamf

## Why?
I wanted to make my own markup format. One that is easy to understand, that uses well-known formats internally (SVG, JSON, etc), one that could support multiple types of files as one.

Forget having to screenshot your spreadsheet to put it into your Big Presentation, or copy pasting your essay, etc... Have all files in one!

**The reference implementation has not been developed yet. The actual format is not complete either. Watch this space!**

## Structure
YAMF files are lrzip files with either lzo or gzip backend. Programs should ideally support both. (lrzip doesn't need you to know the backend compressor on decompression.)
LZO provides extremely fast compression and decompression, but gzip has a better compression ratio.

**Media** should be embedded in the respective file (inside the contents folder), but can be stored in data/media (recommended for larger files (as they can be loaded separately) and things that cannot be embedded into SVG (or are very inefficient).

**Misc data**, or non-media, unembeddable data should be stored inside data/other.

**The content**, such as slides, spreadsheets, etc, should be stored inside contents.

**Templates** (more on that later) should be stored in master. 

## Templates
Templates are optional, but they are meant to save space! You may be questioning: what's the point of compression then? Templates are more convenient for users, temporary files (folders?) are smaller, and compression/decompression is faster!

## Other stuff
WIP
