# CP4-EDGE

# 🚀 Projeto FIWARE com ESP32 - Grupo Brainrotters

Este projeto faz parte da disciplina **CP4 - Edge Computing and Computer Systems**.  
O objetivo é integrar o **ESP32** com o **FIWARE** via **MQTT**, controlando um LED onboard e publicando leituras de luminosidade em tempo real.

---

## 👥 Autores

- Rafael Moraes Ribeiro dos Santos – RM: 565075  
- João Cazarini – RM: 562543  
- Guilherme Andrade Amaral – RM: 562112  
- Enrico Bagli Borges – RM: 562541  
- Matheus Antunes – RM: 561292  

---

## ⚙️ Funcionalidades

- Conexão do **ESP32** ao Wi-Fi e ao **broker MQTT**.
- Controle remoto do **LED onboard (GPIO2)** via tópicos MQTT:
  - `lamp001@on|` → Liga LED  
  - `lamp001@off|` → Desliga LED
- Publicação do estado atual do LED em:
  - `/TEF/lamp001/attrs`
- Leitura de **luminosidade** (potenciômetro no pino 34) e envio para:
  - `/TEF/lamp001/attrs/l`

---

## 🛠️ Tecnologias utilizadas

- **ESP32**
- **Arduino IDE**
- **MQTT (PubSubClient)**
- **WiFi**
- **FIWARE Orion Context Broker**

---

## 🔌 Conexões

- **LED onboard**: GPIO2 (já no ESP32)  
- **Sensor de luminosidade**: Potenciômetro → GPIO34 (entrada analógica)  

---

## 📡 Tópicos MQTT

- **Subscribe (comandos)** → `/TEF/lamp001/cmd`  
- **Publish (estado do LED)** → `/TEF/lamp001/attrs`  
- **Publish (luminosidade)** → `/TEF/lamp001/attrs/l`  

---
