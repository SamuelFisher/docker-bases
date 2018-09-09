FROM microsoft/dotnet:2.1-aspnetcore-runtime-stretch-slim

RUN apt-get update
RUN apt-get install -y libsasl2-modules libsasl2-modules-gssapi-mit krb5-user unixodbc

RUN curl -o /tmp/hive-odbc.deb https://public-repo-1.hortonworks.com/HDP/hive-odbc/2.1.16.1023/Debian/hive-odbc-native_2.1.16.1023-2_amd64.deb
RUN dpkg -i /tmp/hive-odbc.deb
RUN rm /tmp/hive-odbc.deb

ADD odbcinst.ini /etc/odbcinst.ini
