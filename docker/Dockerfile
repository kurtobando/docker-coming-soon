# Use the official nginx alpine image for a smaller footprint
FROM nginx:alpine

# Remove default nginx static assets
RUN rm -rf /usr/share/nginx/html/*

# Copy static files to nginx directory
COPY app/index.html /usr/share/nginx/html/

# Copy nginx configuration from docker/configs directory
COPY docker/configs/nginx/nginx.conf /etc/nginx/conf.d/default.conf

# Expose port 80
EXPOSE 80

# Start nginx in the foreground
CMD ["nginx", "-g", "daemon off;"]
