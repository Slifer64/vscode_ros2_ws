# FROM althack/ros2:humble-dev 
FROM osrf/ros:humble-desktop-full

# ** [Optional] Uncomment this section to install additional packages. **
#
ENV DEBIAN_FRONTEND=noninteractive
# RUN apt-get update \
#    && apt-get -y install --no-install-recommends <your-package-list-here> \
#    #
#    # Clean up
#    && apt-get autoremove -y \
#    && apt-get clean -y \
#    && rm -rf /var/lib/apt/lists/*

# RUN vcs import < src/ros2.repos src
# RUN sudo apt-get update && \
# 	rosdep update && \
# 	rosdep install --from-paths src --ignore-src -y

RUN sudo apt update && \
	sudo apt install ros-humble-turtlesim ~nros-humble-rqt* -y 

ENV DEBIAN_FRONTEND=dialog

# Set up auto-source of workspace for ros user
ARG WORKSPACE
RUN echo "if [ -f ${WORKSPACE}/install/setup.bash ]; then source ${WORKSPACE}/install/setup.bash; fi" >> /home/ros/.bashrc
