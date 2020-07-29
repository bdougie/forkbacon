FROM alpine:latest

# hadolint ignore=DL3018
RUN apk add --no-cache jq bash git openssh-client
COPY entrypoint.sh /usr/local/bin/entrypoint.sh
RUN chmod +x /usr/local/bin/entrypoint.sh

ARG VERSION
ARG GIT_COMMIT

ENV VERSION="${VERSION}"
ENV GIT_COMMIT="${GIT_COMMIT}"

ENTRYPOINT [ "/usr/local/bin/entrypoint.sh" ]
CMD ["--help"]
