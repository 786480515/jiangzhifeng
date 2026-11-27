FROM alpine:3.24
RUN sed -i 's@dl-cdn.alpinelinux.org@mirrors.ustc.edu.cn@g' /etc/apk/repositories && \
apk update && \
apk add --no-cache ca-certificates curl tar git libc6-compat libstdc++ && \
curl https://ghfast.top/https://github.com/gohugoio/hugo/releases/download/v0.160.1/hugo_extended_0.160.1_Linux-amd64.tar.gz -o /tmp/hugo.tar.gz && \
tar -zxf /tmp/hugo.tar.gz -C /usr/bin/ && \
chmod +x /usr/bin/hugo && \
rm -rf /tmp/hugo.tar.gz && \
hugo version