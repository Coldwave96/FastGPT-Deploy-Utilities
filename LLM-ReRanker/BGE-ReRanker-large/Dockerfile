FROM pytorch/pytorch:2.0.1-cuda11.7-cudnn8-runtime

# please download the model from https://huggingface.co/BAAI/bge-reranker-base and put it in the same directory as Dockerfile
COPY ./bge-reranker-large ./bge-reranker-large

COPY api.py Dockerfile requirements.txt .

RUN python3 -m pip install -r requirements.txt

ENTRYPOINT python3 api.py