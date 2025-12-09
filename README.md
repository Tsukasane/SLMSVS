# Adapting Speech Language Model to Singing Voice Synthesis

## SLMSVS Recipe

1. Tokenization of music score conditions and singing waveforms.
2. Multi-stream language model token prediction.
3. Conditional flow matching-based mel-spectrogram generation.
4. A mel-to-wave vocoder.

This repo contain scripts for stage3. For stage1, please follow the [ACE-Opencpop Recipe](https://github.com/espnet/espnet/tree/speechlm/egs2/acesinger/svs1). For stage2, please follow the instruction at [ESPnet-Speechlm](https://github.com/espnet/espnet/tree/speechlm) branch. For stage4, please follow HIFIGAN training in [ParallelWaveGAN](https://github.com/kan-bayashi/ParallelWaveGAN). You may also refer to the [local fork](https://github.com/Tsukasane/ParallelWaveGAN/blob/master/egs/opencpop/voc1/README.md).

## Usage
We use a conditional flow matching model, converting the source Gaussian noise to the target mel spectrogram conditioned on the codec token predicted by SLM.

Please directly modify the path and config at the main entry ``flow.py``.

```
python flow.py
```

## TODOs
- [ ] Update stage1 and stage2 processing scripts to a ESPnet local fork.
- [x] Update stage4 processing scripts to a ParallelWaveGAN local fork.

## Acknowledgements
We thank [INSPIREMUSIC](https://github.com/FunAudioLLM/FunMusic), [Matcha-TTS](https://github.com/shivammehta25/Matcha-TTS) for releasing their code.


