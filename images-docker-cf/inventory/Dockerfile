FROM alpine:3.6 as alpine
RUN apk add -U --no-cache ca-certificates
#FROM scratch
COPY --from=alpine /etc/ssl/certs/ca-certificates.crt /etc/ssl/certs/
COPY inventory /
COPY inventory.conf /conf/
EXPOSE 60001
CMD /inventory /conf/inventory.conf
