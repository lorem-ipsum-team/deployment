ARG CUPID_DATABASE_VERSION
FROM postgis/postgis:${CUPID_DATABASE_VERSION}

RUN apt-get update && apt-get install -y \
    build-essential \
    git \
    postgresql-server-dev-17

RUN git clone --branch v0.8.0 https://github.com/pgvector/pgvector.git /tmp/pgvector \
    && cd /tmp/pgvector \
    && make && make install && rm -rf /tmp/pgvector
