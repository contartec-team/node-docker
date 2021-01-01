FROM circleci/node:12

RUN sudo apt-get -y -qq update && sudo apt-get -y -qq install \
  python3 \
  python3-pip \
  python-pip \
  python-dev \
  build-essential

WORKDIR /home/circleci

RUN curl -O https://bootstrap.pypa.io/get-pip.py

RUN python get-pip.py --user

RUN python -m pip install --user --upgrade pip
RUN python -m pip install awsebcli --upgrade --user
RUN python -m pip install awscli --upgrade --user

ENV PATH=~/.local/bin:$PATH