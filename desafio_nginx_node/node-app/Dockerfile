FROM node:12 AS build
WORKDIR /app
COPY package*.json .
RUN npm install
COPY . .

FROM node:12
WORKDIR /usr/src/app
COPY --from=build /app .
CMD ["node", "index"]
EXPOSE 3000