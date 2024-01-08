# Voices of ಕರುನಾಡು
## Overview

Voices of Karunadu is a unique project that harnesses artificial intelligence to replicate voices representative of the rich linguistic and cultural diversity of the Karunadu region. This initiative aims to provide a platform for synthesizing voices that capture the essence of Karunadu's various languages, dialects, and cultural nuances.

## Features

- **Regional Voice Synthesis:** Generate synthetic voices reflecting the linguistic diversity of ಕರುನಾಡು.
- **Cultural Nuances:** Capture the unique cultural elements in voice synthesis for a more authentic experience.
- **Customizable:** Adapt the voice models to specific languages, dialects, or cultural contexts within ಕರುನಾಡು.

## Getting Started

Follow these instructions to set up the project on your local machine and begin exploring the Voices of ಕರುನಾಡು.


## Changelog

- WebUI for easier conversions and downloading of voice models
- Support for cover generations from a local audio file
- Option to keep intermediate files generated. e.g. Isolated vocals/instrumentals
- Download suggested public voice models from table with search/tag filters
- Support for Pixeldrain download links for voice models
- Implement new rmvpe pitch extraction technique for faster and higher quality vocal conversions
- Volume control for AI main vocals, backup vocals and instrumentals
- Index Rate for Voice conversion
- Reverb Control for AI main vocals
- Local network sharing option for webui
- Extra RVC options - filter_radius, rms_mix_rate, protect
- Local file upload via file browser option
- Upload of locally trained RVC v2 models via WebUI
- Pitch detection method control, e.g. rmvpe/mangio-crepe
- Pitch change for vocals and instrumentals together. Same effect as changing key of song in Karaoke.
- Audio output format option: wav or mp3.


## Setup

### Install Git and Python

Follow the instructions [here](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) to install Git on your computer. Also follow this [guide](https://realpython.com/installing-python/) to install Python **VERSION 3.9** if you haven't already. Using other versions of Python may result in dependency conflicts.


### Clone Voices of ಕರುನಾಡು repository

Open a command line window and run these commands to clone this entire repository and install the additional dependencies required.

1. Clone the repository: `git clone https://github.com/KarunaduVoices/Voices-Of-Karunadu.git`
2. Change into the project directory: `cd Voices-Of-Karunadu`
3. Install dependencies: `pip install -r requirements.txt`

### Download the Huggingface model

Install the RVC beta using the following link https://huggingface.co/lj1995/VoiceConversionWebUI/tree/main
- Note:- Do not download the latest version, use the `RVC-beta.7z` for fast usage.

### Install 7-zip

1.	Download 7-Zip:
   - Visit the official 7-Zip website at https://www.7-zip.org
   - Navigate to the "Download" section.
   - Download the version suitable for your Windows architecture (32-bit or 64-bit)

2.	Run the Installer:
   - Once the download is complete, locate the installer file (usually named something like 7zXXXX.exe where XXXX is the version number).

3.	Install 7-Zip:
   - Double-click on the installer file to run it.
  	- Follow the on-screen instructions in the setup wizard.
   - You can generally leave the default options selected unless you have specific preferences.

4.	Finish Installation:
   - Complete the installation process by clicking "Install" or "Finish" when prompted.

5.	Verify Installation:
   - After installation, you can verify that 7-Zip is installed by right-clicking on a file or folder. You should see 7-Zip options in the context menu.
     
##  Installation of a Huggingface model
1. Unzip the model using 7-zip.
2. Go to the Extracted folder of the RVC model.
3. Search for the `go-web`(bat extension).
4. Double-click on the `go-web` file  and run it.
5. Wait until the system cmd links to GPU(The speed depends upon on your GPU)
6. Gradio interface with the [localhost](http://localhost:7897/) will be poped from your default browser.

![gradio](https://github.com/KarunaduVoices/Voices-Of-Karunadu/assets/154655527/fe6b18f0-cd37-49d2-a299-27817d57aa44)

### Running the Gradio via WebUI

- Open the model from the Voices of Karunadu Excel sheet.
- Unzip and transfer the `.pth` and `.index` files to the weights and logs directory. Each folder should contain one `.pth` and one `.index` file.
- Copy and paste the trained model to the extracted file `.pth` file to Weights and the `.index` file to the logs directory.


The directory structure looks something like this:
```
├── Voices of Karunadu
│   ├── Darshan
│   │   ├── DarshanV2.pth
│   │   └── added_IVF2237_Flat_nprobe_1_v2.index
│   ├── Sudeep
│   │   ├── Sudeep.pth
│   │   └── added_IVF2237_Flat_nprobe_1_v2.index
│   ├── MODELS.txt
│   └── hubert_base.pt
├── mdxnet_models
├── song_output
└── src
 ```

### Steps to Clone the voice from the Gradio via WebUI

- Click on the Model Interface.
- Select the voices from `.pth` that you want to clone from Inferencing Voice.
- Select the same index model that is Automatically detected from the index path and select from the dropdown
- Recommended +12 key for male-to-female conversion and -12 key for female-to-male conversion. If the sound range goes too far and the voice is distorted, you can 
  also adjust it to the appropriate range by yourself.
- Enter the path of the audio file to be processed (default is the correct format example)
- Select the pitch extraction algorithm ('pm': faster extraction but lower-quality speech; 'harvest': better bass but extremely slow; 'crepe': better quality but 
  GPU intensive)
- Drop the File or Click on Upload to convert the voice
- Refresh the voice list and index path when you upload new `.pth` and `.index ` files


##  How to Train the Model?
To train the models follow the steps in the Google Colab and click the link below.

<a target="_blank" href="https://colab.research.google.com/github/KarunaduVoices/Voices-Of-Karunadu/blob/main/Voices%20Of%20Karunadu.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>

## Terms of Use

The use of the converted voice for the following purposes is prohibited.

* Criticizing or attacking individuals.

* Advocating for or opposing specific political positions, religions, or ideologies.

* Publicly displaying strongly stimulating expressions without proper zoning.

* Selling of voice models and generated voice clips.

* Impersonation of the original owner of the voice with malicious intentions to harm/hurt others.

* Fraudulent purposes that lead to identity theft or fraudulent phone calls.

## Disclaimer

I am not liable for any direct, indirect, consequential, incidental, or special damages arising out of or in any way connected with the use/misuse or inability to use this software.
