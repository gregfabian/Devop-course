# Use the official Ubuntu image as the base for this container
FROM ubuntu

# Update the package list in the base image
RUN apt-get update

# Install Apache2 HTTP server (use -y to auto-confirm installation prompts)
RUN apt-get -y install apache2

# Copy all files from the current directory on the host machine
# to the /var/www/html directory inside the container (Apache's default web root)
ADD . /var/www/html

# Set the container's entry point to run Apache in the foreground.
# JSON syntax ensures better signal handling and reliability.
ENTRYPOINT ["apachectl", "-D", "FOREGROUND"]

# Define an environment variable 'name' with the value 'Fortesoft'
# This can be accessed inside the container.
ENV name=Fortesoft
