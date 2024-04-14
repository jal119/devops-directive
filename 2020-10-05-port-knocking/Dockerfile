FROM python:3.12.3-alpine

RUN apk add --no-cache \
  iptables \
  knock

COPY ./entrypoint.sh ./
RUN chmod +x ./entrypoint.sh

COPY knockd.conf /etc/knockd.conf

COPY ./index.html ./

CMD [ "./entrypoint.sh" ]
