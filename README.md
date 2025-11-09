# finetuning-sandbox
unstructured model finetuning tasks

# Setup

Create the venv:

```
python3 -m venv .venv
source .venv/bin/activate
pip install --upgrade -r requirements.txt
```

Install PyTorch, making sure there's a good match between the versions of PyTorch and CUDA:

```
pip install torch torchvision --index-url https://download.pytorch.org/whl/cu130
```

Check if the versions are okay (it should output `True`):

```
python -c "import torch; print(torch.cuda._is_compiled())"
```

Install main modules:

```
pip install transformers peft "datasets==4.3.0" "trl==0.19.1"
pip install --no-deps "unsloth==2025.11.2" "unsloth_zoo==2025.11.3"
pip install hf_transfer
pip install --no-deps "bitsandbytes==0.48.2"
```

Test Unsloth:

```
python test_unsloth.py
```
