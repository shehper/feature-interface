### Feature Interface

This repository contains HTML code for an interface that helps explore features as learned by a Sparse AutoEncoder (SAE). Please see the interface [here](https://shehper.github.io/feature-interface/). The interface hopes to emulate Anthropic's [visualization of features](https://transformer-circuits.pub/2023/monosemantic-features/vis/a1.html) accompanying their [Sparse Dictionary Learning](https://transformer-circuits.pub/2023/monosemantic-features/index.html) paper.

I trained the autoencoder on MLP activations of 1-layer transformer with 512 neurons. The number of features was 4096. 93% of these were alive at the end of training; only 5% of which were ultra-low density neurons. Each feature page contains a feature density histogram, a list of top 10 contexts on which the feature activates, and random samples of activations in various ranges of activation values. Most features are quite interpretable. (There seems to be a correlation between ease of interpretation and bimodality of feature density histograms.) 

<!-- Here is a short list of some interesting features.

- [A feature that activations on Cyrilic vowels](https://shehper.github.io/feature-interface/?page=3987)
- [A feature that activates on token " to"](https://shehper.github.io/feature-interface/?page=1859)
 -->

The codebase used to train the autoencoder is available in another repository [here](https://github.com/shehper/monosemantic). This interface and the training repository are still a work in progress. For example, [Anthropic's visualization](https://transformer-circuits.pub/2023/monosemantic-features/vis/a1.html) covers many more aspects of each feature, such as feature ablations and correlation with neurons. I hope to work on these aspects and also make the code easier to use by others in the future.


### Related Work
Other people have also trained SAEs on language model activations. Please see a (possibly incomplete) list below.

- [Cunningham et al's paper on Sparse Autoencoders](https://arxiv.org/abs/2309.08600)
- [Joseph Bloom's implementation](https://github.com/jbloomAus/mats_sae_training)
- [Neel Nanda's implementation](https://github.com/neelnanda-io/1L-Sparse-Autoencoder)
- [Callum McDougall's exercises on SAEs](https://github.com/callummcdougall/sae-exercises-mats/tree/main)
- [SAE library by AI Safey Foundation](https://github.com/ai-safety-foundation/sparse_autoencoder)