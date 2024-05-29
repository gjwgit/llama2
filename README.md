The Python script `llm_for_IR.py` loads a pre-trained Llama 2 model (7
billions parameters, 4-bit quantised), and asks it to complete a given
prompt.

The pre-trained model is from https://huggingface.co/TheBloke/Llama-2-7B-Chat-GGUF
The script will download the model file if it does not exist on the local machine.

The script uses the
[ctransformers](https://github.com/marella/ctransformers) library to
load the pre-trained model and perform inference.

This library can be installed via `pip install ctransformers`.
