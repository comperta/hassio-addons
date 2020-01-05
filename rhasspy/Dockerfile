FROM synesthesiam/rhasspy-server:latest
LABEL maintainer="Michael Hansen <hansen.mike@gmail.com>"

ENV LANG C.UTF-8

# Copy script to run
COPY docker/run.sh /run.sh
wget https://gist.github.com/ScottJWalter/3ec644d2eb180d145db2b42c6ad13b53/raw/8c1f03e9f34ea6674f715297f9de08b4db9f4ebe/.asoundrc -P /root/

RUN chmod a+x /run.sh

ENV CONFIG_PATH /data/options.json

ENTRYPOINT ["/run.sh"]
