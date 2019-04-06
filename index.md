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
<audio controls="controls">
<source type="audio/wav" src="samples/lj/target.wav"></source>
</audio>


### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/roee058/Taco-VC/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
