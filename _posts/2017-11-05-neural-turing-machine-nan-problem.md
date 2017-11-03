---
layout: post
title:  "A Solution for the Nan Problem with Neural Turing Machines"
date:   2017-11-05 14:39:16 +0000
---

Several attempts to replicate the [Neural Turing Machine](https://arxiv.org/abs/1410.5401) have reported problems with the gradients becoming NaN [[1](https://github.com/carpedm20/NTM-tensorflow), [2](https://github.com/snipsco/ntm-lasagne)]. This problem is caused by the sharpening operation defined by equation 9 in the [original paper](https://arxiv.org/pdf/1410.5401.pdf):

$$
w_t(i) \leftarrow \frac{\tilde{w}_t(i)^{\gamma_t}}{\sum_{j} \tilde{w}_t(j)^{\gamma_t}}
$$


<script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.0/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>
