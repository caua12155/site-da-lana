from flask import Flask, render_template
import random

app = Flask(__name__)

frases = [
    "Você é o meu raio de sol nos dias nublados ☀️",
    "Seu sorriso é meu lugar favorito 💞",
    "Com você eu enfrento qualquer coisa 💪",
    "Você é meu sonho realizado ☁️",
    "Meu amor por você cresce mais a cada dia 🌹",
    "Estar com você é o melhor presente 🎁",
    "Você é a luz que ilumina meu caminho ✨"
]

@app.route('/')
def index():
    frase = random.choice(frases)
    return render_template('index.html', frase=frase)

if __name__ == '__main__':
    app.run(host='0.0.0.0', port=10000)
