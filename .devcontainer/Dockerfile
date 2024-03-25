FROM public.ecr.aws/amazonlinux/amazonlinux:2023

#
# Dependencies for devcontainer support
#
RUN yum groupinstall -y "Development Tools"

#
# Dependencies for building canvas
#
RUN yum install -y gcc-c++ cairo-devel pango-devel libjpeg-turbo-devel giflib-devel librsvg2-devel pango-devel bzip2-devel jq python3

#
# NVM
#
ENV NVM_DIR /nvm
RUN touch ~/.bashrc && mkdir -p $NVM_DIR
RUN curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash

#
# Dependencies for layer unit tests
#
RUN yum install -y dejavu-sans-fonts \
  && mv /usr/share/fonts/dejavu-sans-fonts /usr/share/fonts/dejavu
