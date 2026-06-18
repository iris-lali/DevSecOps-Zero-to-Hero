# First Dockerfile to run the container as root user: insecure container


# FROM node:26
# WORKDIR /app
# COPY . .
# RUN npm install
# EXPOSE 3000
# CMD ["npm", "start"]

# Second Dockerfile to run the container as non-root user: secure container


FROM node:26
WORKDIR /app

RUN groupadd -r appuser && useradd -r -g appuser appuser

COPY . .

RUN npm install

USER appuser 

EXPOSE 3000
CMD ["npm", "start"]