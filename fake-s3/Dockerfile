FROM ruby:2.6.5-alpine

LABEL Description="FakeS3"

RUN set -ex && \
    mkdir -pv /s3_data && \
    gem install fakes3

WORKDIR /s3_data

EXPOSE 4567

ENTRYPOINT ["fakes3", "-r", "/s3_data", "-p", "4567", "--license"]