# list-Downloaded-Huggingface-Models
A quick python script to list all the previously downloaded model available offline in Huggingface Cache.

from transformers.utils import logging
from pathlib import Path

# Find the cache directory
cache_dir = Path.home() / ".cache" / "huggingface" / "hub"

# List all cached models
models = [p.name for p in cache_dir.glob("models--*")]
print("Cached Models:")
for model in models:
    print(model)
