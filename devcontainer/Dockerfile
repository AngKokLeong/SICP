FROM mcr.microsoft.com/devcontainers/base:bullseye

WORKDIR /

RUN apt-get update -yq
RUN apt-get install tzdata -yq

RUN apt-get install gcc make m4 libncurses-dev texinfo -yq

RUN wget --content-disposition 'https://ftp.gnu.org/gnu/mit-scheme/stable.pkg/12.1/mit-scheme-12.1-x86-64.tar.gz' -O mit-scheme-12.1-x86-64.tar.gz
RUN tar -xzvf mit-scheme-12.1-x86-64.tar.gz

WORKDIR mit-scheme-12.1/src

RUN ./configure

RUN make 

RUN make install



