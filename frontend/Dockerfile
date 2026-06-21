FROM node:20-alpine
WORKDIR /app
COPY package.json ./
RUN npm install && npm install -g serve
ARG REACT_APP_API_URL=http://localhost:3001
ENV REACT_APP_API_URL=$REACT_APP_API_URL
RUN npm run build
EXPOSE 80
CMD ["serve", "-s", "build", "-l", "80"]