# To Diverge or Not to Diverge: A Morphosyntactic Perspective on Machine Translation vs Human Translation
This repository contains the annotations from the paper "[To Diverge or Not to Diverge: A Morphosyntactic Perspective on Machine Translation vs Human Translation](https://arxiv.org/abs/2401.01419)."

## Overview
Three language pairs are included in the analyses: English->Chinese, English->German, and English->French. For each language pair, about 1 million examples are automatically annotated by our in-house tools. More specifically, each example is a triplet of (src, ref, hyp), corresponding to the source, the reference, and the hypothesis (i.e., prediction) from a trained Transformer-based encoder-decoder MT system. Five **parallel** files (all compressed into `.gz` format) can be found for each language pair (denoted below by `<lp>`):
* `<lp>.src.conll`: Dependency parse tree for the source in CONLL format.
* `<lp>.ref.conll`: Dependency parse tree for the reference in CONLL format.
* `<lp>.hyp.conll`: Dependency parse tree for the hypothesis in CONLL format.
* `<lp>.ref.pharaoh`: Word alignment for the source-reference translation pair stored in the [Pharaoh](https://opennmt.net/OpenNMT-tf/alignments.html) format. Alignment uses 1-based indexing, since 0 is reserved for the root node for dependency trees.
* `<lp>.hyp.pharaoh`: Word alignment for the source-hypothesis translation pair stored in the Pharaoh format.

## Citation
If you use the annotations from this work, please cite the following paper:
```
@misc{luo2024diverge,
      title={To Diverge or Not to Diverge: A Morphosyntactic Perspective on Machine Translation vs Human Translation}, 
      author={Jiaming Luo and Colin Cherry and George Foster},
      year={2024},
      eprint={2401.01419},
      archivePrefix={arXiv},
      primaryClass={cs.CL}
}
```