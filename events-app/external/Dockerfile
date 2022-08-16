# Use base image for NodeJS
FROM node:14-alpine

# Copy application code.
COPY . /app/

# Change the working directory
WORKDIR /app

# Install dependencies.
RUN npm install

# Start the Express app
CMD ["node", "server.js"]
docker build -t external:v1.0 .
<CTRL>+C
docker run -d -p 8080:8080 -e SERVER='http://localhost:8082' --network="host" external:v1.0