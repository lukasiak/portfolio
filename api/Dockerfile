# Use a lighter version of Node as a parent image
FROM mhart/alpine-node:8.11.4

# Set the working directory to /api
WORKDIR /api

# copy package.json into the container at /api
COPY package*.json /api/

# install dependencies
RUN npm install

# copy current dir contents into the container
COPY . /api/

# make port 80 available
EXPOSE 80

# run the app when the container starts
CMD ["npm", "start"]