# pull python base image
FROM python:3.10-slim

# copy application files
ADD GitHubActions_to_train_test_build_and_push/titanic_model_api /titanic_model_api/

# specify working directory
WORKDIR GitHubActions_to_train_test_build_and_push/titanic_model_api

# update pip
RUN pip install --upgrade pip

RUN $PWD

# install dependencies
RUN pip install -r requirements.txt

# expose port for application
EXPOSE 8001

# start fastapi application
CMD ["python", "app/main.py"]
