FROM postgres:10-alpine

RUN apk add --no-cache --virtual build-deps musl-dev make gcc git && \
    git clone https://github.com/arkhipov/temporal_tables.git --depth 1 && \
    cd temporal_tables && \
    make && \
    make install && \
    cd ../ && rm -rf temporal_tables && \
    apk del build-deps musl-dev make gcc git
