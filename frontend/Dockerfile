# 1) build react frontend


FROM node:18-alpine as build
 
WORKDIR /app


COPY package*.json ./


RUN npm install
 
COPY . .


RUN npm run build
 
# 2) serve with nginx


FROM nginx:stable-alpine
 
COPY --from=build /app/dist /usr/share/nginx/html
 
# Optional: custom nginx config


# COPY nginx.conf /etc/nginx/conf.d/default.conf
 
EXPOSE 80


CMD ["nginx", "-g", "daemon off;"]
 
