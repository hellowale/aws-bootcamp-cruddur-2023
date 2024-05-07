FROM python:3.10-slim-buster

# Inside Container
WORKDIR /backend-flask

# Outside Container--> Inside Container
COPY requirements.txt requirements.txt

# Inside Container
# Inside the python libraries used for the app
RUN pip install -r requirements.txt

# Outside Container --> Inside Container
# . means everything inside the current directory
# . (first . means everything outside the backend flask outside container)
# . (second . means everything inside the backend flask insid the container)


COPY .  .

# Set Environment Variables inside container and will remain set when the container when the container is running
ENV FLASK_APP=app.py
ENV FLASK_ENV=development

# Expose port 4567
EXPOSE 4567

# CMD (Command)
# python3 -m flask run --host --port=4567
CMD [ "python3",  "-m","flask", "run", "--host=0.0.0.0", "--port=4567"]

