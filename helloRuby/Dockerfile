FROM ruby:3.0.3
LABEL maintainer="okansungur@gmail.com"
RUN apt-get update -yqq && apt-get install -yqq --no-install-recommends nodejs
COPY Gemfile* /usr/src/app/
WORKDIR /usr/src/app
RUN bundle install
COPY . /usr/src/app/
CMD ["ruby","bin/rails", "s", "-b", "0.0.0.0"]
