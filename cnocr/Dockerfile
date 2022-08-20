FROM centos:latest
  
COPY test_ocr.png /tmp/test_ocr.png
COPY ocr.py /tmp/ocr.py

RUN rm -rf /etc/yum.repos.d/*
RUN curl -o /etc/yum.repos.d/CentOS-Base.repo  https://mirrors.aliyun.com/repo/Centos-8.repo

RUN yum -y install python39 python39-devel python39-pip gcc mesa-libGL \
    && pip3 install cnocr -i https://mirrors.aliyun.com/pypi/simple/ --use-feature=2020-resolver \
    && python3 /tmp/ocr.py
