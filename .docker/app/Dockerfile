FROM python:3.8
#package manager
RUN pip install pipenv

ENV PROJECT_DIR /var/www/html

WORKDIR ${PROJECT_DIR}

COPY ../.. .

COPY ../../Pipfile Pipfile.lock ${PROJECT_DIR}/
RUN pipenv install --system --deploy

EXPOSE 8007
CMD [ "python", "app.py" ]