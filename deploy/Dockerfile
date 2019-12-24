FROM postgres:10.11

RUN apt-get update && apt-get install -y postgresql-server-dev-10
RUN apt-get install -y gcc && apt-get install -y git && apt-get install -y make

RUN git clone https://github.com/guenthermi/postgres-word2vec.git

RUN cd /postgres-word2vec/freddy_extension && make install
COPY init.sql /docker-entrypoint-initdb.d/

