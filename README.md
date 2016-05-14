# About

This is an un-official fork of the Lapos tagger, based on version 0.1.2. [Official source available here](http://www.logos.ic.i.u-tokyo.ac.jp/~tsuruoka/lapos/).

The goal of this fork is to add Unicode support for use in the Classical Language Toolkit. Once fixed, the CLTK hopes that these changes will be merged upstream.

# Changes

To compile on Clang, a few changes need to be made, namely removing `tr1` from, e.g., (`<tr1/unordered_map>` and `td::tr1::unordered_map`).


# License
Lapos created by Yoshimasa Tsuruoka, Yusuke Miyao, and Jun'ichi Kazama. For all technical details, see `README` and for license `LICENSE`.
