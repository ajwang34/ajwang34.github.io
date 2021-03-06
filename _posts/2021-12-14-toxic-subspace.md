---
layout: post
title: "Simple Text Detoxification by Identifying a Linear Toxic Subspace in Language Model Embeddings"
date:   2021-12-13
categories: projects
---

Abstract
--------
#### [Arxiv]()  

Large pre-trained language models are often trained on large volumes of internet data, some of which may contain toxic or abusive language. Consequently, language models encode toxic information, which makes the real-world usage of these language models limited. Current methods aim to prevent toxic features from appearing in text. We hypothesize the existence of a low-dimensional toxic subspace in the latent space of pre-trained language models, the existence of which suggests that toxic features follow some underlying pattern and are thus removable. To construct this toxic subspace, we propose a method to generalize toxic directions in the latent space. We also provide a methodology for constructing parallel datasets using a context based word masking system. Through our experiments, we show that when the toxic subspace is removed from a set of sentence representations, almost no toxic representations remain in the result. We demonstrate empirically that the subspace found using our method generalizes to multiple toxicity corpora, indicating the existence of a low-dimensional toxic subspace. 