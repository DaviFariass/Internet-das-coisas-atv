# 🔌 Internet das Coisas e Aplicações - FATEC Itaquera

Repositório dedicado às atividades práticas de IoT, desenvolvimento em C/C++ para microcontroladores e simulações de circuitos utilizando o **Wokwi** e **Arduino**.

---

## 📂 Estrutura das Atividades

### 📁 `atv1/` - Pisca LED Simples
* **Descrição:** Primeiro contato com a plataforma Arduino e a estrutura básica de código (`setup` e `loop`).
* **Objetivo:** Controlar o acendimento e o apagamento de um único LED utilizando portas digitais e atrasos (`delay`).
* 📸 *Evidência:* `atv1.png`

### 📁 `atv2/` - Alternador de LEDs
* **Descrição:** Evolução lógica para o controle de múltiplos pinos digitais de forma sequencial.
* **Objetivo:** Alternar o funcionamento de dois LEDs na placa em intervalos de tempo controlados.
* 📸 *Evidência:* `atv2.png`

### 📁 `atv3/` - Circuito na Protoboard
* **Descrição:** Montagem física virtual utilizando protoboard, resistores de proteção e múltiplos componentes integrados.
* **Objetivo:** Praticar o fechamento de circuitos elétricos, o uso correto do polo negativo (**GND**) e a polaridade dos LEDs.
* 📸 *Evidência:* `atv3.png`

---

## 🚦 Projeto Bônus: Semáforo Inteligente
Como complemento prático, desenvolvemos um semáforo completo de trânsito utilizando **3 LEDs (Vermelho, Amarelo e Verde)** sincronizados por lógica de estados.

```cpp
void setup() {
  pinMode(13, OUTPUT); // Vermelho
  pinMode(12, OUTPUT); // Amarelo
  pinMode(11, OUTPUT); // Verde
}

void loop() {
  // Sinal Verde
  digitalWrite(11, HIGH); 
  digitalWrite(12, LOW);  
  digitalWrite(13, LOW);  
  delay(3000);            

  // Sinal Amarelo
  digitalWrite(11, LOW);  
  digitalWrite(12, HIGH); 
  digitalWrite(13, LOW);  
  delay(1000);            

  // Sinal Vermelho
  digitalWrite(11, LOW);  
  digitalWrite(12, LOW);  
  digitalWrite(13, HIGH); 
  delay(3000);            
}
