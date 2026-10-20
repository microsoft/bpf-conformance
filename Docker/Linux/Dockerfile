# Copyright (c) Microsoft Corporation
# SPDX-License-Identifier: MIT

FROM ubuntu:26.04@sha256:c098726dd9b9733f3e885f8de0ef375206a311b0a317eadc40d347b1115fb944

# Install dependencies
RUN apt-get update && apt-get install -y \
    libboost-program-options-dev \
    libbpf-dev

# Clean up APT when done.
RUN apt-get clean && rm -rf /var/lib/apt/lists/*

WORKDIR /app

COPY . .

LABEL org.opencontainers.image.source=https://github.com/Alan-Jowett/bpf_conformance
LABEL org.opencontainers.image.description="BPF Conformance container image"
LABEL org.opencontainers.image.licenses=MIT