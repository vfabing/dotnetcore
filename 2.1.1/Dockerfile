FROM microsoft/dotnet:2.1.1-aspnetcore-runtime
LABEL maintainer="Azure App Services Container Images <appsvc-images@microsoft.com>"

RUN mkdir -p /defaulthome/hostingstart

COPY bin /defaulthome/hostingstart
COPY init_container.sh /bin/
COPY hostingstart.html /home/site/wwwroot/

RUN echo "root:Docker!" | chpasswd \
  && echo "cd /home" >> /etc/bash.bashrc \
  && chmod 755 /bin/init_container.sh \
  && mkdir -p /home/LogFiles/

EXPOSE 2222 8080

ENV PORT 8080
ENV WEBSITE_ROLE_INSTANCE_ID localRoleInstance
ENV WEBSITE_INSTANCE_ID localInstance
ENV PATH ${PATH}:/home/site/wwwroot
ENV ASPNETCORE_URLS=

WORKDIR /home/site/wwwroot

ENTRYPOINT ["/bin/init_container.sh"]
