# metamind-image-identifier
Heroku Node app - Image Classification with Metamind. 

[![Deploy](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy)

##Setup

Clone or download the project and install dependencies:

```
npm install
```

Sign up for a metamind account and generate a JWT token:

http://docs.metamind.io/docs/what-you-need-to-call-api

Once you have a JWT token Set the config var:

`heroku config:set -a <appname> METAMIND_TOKEN=<your_jwt_token>`

The app will default to the General Image identification model supplied by metamind. If you create your own model you can use it by setting the config var:

`heroku config:set -a <appname> METAMIND_MODEL=<your_modelID>`

##Images
Image resizing is handled by Cloudinary. 

`heroku addons:create -a <appname> cloudinary`

Image uploading implemented with Dropzone.js



