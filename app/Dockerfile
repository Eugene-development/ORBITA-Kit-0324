FROM --platform=linux/amd64 node:18.17.1

WORKDIR /app
COPY . .

# Удаляем node_modules и package-lock.json, затем устанавливаем зависимости заново
RUN rm -rf node_modules package-lock.json

RUN npm install
RUN npm run build

ENV HOST 0.0.0.0

CMD [ "npm", "run", "start" ]