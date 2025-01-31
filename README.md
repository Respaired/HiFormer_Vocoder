---
license: mit
tags:
- vocoder
- audio
- speech
- tts
---

# Model Card for Model ID

This Vocoder, is a combination of [HiFTnet](https://github.com/yl4579/HiFTNet) and [Ringformer](https://github.com/seongho608/RingFormer). it supports Ring Attention, Conformer and Neural Source Filtering etc.
This repository is experimental, expect some bugs and some hardcoded params.

The default setting is 44.1khz - 128 Mel bin. if you want to change it to 24khz, copy the config from HiFTnet (make sure to copy its pitch extractor, both the model + the checkpoint.), then change 128 to 80 in LN-384 of the models.py. then uncomment the "multiscale_subband_cfg" for the 24khz version.

Huge Thanks to [Johnathan Duering](https://github.com/duerig) for his help. I mostly implemented this based on his [STTS2 Fork](https://github.com/duerig/StyleTTS2/tree/main)
