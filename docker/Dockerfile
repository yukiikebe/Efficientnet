# Use the specified base image
FROM cnstark/pytorch:1.13.1-py3.9.16-cuda11.7.1-devel-ubuntu20.04

# Set the working directory
WORKDIR /app

# Update package lists and install necessary packages
RUN apt-get update && apt-get install -y --no-install-recommends \
    python3-pip \
    && rm -rf /var/lib/apt/lists/*

# Install Python packages
RUN pip install --no-cache-dir \
    torchvision \
    tqdm \
    scikit-learn \
    opencv-python-headless \
    pandas \
    matplotlib
RUN pip install tensorboard
# Optionally, you can copy your application code into the image
# COPY . /app

# Set the entry point for the container (if needed)
# CMD ["python", "your_script.py"]

