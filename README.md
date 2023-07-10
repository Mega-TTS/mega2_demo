
# Mega-TTS 2
# Zero-Shot Text-to-Speech with Arbitrary Length Speech Prompts

## Abstract
Zero-shot text-to-speech aims at synthesizing voices with unseen speech prompts. Previous large-scale multispeaker TTS models, such as Mega-TTS, have successfully achieved this goal with an enrolled recording within 10 seconds. However, most of them are designed to utilize only short speech prompts. The limited information in short speech prompts significantly hinders the performance of fine-grained identity imitation. In this paper, we introduce Mega-TTS 2, a generic zero-shot multispeaker TTS model that is capable of synthesizing speech for unseen speakers with arbitrary-length prompts. Specifically, we 1) design a multi-reference timbre encoder to extract timbre information from multiple reference speeches; 2) and train a prosody language model with arbitrary-length speech prompts; With these designs, our model is suitable for prompts of different lengths, which extends the upper bound of speech quality for zero-shot text-to-speech. Furthermore, we propose a phoneme-level auto-regressive duration model to introduce in-context learning capabilities to duration modeling. Experiments demonstrate that our method could not only synthesize identity-preserving speech with a short prompt of an unseen speaker but also achieve improved performance with longer speech prompts.

[*] This page is for <strong>research demonstration purposes</strong> only.

<div style="width:100%;">
<img align="center" src="figure/MegaTTS.png" style="  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 100%;"  /></div>

<div style="width:100%;height:50px;"></div>

<h2> Zero-Shot TTS Samples </h2>
<table border="0" width="100%">
  <thead>
    <tr>
      <th align="center"><strong>Text</strong></th>
      <th align="center"><strong>Speaker Prompt</strong></th>
      <th align="center"><strong>Ground Truth</strong></th>
      <th align="center"><strong>YourTTS</strong></th>
      <th align="center"><strong>VALL-E</strong></th>
      <th align="center"><strong>Mega-TTS</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td width="28%"><p>He was in deep converse with the clerk and entered the hall holding him by the arm.</p></td>
      <td width="12%" style="text-align: center;"><audio controls="" ><source src="audio_sample/zero-shot_TTS/prompt/4.wav" type="audio/wav"></audio></td>
      <td width="12%" style="text-align: center;"><audio controls="" ><source src="audio_sample/zero-shot_TTS/gt/4.wav" type="audio/wav"></audio></td>
      <td width="12%" style="text-align: center;"><audio controls="" ><source src="audio_sample/zero-shot_TTS/yourtts/4.wav" type="audio/wav"></audio></td>
      <td width="12%" style="text-align: center;"><audio controls="" ><source src="audio_sample/zero-shot_TTS/valle/4.wav" type="audio/wav"></audio></td>
      <td width="12%" style="text-align: center;"><audio controls="" ><source src="audio_sample/zero-shot_TTS/mega-tts/4.wav" type="audio/wav"></audio></td>
      <td width="12%" style="text-align: center;"><audio controls="" ><source src="audio_sample/zero-shot_TTS/mega-tts2/4.wav" type="audio/wav"></audio></td>
    </tr>
    <tr>
      <td width="28%"><p>Yea, his honourable worship is within, but he hath a godly minister or two with him, and likewise a leech.</p></td>
      <td width="12%" style="text-align: center;"><audio controls="" ><source src="audio_sample/zero-shot_TTS/prompt/1.wav" type="audio/wav"></audio></td>
      <td width="12%" style="text-align: center;"><audio controls="" ><source src="audio_sample/zero-shot_TTS/gt/1.wav" type="audio/wav"></audio></td>
      <td width="12%" style="text-align: center;"><audio controls="" ><source src="audio_sample/zero-shot_TTS/yourtts/1.wav" type="audio/wav"></audio></td>
      <td width="12%" style="text-align: center;"><audio controls="" ><source src="audio_sample/zero-shot_TTS/valle/1.wav" type="audio/wav"></audio></td>
      <td width="12%" style="text-align: center;"><audio controls="" ><source src="audio_sample/zero-shot_TTS/mega-tts/1.wav" type="audio/wav"></audio></td>
      <td width="12%" style="text-align: center;"><audio controls="" ><source src="audio_sample/zero-shot_TTS/mega-tts2/1.wav" type="audio/wav"></audio></td>
    </tr>
    <tr>
      <td width="28%"><p>Instead of shoes, the old man wore boots with turnover tops, and his blue coat had wide cuffs of gold braid.</p></td>
      <td width="12%" style="text-align: center;"><audio controls="" ><source src="audio_sample/zero-shot_TTS/prompt/2.wav" type="audio/wav"></audio></td>
      <td width="12%" style="text-align: center;"><audio controls="" ><source src="audio_sample/zero-shot_TTS/gt/2.wav" type="audio/wav"></audio></td>
      <td width="12%" style="text-align: center;"><audio controls="" ><source src="audio_sample/zero-shot_TTS/yourtts/2.wav" type="audio/wav"></audio></td>
      <td width="12%" style="text-align: center;"><audio controls="" ><source src="audio_sample/zero-shot_TTS/valle/2.wav" type="audio/wav"></audio></td>
      <td width="12%" style="text-align: center;"><audio controls="" ><source src="audio_sample/zero-shot_TTS/mega-tts/2.wav" type="audio/wav"></audio></td>
      <td width="12%" style="text-align: center;"><audio controls="" ><source src="audio_sample/zero-shot_TTS/mega-tts2/2.wav" type="audio/wav"></audio></td>
    </tr>
    <tr>
      <td width="28%"><p>The army found the people in poverty and left them in comparative wealth.</p></td>
      <td width="12%" style="text-align: center;"><audio controls="" ><source src="audio_sample/zero-shot_TTS/prompt/3.wav" type="audio/wav"></audio></td>
      <td width="12%" style="text-align: center;"><audio controls="" ><source src="audio_sample/zero-shot_TTS/gt/3.wav" type="audio/wav"></audio></td>
      <td width="12%" style="text-align: center;"><audio controls="" ><source src="audio_sample/zero-shot_TTS/yourtts/3.wav" type="audio/wav"></audio></td>
      <td width="12%" style="text-align: center;"><audio controls="" ><source src="audio_sample/zero-shot_TTS/valle/3.wav" type="audio/wav"></audio></td>
      <td width="12%" style="text-align: center;"><audio controls="" ><source src="audio_sample/zero-shot_TTS/mega-tts/3.wav" type="audio/wav"></audio></td>
      <td width="12%" style="text-align: center;"><audio controls="" ><source src="audio_sample/zero-shot_TTS/mega-tts2/3.wav" type="audio/wav"></audio></td>
    </tr>
  </tbody>
</table>