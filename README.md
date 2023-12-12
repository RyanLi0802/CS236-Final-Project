# CS236-Final-Project
![Read Our Poster](CS_236_Poster.png)

### Setting up the environment
```
pip install -q -U --pre triton
pip install typing-extensions==4.5.0 kaleido
pip install -q diffusers[torch]==0.11.1 transformers==4.26.0 bitsandbytes==0.35.4\
decord accelerate omegaconf einops ftfy gradio imageio-ffmpeg xformers
```
Or
```
pip install -r requirements.txt
```

### Training the Model
1. Clone the git repository
2. Download custom training videos from [Frozen-in-Time](https://meru.robots.ox.ac.uk/frozen-in-time/) and save them under `main/training_videos/[your training folder name]`
3. Add a config file under `main/configs/[your config name]`, see existing configs as examples. The suggested numbers of training steps are 4800, 12000, 16000.
4. Run `cd main; accelerate launch train_cs236.py --config=[path-to-your-config]`

### Inference
Sample inference script can be found in `CS236_Main.ipynb`
