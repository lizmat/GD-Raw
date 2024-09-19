[![Actions Status](https://github.com/raku-community-modules/GD-Raw/actions/workflows/linux.yml/badge.svg)](https://github.com/raku-community-modules/GD-Raw/actions) [![Actions Status](https://github.com/raku-community-modules/GD-Raw/actions/workflows/macos.yml/badge.svg)](https://github.com/raku-community-modules/GD-Raw/actions)

NAME
====

GD::Raw - Low level language bindings to GD Graphics Library

SYNOPSIS
========

```raku
use GD::Raw;

my $fh = fopen("my-image.png", "rb");
my $img = gdImageCreateFromPng($fh);
LEAVE gdImageDestroy($_) with $img;

say "Image resolution is ", gdImageSX($img), "x", gdImageSX($img);
```

DESCRIPTION
===========

`GD::Raw` is a low level language bindings to LibGD. It does not attempt to provide you with an rakuish interface, but tries to stay as close to its `C` origin as possible.

LibGD is large and this module far from covers it all. Feel free to add anything your missing and submit a pull request!

AUTHORS
=======

  * Dagur Valberg Johannsson

  * Raku Community

COPYRIGHT AND LICENSE
=====================

Copyright 2013 - 2018 Dagur Valberg Johannsson

Copyright 2024 Raku Community

This library is free software; you can redistribute it and/or modify it under the Artistic License 2.0.

