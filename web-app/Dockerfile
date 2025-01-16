FROM python:3.12-alpine

# Создать каталог /app и назначить его рабочей директорией
WORKDIR /app

# Скопировать содержимое текущей директории в /app
COPY . /app

# Добавить пользователя с UID 10001
RUN adduser -D -u 10001 appuser

# Назначить права пользователя на файлы
RUN chown -R appuser:appuser /app

# Переключиться на нового пользователя
USER appuser

# Указать команду для запуска Python HTTP сервера
CMD ["python", "-m", "http.server", "8000"]
