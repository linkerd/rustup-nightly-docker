# rustup-nightly

A base docker image for building against the latest nightly.

This image should be extended.  For example:

```Dockerfile
FROM linkerd/rustup-nightly:latest

RUN rustup update nightly && cargo install rustfmt && cargo install clippy

COPY . /app
WORKDIR /app
RUN cargo clippy
```
