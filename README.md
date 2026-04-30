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
# edit GNUmakefile
sed -i '' 's/CXXFLAGS = -g -O2 -fvisibility=hidden$/CXXFLAGS = -g -O2 -fvisibility=hidden -Wno-c++11-narrowing/' Makefile
make
```
after that binaries will located at `.libs` filder.

### editing GNUmakefile before run `make`

find `CXXFLAGS` definition:
```
grep -n "^CXXFLAGS" GNUmakefile
533:CXXFLAGS = -g -O2 -fvisibility=hidden
```
then put `CXXFLAGS += -Wno-c++11-narrowing` right after 533 string


## Binaries 

See releases to reach pre-built binaries for Apple Silicon ARM64 [Darwin]

