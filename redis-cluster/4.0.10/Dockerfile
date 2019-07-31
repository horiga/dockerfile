FROM redis:4.0.10-alpine

RUN apk add ruby && \
    gem install -N redis

COPY redis-trib.rb /usr/local/bin/
COPY docker-entrypoint.sh /usr/local/bin/

RUN chmod +x /usr/local/bin/docker-entrypoint.sh

ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]

EXPOSE 7000 7001 7002 7003 7004 7005

CMD ["sh"]
