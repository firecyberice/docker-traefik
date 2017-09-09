FROM alpine:3.6

RUN apk add --no-cache \
  ca-certificates \
&& rm -rf /var/cache/apk

COPY traefik /usr/local/bin/traefik

EXPOSE 80 443 8080
ENTRYPOINT ["traefik"]
CMD ["--help"]

# Add metadata
ARG BUILD_DATE
ARG VCS_REF
ARG VERSION
ARG VCS_URL
LABEL org.label-schema.schema-version="1.0" \
      org.label-schema.vendor="firecyberice" \
      org.label-schema.build-date=$BUILD_DATE \
      org.label-schema.vcs-ref=$VCS_REF \
      org.label-schema.vcs-url=$VCS_URL


