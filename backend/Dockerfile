# Use an official Node.js runtime
FROM node:18-alpine
 
WORKDIR /usr/src/app
 
# Install dependencies
COPY package*.json ./
RUN npm install
 
# Copy source
COPY . .
 
# If using environment variables
# ENV MONGO_URI=<your_uri> \
#     JWT_SECRET=<your_secret> \
#     STRIPE_SECRET_KEY=<your_stripe_key>
 
EXPOSE 4000
 
# Run the Node/Express server
CMD ["node", "server.js"]
