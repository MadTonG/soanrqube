FROM sonarqube:lts-community


LABEL maintainer="Leo <slzlzxlz@gmail.com>"


# plugin-branch
ARG PLUGIN_BRANCH_NAME=sonarqube-community-branch-plugin
ARG PLUGIN_BRANCH_VERSION=1.14.0
ARG PLUGIN_BRANCH_DOWNLOAD_URL=https://github.com/mc1arke/sonarqube-community-branch-plugin/releases/download
# plugin-cxx
ARG PLUGIN_CXX_NAME=soanr-cxx-plugin
ARG PLUGIN_CXX_VERSION=2.1.0
ARG PLUGIN_CXX_PATCH=428
ARG PLUGIN_CXX_DOWNLOAD_URL=https://github.com/SonarOpenCommunity/sonar-cxx/releases/download
# plugin-zh
ARG PLUGIN_ZH_NAME=sonar-l10n-zh-plugin
ARG PLUGIN_ZH_VERSIN=9.9
ARG PLUGIN_ZH_DOWNLOAD_URL=https://github.com/xuhuisheng/sonar-l10n-zh/releases/download

ARG SONAR_EXTENSIONS_PATH=/opt/sonarqube/extensions/plugins

# https://github.com/SonarOpenCommunity/sonar-cxx/releases/download/cxx-2.1.0/soanr-cxx-plugin-2.1.0.428.jar
# https://github.com/xuhuisheng/sonar-l10n-zh/releases/download/sonar-l10n-zh-plugin-9.9/sonar-l10n-zh-plugin-9.9.jar
# https://github.com/mc1arke/sonarqube-community-branch-plugin/releases/download/1.14.0/sonarqube-community-branch-plugin-1.14.0.jar
RUN curl -o ${SONAR_EXTENSIONS_PATH}/${PLUGIN_BRANCH_NAME}-${PLUGIN_BRANCH_VERSION}.jar ${PLUGIN_BRANCH_DOWNLOAD_URL}/${PLUGIN_BRANCH_VERSION/${PLUGIN_BRANCH_NAME}-${PLUGIN_BRANCH_VERSION}.jar -L \
&& curl -o ${SONAR_EXTENSIONS_PATH}/${PLUGIN_CXX_NAME}-${PLUGIN_CXX_VERSION}.jar ${PLUGIN_CXX_DOWNLOAD_URL}/cxx-${PLUGIN_CXX_VERSION}/${PLUGIN_CXX_NAME}-${PLUGIN_CXX_VERSION}.${PLUGIN_CXX_PATCH}.jar -L \
&& curl -o ${SONAR_EXTENSIONS_PATH}/${PLUGIN_ZH_NAME}-${PLUGIN_ZH_VERSIN}.jar ${PLUGIN_ZH_DOWNLOAD_URL}/${PLUGIN_ZH_NAME}-${PLUGIN_ZH_VERSIN}/${PLUGIN_ZH_NAME}-${PLUGIN_ZH_VERSIN}.jar -L
