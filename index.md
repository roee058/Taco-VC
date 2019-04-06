## Taco-VC: A Single Speaker Tacotron based Voice Conversion with Limited Data ##

In this page you will find a short description of the Taco-VC system.
The paper can be found here - TODO

Taco-VC is a four stages architecture for high quality, non-parallel, many-to-one voice conversion

#### Voice Conversion
The purpose of voice conversion (VC) is to convert the speech of a source speaker into a given desired target speaker.
A successful conversion will preserve the linguistic and phonetic characteristics of the source audio while keeping naturalness and similarity to the target speaker.

#### Taco-VC Architecture
Phonetic Posteriorgrams (PPG) are being extracted from a phoneme recognition (PR) model to preserve the prosody of the source speech. Using a chopped Tacotron (C-Taco), we synthesize the target Mel-Spectrograms (MSPEC) directly from the PPGs. 
The synthesized MSPECs (SMSPEC) are passed through a speech enhancement network (Taco-SE), which outputs the speech enhanced SMSPECs (SE-SMSPEC). 
Finally, a Wavenet vocoder is used to generate the target audio from the SE-SMPSECs. 
We use the same acoustic features (80-band MSPECs) in our different networks. 

#### Audio Samples

##### Target - Female F1
<audio controls="controls">
<source type="audio/wav" src="samples/F1/30005_F1.wav"></source>
</audio>

<table>
  <tr><td><b>Source</b></td><td><b>Target</b></td><td><b>Taco-VC</b></td><td><b>Taco-VC-NoSe</b></td></tr>
  
  <tr>
  <td><audio controls><source src="samples/F1/30005_F1.wav"></audio></td>
  <td><audio controls><source src="samples/F1/30005_F1.wav"></audio></td>
  <td><audio controls><source src="samples/F1/30005_F1.wav"></audio></td>
  <td><audio controls><source src="samples/F1/30005_F1.wav"></audio></td>
  </tr>

</table>
