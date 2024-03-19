FROM node:18.17.1
ENV APP_ROOT /app

RUN mkdir ${APP_ROOT}
WORKDIR ${APP_ROOT}
ADD ./app ${APP_ROOT}

# Удаляем node_modules и package-lock.json, затем устанавливаем зависимости заново
RUN rm -rf node_modules package-lock.json

RUN npm install
RUN npm run build

ENV HOST 0.0.0.0
