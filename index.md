This is the demo page for the Bachelor's Thesis **Dataset Generation for Virtual Analog Modelling with Neural Network Models**


## Abstract
 Here, you can listen to several examples showing the input audio, the target signal processed using Farina’s partitioned convolution method (Torger & Farina, 2001) to emulate the reverberation effect, and the output generated by a neural network model (GCN) trained on data derived from the EGDB dataset (Chen et al., 2022). The EGDB dataset consists of electric guitar performances, which were processed using partitioned convolution to create high-quality input-target pairs for training and evaluation. This demo allows for a direct comparison between the reference processing and the neural model’s output, facilitating the assessment of model performance in virtual analog audio effects modelling.


### Audio Examples
The following examples allow you to compare the input audio (dry), the target signal (wet, processed using Farina’s partitioned convolution method), and the output generated by a neural network model (GCN).

| Example | Input (Dry) | Target (Wet, Farina's Partitioned) | Model Output |
|---------|-------------|-------------------------|--------------|
| 1 | <audio src="Audio_Examples\inp_44100\01_SaxophoneCloseMic1.wav" controls preload></audio> | <audio src="Audio_Examples\Partitioned_outputs\01_SaxophoneCloseMic1.wav" controls preload></audio> | <audio src="Audio_Examples\Model_outputs\procesado_01_SaxophoneCloseMic1.wav" controls preload></audio> |
| 2 | <audio src="Audio_Examples\inp_44100\2.wav" controls preload></audio> | <audio src="Audio_Examples\Partitioned_outputs\2.wav" controls preload></audio> | <audio src="Audio_Examples\Model_outputs\procesado_2.wav" controls preload></audio> |
| 3 | <audio src="Audio_Examples\inp_44100\10_Piano.wav" controls preload></audio> | <audio src="Audio_Examples\Partitioned_outputs\10_Piano.wav" controls preload></audio> | <audio src="Audio_Examples\Model_outputs\procesado_10_Piano.wav" controls preload></audio> |

### Pedalboard vs Partitioned Convolution Comparison
Below you can compare the same input processed with Farina’s partitioned convolution method and with Pedalboard (Spotify, 2023), including Pedalboard outputs normalized to match the reference level (the target processed with Farina’s method), using both RMS (Root Mean Square) and peak normalization methods. RMS normalization adjusts the overall loudness to match the reference, while peak normalization matches the maximum amplitude of the signals.

In the following example, the output from Pedalboard is approximately 31.24 dBs lower in both peak and RMS level compared to the reference target processed with Farina’s method. This significant level difference is corrected in the normalized versions shown in the table below. As can be appreciated, they sound identical and, both perceptually and when analyzed with a spectrogram, the results are indistinguishable.

| Example | Input (Dry) | Target (Wet, Farina's Partitioned) | Target (Wet, Pedalboard (low volume sample)) | Target (Wet, Pedalboard Norm Peak) | Target (Wet, Pedalboard Norm RMS) |
|---------|------------------|----------------------|---------------------|---------------------|---------------------|
| 1 | <audio src="githubpage_pedal_farina/12_input.wav" controls preload></audio> | <audio src="githubpage_pedal_farina/farina/12.wav" controls preload></audio> | <audio src="githubpage_pedal_farina/nonorm/12.wav" controls preload></audio> | <audio src="githubpage_pedal_farina/12_pedal_norm_peak.wav" controls preload></audio> | <audio src="githubpage_pedal_farina/12_pedal_norm_rms.wav" controls preload></audio> | 


### References 

- Torger, A., & Farina, A. (2001). Real-Time Partitioned Convolution for Ambiophonics Surround Sound. 
- [Chen, Y.-H., Hsiao, W.-Y., Hsieh, T.-K., Jang, J.-S. R., & Yang, Y.-H. (2022). towards automatic transcription of polyphonic electric guitar music:a new dataset and a multi-loss transformer model. ArXiv.org.](http://arxiv.org/abs/2202.09907)
- [Pedalboard: Spotify Audio Effects Library (GitHub)](https://github.com/spotify/pedalboard)
- Gated Convolutional Networks (GCN): Dauphin, Y. N., Fan, A., Auli, M., & Grangier, D. (2017). Language Modeling with Gated Convolutional Networks. Proceedings of the 34th International Conference on Machine Learning (ICML 2017).
- [Cambridge Music Technology. (n.d.). The “Mixing Secrets” Free Multitrack Download Library. Cambridge-Mt.com](https://cambridge-mt.com/ms/mtk/) 


### Contact 
Claudia Guallarte   
claudia.guallarte01@estudiant.upf.edu
