[![Build Status](https://travis-ci.org/cltk/lapos.svg?branch=apple)](https://travis-ci.org/cltk/lapos)

# About

This is an un-official fork of the Lapos tagger, based on version 0.1.2. [Official source available here](http://www.logos.ic.i.u-tokyo.ac.jp/~tsuruoka/lapos/).

The goal of this fork is to add Unicode support for use in the Classical Language Toolkit. Once fixed, the CLTK hopes that these changes will be merged upstream.

# Use

For full instructions, see `README`. The CLTK's Latin model (based on Perseus treebanks) was made with the following command:

``` shell
$ ./lapos-learn -m ./model latin_training_set.pos
```

For running, use `echo` to pass one sentence at a time:

``` shell
$ echo "He opened the window." | ./lapos -t -m ./model_wsj02-21
He/PRP opened/VBD the/DT window/NN ./.
```


# Changes

To compile on Clang, a few changes need to be made, namely removing `tr1` from, e.g., (`<tr1/unordered_map>` and `td::tr1::unordered_map`).

We also increased the maximum number of tags, from 50 to 2000 (in `crf.h`, commenting out `enum { MAX_LABEL_TYPES = 50 };` and uncommenting `const static int MAX_LABEL_TYPES = 2000;`). Also removed the unnecessary empty-input-line warning in `crf.ppp` (``"warning: empty sentence"``).

# License
Lapos created by Yoshimasa Tsuruoka, Yusuke Miyao, and Jun'ichi Kazama. For all technical details, see `README` and for license `LICENSE`.
