# Flask application

## ./flask/requirements.txt
- soubor, ktery obsahuje nazvy modulu, ktere je treba doinstalovat pri buildovani docker containeru

## ./flask/Dockerfile
- obsahje zakladni konfiguraci pri buildovani docker containeru
- `ENV FLASK_APP=app.py` -> nazev root souboru, ktery se bude spoustet
- `CMD ["flask", "run"]` -> nazev prikazu, ktery se spusti pro spusteni flask serveru

## docker-compose.yml
- pod `services` je seznam containeru, ktere se budou spoustet
- pod flask containerem `web` je treba zadat do `build` umisteni slozky, ktera se bude kopirovat do containeru
