FROM ruby:2.6.3-slim-stretch

RUN apt-get update && apt-get install -y --no-install-recommends \
  build-essential default-libmysqlclient-dev vim curl sudo gnupg gnupg1 gnupg2 apt-transport-https

# install yarn
RUN curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add - \
  && echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list \
  && sudo apt-get update && sudo apt-get install -y yarn

# install nodejs
RUN curl -sL https://deb.nodesource.com/setup_10.x | sudo -E bash - \
  && sudo apt-get install -y nodejs \
  && apt-get clean

WORKDIR /kubernetes-sample
