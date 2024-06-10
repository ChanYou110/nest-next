FROM mysql:8.0

# Set up Japanese locale
RUN apt-get update && apt-get install -y locales
RUN locale-gen ja_JP.UTF-8
RUN localedef -f UTF-8 -i ja_JP ja_JP

# Set Japanese locale and timezone
ENV LANG=ja_JP.UTF-8
ENV LANGUAGE=ja_JP:ja
ENV LC_ALL=ja_JP.UTF-8
ENV TZ=Asia/Tokyo

# Copy custom configuration file
COPY my.cnf /etc/mysql/my.cnf
