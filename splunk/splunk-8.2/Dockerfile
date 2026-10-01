# ******************************************************************************
#  Dockerfile for Splunk 8.2.
#
#  Since : September, 2021
#  Author: Arnold Somogyi <arnold.somogyi@gmail.com>
#
#  Copyright (c) 2020-2026 Remal Software and Arnold Somogyi All rights reserved
# ******************************************************************************
FROM splunk/splunk:8.2
LABEL authors="Arnold Somogyi <arnold.somogyi@gmail.com>"

ENV SPLUNK_HOME=/opt/splunk
COPY --chown=splunk:splunk properties/* $SPLUNK_HOME/etc/system/local/
