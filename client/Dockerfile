FROM node:18-alpine AS builder
WORKDIR /app
COPY package*.json .
RUN npm install
COPY . .
RUN npm run build
FROM node:18-alpine AS production
COPY --from=builder /app/build ./build
RUN npm install -g serve
CMD ["serve","-s","build"]



#FROM node:18-alpine
#WORKDIR /apps
#COPY package*.json ./
#RUN ls -l
#RUN npm install
#COPY . .
#EXPOSE 3000
#CMD ["npm", "start"]
#
