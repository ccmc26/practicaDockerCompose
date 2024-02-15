# Primera etapa: construcción
FROM node:19-alpine AS build
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .

# Segunda etapa: ejecución
FROM node:19-alpine
WORKDIR /app
COPY --from=build /app .
CMD ["npm", "start"]
