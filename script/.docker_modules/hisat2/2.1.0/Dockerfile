FROM lbmc/samtools:1.7
MAINTAINER Nicolas Fontrodona

ENV HISAT2_VERSION=2.1.0
ENV PACKAGES curl \
             zip \
             g++ \
             perl \
             python

RUN apk update && \
    apk add ${PACKAGES}

RUN curl -k -L http://ccb.jhu.edu/software/hisat2/dl/hisat2-${HISAT2_VERSION}-source.zip -o hisat2_linux-v${HISAT2_VERSION}.zip && \
unzip hisat2_linux-v${HISAT2_VERSION}.zip && \
cd hisat2-${HISAT2_VERSION} && \
make && \
cp hisat2 /usr/bin && \
cp hisat2-* /usr/bin && \
rm -Rf hisat2-${HISAT2_VERSION}
