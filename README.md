# Posio

A multiplayer geography game using Websockets.

Visit [https://posio.abrenaut.com/](https://posio.abrenaut.com/) for a live demo.

![Screenshot](screenshot.png)

## 🐳 Example 1 - Docker

### Docker Run

````
docker run --rm -p 5000:5000 -e FLASK_APP=/app/posio/game_master.py -e POSIO_SETTINGS=/app/posio/config.py --name posio l4rm4nd/posio:latest
````
The web application will be available at [http://127.0.0.1:5000](http://127.0.0.1:5000).

### Docker Compose

````
# download compose file and adjust to your needs
wget https://raw.githubusercontent.com/l4rm4nd/posio/master/docker-compose.yml

# spawn the stack
docker compose up -d
````
The web application will be available at [http://127.0.0.1:5000](http://127.0.0.1:5000).

## 🐍 Example 2 - Native Python


```
# download github repo
git clone https://github.com/l4rm4nd/posio && cd posio

# create virtualenv
python -m venv .venv
source .venv/bin/activate

# install dependencies
pip install -r requirements.txt

# export envs
export FLASK_APP=$(pwd)/posio/game_master.py
export POSIO_SETTINGS=$(pwd)/posio/config.py

# run the app on localhost
flask run --host 127.0.0.1
```
The web application will be available at [http://127.0.0.1:5000](http://127.0.0.1:5000).

## License

This project is under [MIT license](LICENSE).
