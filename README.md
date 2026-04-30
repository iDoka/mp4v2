# for Apple Silicon [MacOS]

## Sources

This fork contain fixes to build MP4v2 Library on Apple Silicon.

Steps:
```
git clone https://github.com/iDoka/mp4v2
cd mp4v2
autoupdate
aclocal
autoreconf -fi
./configure
### edit GNUmakefile
make
```
after that binaries will located at `.libs` filder.

## Binaries 

See releases to reach pre-built binaries for Apple Silicon ARM64 [Darwin]

