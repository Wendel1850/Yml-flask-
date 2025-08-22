
pip install flask
from flask import Flask

app = Flask(__name__)

@app.route('/')
def index():
    return 'Olá, mundo!'

if __name__ == '__main__':
    app.run()
python app.py
@app.route('/sobre')
def sobre():
    return 'Essa é a página sobre!'

from flask import Flask, render_template

app = Flask(__name__)

@app.route('/')
def index():
    nome = 'João'
    return render_template('index.html', nome=nome)

if __name__ == '__main__':
    app.run()
