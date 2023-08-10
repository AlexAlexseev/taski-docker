FROM node:18
WORKDIR /app

COPY package.json package.json
COPY package-lock.json package-lock.json

RUN npm install -g npm@9.8.1
RUN npm install

COPY . .
RUN npm run build

CMD ["npx", "-y", "http-server", "-p", "8000", "/app/build"]
