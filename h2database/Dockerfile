# Base Java image
FROM openjdk:8-jre-slim

# H2 version
ARG H2_VERSION

# Port to expose
EXPOSE 8082
EXPOSE 9082

# Volume containing the H2 data
VOLUME /usr/lib/h2

# Copy
ADD h2-$H2_VERSION.jar /var/lib/h2/h2.jar

# Startup script
COPY h2.sh /var/lib/h2/
COPY receptes.mv.db /usr/lib/h2/

# Rights
RUN chmod u+x /var/lib/h2/h2.sh

# Java options
ENV JAVA_OPTIONS ""

# Additional H2 options
ENV H2_OPTIONS ""

# Entry point
ENTRYPOINT ["/var/lib/h2/h2.sh"]
