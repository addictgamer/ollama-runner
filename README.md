# How to use ollama

```bash
sudo systemctl stop ollama
sudo systemctl disable ollama
```
b/c I want to run it here locally.

First, you need to start the server:
```bash
OLLAMA_HOST=0.0.0.0:11434 ./bin/ollama serve
```
To connect to this from anything-llm running in docker, use this URL: `http://host.docker.internal:11434`

Create the LLM from the model file (unfortunately, yes, it does transfer it over 😢)
```bash
./bin/ollama create thebloke-llama2-13b-gguf -f modelfiles/thebloke-llama2-13b-gguf
```

Now run the model:
```bash
./bin/ollama run thebloke-llama2-13b-gguf
```

To list all llocally-installed models:
```bash
ollama list
```
