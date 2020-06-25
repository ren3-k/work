FROM centos:7

RUN yum update -y && yum install -y \
  docbook-dtds \
  docbook-style-dsssl \
  docbook-style-xsl \
  gcc \
  gettext \
  git \
  jade \
  libxml2-devel \
  libxslt \
  libxslt-devel \
  make \
  readline-devel \
&& yum clean all

RUN git clone -b doc_ja_12 https://github.com/pgsql-jp/jpug-doc.git

RUN cd jpug-doc/ && ./configure --enable-nls --with-libxml --with-libxslt && make html

