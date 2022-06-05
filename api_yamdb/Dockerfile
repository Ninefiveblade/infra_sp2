FROM python:3.7-slim
RUN mkdir /app
COPY requirements.txt /app
RUN pip3 install -r /app/requirements.txt --no-cache-dir
# Скопировать содержимое директории /api_yamdb c локального компьютера
# в директорию /app
COPY . ./app
# Сделать директорию /app рабочей директорией. 
WORKDIR /app
# Выполнить запуск сервера разработки при старте контейнера.
CMD ["gunicorn", "api_yamdb.wsgi:application", "--bind", "0:8000" ] 
LABEL author="Alexeev Ivan" version=1
