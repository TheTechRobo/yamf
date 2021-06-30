# yamf

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
