# 🏠 Sistema de Automação Residencial com ESP32 e IA

Projeto de automação residencial desenvolvido para a feira de ciências,
integrando **ESP32, MicroPython, Flask, SQLite, JavaScript e Inteligência Artificial**.

## 📌 Sobre o projeto

O sistema permite controlar dispositivos de uma residência por meio de uma
interface web. O usuário pode:

- 💡 Ligar e desligar luzes;
- 🚪 Abrir e fechar o portão;
- 🛗 Controlar o elevador;
- 🤖 Enviar comandos em linguagem natural para uma IA;
- 📊 Visualizar o estado dos dispositivos;
- 📝 Registrar ações no histórico.

A interface web é hospedada no GitHub Pages, enquanto um computador local
executa o servidor Flask responsável pela comunicação entre o site, o banco
de dados, a API de IA e o ESP32.

## 🧠 Como funciona

```text
                 SITE
            GitHub Pages
                 │
                 │ HTTP
                 ▼
              Ngrok
                 │
                 ▼
        ┌─────────────────┐
        │      Flask      │
        │    Backend      │
        └───────┬─────────┘
                │
       ┌────────┼─────────┐
       │        │         │
       ▼        ▼         ▼
    SQLite   OpenAI     ESP32
                         │
                ┌────────┼────────┐
                ▼        ▼        ▼
              Luzes   Portão  Elevador