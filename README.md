# AWS Light Sail Demo

Deployed a .NET Core Web API application to LightSail Container Service.    

## Article
https://hexquote.com/amazon-lightsail-virtual-cloud-server/    

## Docker Commands

`docker image build -t dotnettokengen .`    
`docker run --rm --name dotnettokengen -p 80:80 dotnettokengen`    

## aws cli (LightSail) command

`aws lightsail push-container-image --region eu-central-1 --service-name container-service-1 --label dotnettokengen --image dotnettokengen`
