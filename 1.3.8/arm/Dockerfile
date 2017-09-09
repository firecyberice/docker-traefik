FROM arm32v6/alpine:3.6
COPY qemu-arm-static /usr/bin/

RUN apk add --no-cache \
  ca-certificates \
&& rm -rf /var/cache/apk

COPY traefik /usr/local/bin/traefik

EXPOSE 80 443 8080
ENTRYPOINT ["traefik"]
CMD ["--help"]
