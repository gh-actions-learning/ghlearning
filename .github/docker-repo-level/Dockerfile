FROM ghcr.io/actions/actions-runner:2.327.1

USER root

# Best to place files under /home/runner
COPY entrypoint.sh /home/runner/entrypoint.sh

RUN chmod +x /home/runner/entrypoint.sh

RUN curl -LO https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl \
 && chmod +x kubectl \
 && mv kubectl /usr/local/bin/

# Optional: metadata
# LABEL maintainer=""
# LABEL org.opencontainers.image.source=""

USER runner

ENTRYPOINT ["/home/runner/entrypoint.sh"]