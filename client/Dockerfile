FROM node:18-alpine

WORKDIR /apps

COPY package*.json ./
RUN ls -l

# Install dependencies
RUN npm install

# Copy semua kode proyek setelah dependencies terinstall
COPY . .

# Expose port 3000 untuk React
EXPOSE 3000

# Jalankan aplikasi React
CMD ["npm", "start"]

