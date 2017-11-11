
Skinny-C
========

The SKINNY family of tweakable block ciphers is intended for lightweight
implementation in hardware and software, [paper](https://eprint.iacr.org/2016/660.pdf).

The algorithm author's [web site](https://sites.google.com/site/skinnycipher/) provides a
[reference implementation](https://sites.google.com/site/skinnycipher/downloads/skinny_reference.c)
in C, but it isn't terribly efficient - it is intended to be *correct*
to make the algorithm easier to analyse.  And that's OK.

This repository provides an alternative implementation in ISO C99 that is
designed for efficient operation on 32-bit and 64-bit platforms.
Assembly language and SIMD speed-ups are definitely possible,
such as [this](https://github.com/kste/skinny_avx) AVX2 implementation,
and may be added later.

This implementation is designed to have constant-time and constant-cache
behaviour.  There are no lookup tables, particularly for the S-boxes.

Skinny-C is distributed under the terms of the MIT license.

For instructions on how to build and use Skinny-C, see the
<a href="http://rweather.github.com/skinny-c/index.html">documentation</a>.

For more information on this code, to report bugs, or to suggest
improvements, please contact the author Rhys Weatherley via
[email](mailto:rhys.weatherley@gmail.com).