FROM node:16

RUN mkdir /project
WORKDIR /project

COPY . .

RUN npm install --location=global @angular/cli
RUN yarn add @angular-devkit/build-angular --dev
RUN yarn install
RUN ng update --allow-dirty --force
CMD ["ng", "serve", "--disableHostCheck", "true", "--host", "0.0.0.0"]
