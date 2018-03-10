# CifraChaCha20Poly1305

An Arduino library that contains ChaCha20 and Poly1305 implementations from 
Joseph Birr-Pixton's [Cifra](https://github.com/ctz/cifra) project.

After removing files not needed for ChaCha20 and Poly1305, only minimal changes 
were required to build Cifra's source code with the Arduino toolchain.  

1. handy.h was moved from src/ext so the C file includes didn't have to change 
   (there's no easy way to add an include path for src/ext when Arduino builds libraries)
2. The "static" keyword was removed from array size initializers
3. Wrap header files with non-static functions with 'extern "C" {}'

## Project

Find CifraChaCha20Poly1305 at [https://github.com/sterwill/CifraChaCha20Poly1305](https://github.com/sterwill/CifraChaCha20Poly1305)

## Upstream Version 

The files in this library are derived from [this commit of Cifra](https://github.com/ctz/cifra/tree/319fdb764cd12e12b8296358cfcd640346c4d0dd).

## License

[CC0](https://creativecommons.org/publicdomain/zero/1.0/).

Please attribute the author.  This is a request only, and not a license term.

## Author

Joseph Birr-Pixton <jpixton@gmail.com>

## Arduino Library Maintainer

Shaw Terwilliger <sterwill@tinfig.com>
