FROM osrf/ros:humble-desktop

SHELL ["/bin/bash", "-c"]

RUN apt-get update && apt-get install -y nano && apt-get install tree
RUN apt install -y python3-pip
RUN apt-get install dos2unix
RUN pip3 install setuptools==58.2.0
RUN echo "source /opt/ros/humble/setup.bash" >> ~/.bashrc
RUN ["/bin/bash", "-c", "source /opt/ros/${ROS_DISTRO}/setup.bash"]

RUN git config --global user.email "leonardoacha@hotmail.com"
RUN git config --global user.name "Leonardo Acha Boiano"