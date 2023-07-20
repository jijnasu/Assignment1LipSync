# LipSync

### This project accurately synchronizes an audio file with a video file by matching the lip movements of the characters in the given video file with the corresponding audio file.




Prerequisites
-------------
- `Windows` 
- `Anaconda already installed and added to path`


Instructions to run the project
-------------
- Create a new clean working directory and follow the following commands on command prompt to clone the project install all the dependencies. 
- `git clone https://github.com/jijnasu/Assignment1LipSync.git`
- `cd Assignment1LipSync`
- Create Virtual Environment `conda create -n lipsync python=3.6`
- `conda activate lipsync`
- Install necessary packages using `pip install -r requirements.txt`
- `conda install pytorch-cpu==1.1.0 torchvision-cpu==0.3.0 cpuonly -c pytorch`



To get the desired output video
---------------
- Run the command `python inference.py --checkpoint_path checkpoints/wav2lip_gan.pth --face media/invdo720-1-17red.mp4 --audio media/inaud.wav --outfile results/output1-17.mp4`
- The output is `output1-17.mp4` file under `results` directory



To run model with different input video and audio
--------------
- Save your files video as `video.mp4` and audio as `audio.wav` under the directory `media`
- Run the command `python inference.py --checkpoint_path checkpoints/wav2lip_gan.pth --face media/video.mp4 --audio media/audio.wav --outfile results/output.mp4`
- The output is `output.mp4` file under `results` directory


Acknowledgments
----------
This project was made possible using the pre-trained model [Wav2Lip](https://github.com/Rudrabha/Wav2Lip). We thank the author for this wonderful model.