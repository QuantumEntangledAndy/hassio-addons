ARG BUILD_FROM
FROM $BUILD_FROM

RUN apt-get update

RUN apt-get -y install \
  wget \
  unzip \
  libgstrtspserver-1.0-0 \
  libgstreamer1.0-0 \
  libgstreamer-plugins-bad1.0-0 \
  gstreamer1.0-x \
  gstreamer1.0-plugins-base \
  gstreamer1.0-plugins-good \
  gstreamer1.0-plugins-bad

RUN wget https://github.com/QuantumEntangledAndy/neolink/releases/latest/download/neolink_linux_arm64.zip
RUN unzip neolink_linux_arm64.zip
RUN cp neolink_linux_arm64/neolink /bin/neolink_aarch64
RUN chmod +x /bin/neolink_aarch64
RUN rm neolink_linux_arm64.zip neolink_linux_arm64/ -R

RUN wget https://github.com/QuantumEntangledAndy/neolink/releases/latest/download/neolink_linux_x86_64_ubuntu.zip
RUN unzip neolink_linux_x86_64_ubuntu.zip
RUN cp neolink_linux_x86_64_ubuntu/neolink /bin/neolink_amd64
RUN chmod +x /bin/neolink_amd64
RUN rm neolink_linux_x86_64_ubuntu.zip neolink_linux_x86_64_ubuntu/ -R

RUN wget https://github.com/QuantumEntangledAndy/neolink/releases/latest/download/neolink_linux_armhf.zip
RUN unzip neolink_linux_armhf.zip
RUN cp neolink_linux_armhf/neolink /bin/neolink_armhf
RUN chmod +x /bin/neolink_armhf
RUN rm neolink_linux_armhf.zip neolink_linux_armhf/ -R

RUN wget https://github.com/QuantumEntangledAndy/neolink/releases/latest/download/neolink_linux_i386.zip
RUN unzip neolink_linux_i386.zip
RUN cp neolink_linux_i386/neolink /bin/neolink_i386
RUN chmod +x /bin/neolink_i386
RUN rm neolink_linux_i386.zip neolink_linux_i386/ -R

# Copy data for add-on
COPY run.sh /
RUN chmod a+x /run.sh

CMD [ "/run.sh" ]
