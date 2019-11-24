FROM node:8
WORKDIR /api
RUN mkdir -p /api/node /api/node/mock/acciones
RUN chmod 777 -R /api
COPY /api/node/config-generated.json /api/node
COPY /api/node/mock/acciones/*.json /api/node/mock/acciones/
RUN npm install -g apimocker --unsafe-perm=true --allow-root
EXPOSE 8000
CMD ["apimocker", "-c", "/api/node/config-generated.json", "-p", "8000"]ll