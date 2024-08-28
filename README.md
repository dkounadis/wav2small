# wav2small

### WAV2SMALL: DISTILLING WAV2VEC2 TO 72K PARAMETERS FOR LOW-RESOURCE SPEECH EMOTION RECOGNITION

> Speech Emotion Recognition (SER) needs high computational resources to overcome the challenge of substantial annotator disagreement. Today SER is shifting towards dimensional annotations of arousal, dominance, and valence (A/D/V). Universal metrics as the L2 distance prove unsuitable for evaluating A/D/V accuracy due to non converging consensus of annotator opinions. However, Concordance Correlation Coefficient (CCC) arose as an alternative metric for A/D/V where a model's output is evaluated to match a whole dataset's CCC rather than L2 distances of individual audios. Recent studies have shown that Wav2Vec2.0 / WavLM architectures outputing a float value for each A/D/V dimension achieve today's State-of-the-art (SOTA) CCC on A/D/V. The Wav2Vec2.0 / WavLM family has high computational footprint, but training tiny models using human annotations has been unsuccessful. In this paper we use a large Transformer SOTA A/D/V model as Teacher/Annotator to train 5 student models: 4 MobileNets and our proposed Wav2Small, using only the Teacher's A/D/V predictions instead of human annotations. We chose MobileNet-V4 / MobileNet-V3 as students, as MobileNet has been designed for fast execution times. We propose Wav2Small an architecture designed for minimal parameter number and RAM consumption. Wav2Small with an .onnx (quantized) of only 60KB is a potential solution for A/D/V on hearing aids, having only 72K parameters vs 3.12M parameters for MobileNet-V4-Small. The Teacher model we construct sets a new SOTA on the MSP Podcast Test-1 dataset with valence CCC=0.676.

**[arXiv](https://arxiv.org/abs/2408.13920)**

```
WAV2SMALL: DISTILLING WAV2VEC2 TO 72K PARAMETERS FOR LOW-RESOURCE SPEECH EMOTION RECOGNITION
Dionyssos Kounades-Bastian, Oliver Schrüfer, Anna Derington, Hagen Wierstorf,
Florian Eyben, Felix Burkhardt, Björn W. Schuller.
arXiv preprint https://arxiv.org/pdf/2408.13920
```


**[HuggingFace Code](https://huggingface.co/dkounadis/wav2small)**

    



