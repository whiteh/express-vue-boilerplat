FROM mhart/alpine-node:8

WORKDIR /var/app

# Install app dependencies
COPY package.json .
# For npm@5 or later, copy package-lock.json as well
# COPY package.json package-lock.json ./

RUN npm install
RUN npm install -g npm-watch
COPY . .

EXPOSE 3000

CMD ["npm-watch"]