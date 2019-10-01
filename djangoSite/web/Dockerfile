FROM python:3.7
ENV PYTHONUNBUFFERED 1
ENV PIPENV_VENV_IN_PROJECT 1
RUN mkdir /code
WORKDIR /code
RUN pip config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple
RUN pip install -U pip
RUN pip install pipenv
