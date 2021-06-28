FROM python:3.9

RUN pip install click==7.1.2
RUN pip install Flask==1.1.2
RUN pip install itsdangerous==1.1.0
RUN pip install Jinja2==2.11.2
RUN pip install MarkupSafe==1.1.1
RUN pip install Werkzeug==1.0.1

COPY . /app

RUN useradd -ms /bin/bash testuser && chown -R testuser /app

EXPOSE 8080

USER testuser

ENTRYPOINT python /app/app.py runserver 0.0.0.0:8080
