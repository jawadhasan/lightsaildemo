# escape=`

#Base Image from Microsoft
FROM mcr.microsoft.com/dotnet/core/sdk:3.1-buster AS build

#set up a directory in container
WORKDIR /scr

#copy sourceCode to /src folder on container
COPY TokenGenerator.Web/ .

#restore nuget packages -- #RUN: Used to execute a command during the build process of the docker image
RUN dotnet restore

#Build the app
RUN dotnet build

#Expose Port
EXPOSE 80

#Run the app
ENTRYPOINT [ "dotnet", "run" ]

#docker image build -t dotnettokengen .
#aws lightsail push-container-image --region eu-central-1 --service-name container-service-1 --label dotnettokengen --image dotnettokengen