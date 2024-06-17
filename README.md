# Mistrial Demo

### OS  
Use Linux. Preferably Ubuntu 22.04

### Pre-requistie

####
HuggingFace Token with atleast with read access is needed. 
The token value should be in the enviornment variable with the name HUGGINGFACEHUB_API_TOKEN.
```bash

sudo vim ~/.bashrc

#append at the bottom of the file
export HUGGINGFACEHUB_API_TOKEN='<Your_very_own_token>'

# save and exit vim 

source ~/.bashrc
```


#### Hardware
Nividia GPU. Script has been tested on 3080

### Running it directly from terminal window
This command do not require the python code however mistral_inference should be installed before running this command `pip install mistral_inference`
```bash
mistral-chat $HOME/mistral_models/7B-Instruct-v0.3 --instruct --max_tokens 8192
```


### Install dependecies

Virtual enviornment
```bash
sudo apt-get install python3-venv
python3 -m venv myenv
source myenv/bin/activate
```

```bash
source myenv/bin/activate
pip install -r requirements.txt #install dependecies
```


### Execute
```bash
    python .\basic.py
```


### Monitor 
Nivida latest driver should be installed before running this command
```bash
watch -n 1 nvidia-smi #GPU

watch -n 1 ps -eo pid,ppid,cmd,%mem,%cpu --sort=-%mem | head #process


```