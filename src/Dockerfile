FROM alpine:3.19.0

# Install python
RUN apk add --update --no-cache python3 && ln -sf python3 /usr/bin/python

# Install busybox-suid
RUN apk add --update busybox-suid

# Create folder for the script
RUN mkdir /scripts

# Entrypoint to run the cron and get output to stdout
ENTRYPOINT ["/usr/sbin/crond", "-f", "-l", "2", "-L", "/dev/stdout"]