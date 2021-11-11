FROM ruby:2.3.3
RUN apt-get -y update -qq && apt-get install -y build-essential libpq-dev node.js
RUN mkdir /myapp
WORKDIR /myapp
COPY Gemfile /myapp/Gemfile
COPY Gemfile.lock /myapp/Gemfile.lock
RUN bundle install
COPY . /myapp
