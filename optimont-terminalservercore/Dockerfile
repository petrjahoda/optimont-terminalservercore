FROM mcr.microsoft.com/dotnet/core/runtime:2.2-alpine3.9
RUN apk update && apk upgrade && apk add bash
RUN cp /usr/share/zoneinfo/Europe/Prague /etc/localtime
WORKDIR /publish
COPY /publish /publish
ENTRYPOINT dotnet optimont-terminalservercore.dll
