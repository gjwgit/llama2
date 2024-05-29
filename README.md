The Python script `chat.py` (Author Dawei Chen) loads a pre-trained
Llama 2 model (7 billions parameters, 4-bit quantised), and asks it to
complete a given prompt.

The pre-trained model is from
https://huggingface.co/TheBloke/Llama-2-7B-Chat-GGUF The script will
download the model file if it does not exist on the local machine.

The script uses the
[ctransformers](https://github.com/marella/ctransformers) library to
load the pre-trained model and perform inference.

This library can be installed via `pip install ctransformers`.

```
$ python chat.py
loading model "TheBloke/Llama-2-7b-Chat-GGUF/llama-2-7b-chat.Q4_K_M.gguf" ...
config.json: 100%|█████████████████████████████| 29.0/29.0 [00:00<00:00, 103kB/s]
Fetching 1 files: 100%|████████████████████████████| 1/1 [00:00<00:00,  1.39it/s]
llama-2-7b-chat.Q4_K_M.gguf: 100%|██████████| 4.08G/4.08G [10:40<00:00, 6.37MB/s]
Fetching 1 files: 100%|███████████████████████████| 1/1 [10:41<00:00, 641.22s/it]

Answer the question below in text using about 50 words, your answer should be in bullet points.

Question:
Is nuclear power plant eco-friendly?

Answer:
• No, nuclear power plants produce radioactive waste that can harm the environment and human health.
• The process of generating electricity through nuclear reactions also releases greenhouse gases.
• Nuclear power plants require large amounts of water for cooling, which can impact local ecosystems.
• Accidents at nuclear power plants, such as Chernobyl and Fukushima, have had severe environmental and health consequences.

Answer the question below in text using about 50 words, your answer should be in bullet points.

Question:
How to stay safe during severe weather?

Answer:
• Stay informed through local news and weather alerts
• Create a family emergency plan
• Stock up on essential supplies
• Stay indoors and away from windows
• Avoid driving during severe weather
• Keep your phone charged and have a backup power source.
```


This will become:

```
$ ml chat llama2 Is nuclear power plant eco-friendly?
```
and 

```
$ ml chat llama2 How to stay safe during severe weather?
```


