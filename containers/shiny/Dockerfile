###############################################################################
#
# Licensed to the Apache Software Foundation (ASF) under one
# or more contributor license agreements.  See the NOTICE file
# distributed with this work for additional information
# regarding copyright ownership.  The ASF licenses this file
# to you under the Apache License, Version 2.0 (the
# "License"); you may not use this file except in compliance
# with the License.  You may obtain a copy of the License at
#
#   http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing,
# software distributed under the License is distributed on an
# "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
# KIND, either express or implied.  See the License for the
# specific language governing permissions and limitations
# under the License.
#
###############################################################################
FROM  rocker/shiny

ENV DEBIAN_FRONTEND="noninteractive" \
    TZ="Etc/UTC" \
    ECCODES_DIR=/opt/eccodes \
    PATH="${PATH}:/opt/eccodes/bin"

WORKDIR /tmp

# build r and r studio
# RUN apt-get install -y r-base
RUN apt-get update && \
    apt-get install -y libhiredis-dev

RUN R -e 'install.packages(c("leaflet"))' && \
    R -e 'install.packages(c("leaflet.extras"))' && \
    R -e 'install.packages(c("viridis"))' && \
    R -e 'install.packages(c("leafem"))' &&\
    R -e 'install.packages(c("jsonlite"))' && \
    R -e 'install.packages(c("htmltools"))' && \
    R -e 'install.packages(c("shinyjs"))' && \
    R -e 'install.packages(c("httr"))' && \
    R -e 'install.packages(c("redux"))' && \
    R -e 'install.packages(c("shinydashboard"))' && \
    R -e 'install.packages(c("shinyjs"))'
