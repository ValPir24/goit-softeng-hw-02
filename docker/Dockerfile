# Використовуйте офіційний образ Python як базовий
FROM python:3.12

# Встановіть pipenv
RUN pip install pipenv

# Створіть директорію для вашого проекту
WORKDIR /usr/src/app

# Копіюйте файли Pipfile та Pipfile.lock у контейнер
COPY Pipfile Pipfile.lock ./

# Встановіть залежності проекту
RUN pipenv install --deploy --ignore-pipfile

# Копіюйте ваш код проекту у контейнер
COPY . .

# Вкажіть команду для запуску вашого проекту
CMD ["pipenv", "run", "python", "your_script.py"]