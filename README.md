import hashlib
import time
import random

def generate_hash():
    seed = f"{time.time()}-{random.random()}"
    return hashlib.sha256(seed.encode()).hexdigest()

if __name__ == "__main__":
    h = generate_hash()
    print("Generated SHA256 Hash:", h)
