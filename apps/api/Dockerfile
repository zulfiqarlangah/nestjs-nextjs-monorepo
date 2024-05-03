FROM node:21-alpine AS base 

ARG APP 
RUN mkdir -p /app
COPY . /app
WORKDIR /app 
RUN npm install --production
RUN npm i -g @nestjs/cli
RUN npm run build 
#${APP}

#COPY --from=development /app/dist ./dist 

# Add an env to save ARG
ENV APP_MAIN_FILE=dist/apps/${APP}/main 
CMD node ${APP_MAIN_FILE}