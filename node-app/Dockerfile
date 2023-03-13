FROM node
WORKDIR /app
COPY package*.json ./
RUN npm install
RUN npm uninstall bcrypt
RUN npm install && \
  npm rebuild bcrypt --build-from-source 
COPY . .
EXPOSE 4222
ENV PORT=4222
ENV HOST=127.0.0.1

CMD ["node", "./src/server.js"]