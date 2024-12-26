FROM python:3 as builder
RUN pip install pipenv
COPY Pipfile* /
WORKDIR /
RUN mkdir /.venv  # The presence of a .venv folder triggers pipenv to use it by default
RUN pipenv install --deploy

# FROM python:3-slim
# COPY --from=builder /.venv /.venv
# ENV PATH=/.venv/bin:$PATH  # Activate virtualenv!
# WORKDIR /myapp
# COPY src .
# CMD ["python3", "app.py"]
