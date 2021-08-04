#stazeni image z dockerhuhu (nemenit)
FROM python:3.7-alpine

#vytvoreni adresare v docker conatineru (nemenit)
WORKDIR /code

#definice env promennych, nutne pro flask (nazev .py flask aplikace)
ENV FLASK_APP=app.py
ENV FLASK_RUN_HOST=0.0.0.0

#instalace potrebnych knihoven (nemenit)
RUN apk add --no-cache gcc musl-dev linux-headers

#kopirovani souboru s dep do containeru nemenit
COPY requirements.txt requirements.txt

#instalace modulu ze seznamu z .txt souboru (nemenit)
RUN pip install -r requirements.txt

#kopirovani adresare do containeru (nemenit)
COPY . .

#command pro spusteni flask aplikace 
CMD ["flask", "run"]

