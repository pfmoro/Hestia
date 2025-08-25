# 🌿 Héstia - Sistema de Automação de Jardim Inteligente

## 🏛️ Sobre o Projeto e a Deusa Héstia

O projeto **Héstia** é um sistema completo de automação para jardins, inspirado na deusa grega de mesmo nome. Héstia era a deusa do lar, da arquitetura e do fogo que ardia nas lareiras, simbolizando o calor e a segurança do lar. Da mesma forma, este projeto busca trazer cuidado e automação para o "lar" de suas plantas, garantindo que elas estejam sempre saudáveis e bem cuidadas.

O sistema Héstia atua em três frentes:

1.  **Sensores Ambientais e Monitoramento**: Observa o ambiente do jardim.
2.  **Controle de Irrigação**: Gerencia a distribuição de água de forma autônoma.
3.  **Sistema de Alertas Inteligentes**: Comunica o status do jardim de forma personalizada.

A arquitetura do projeto é modular e distribuída em três repositórios.

## ✨ Componentes do Sistema

O projeto é dividido em três repositórios independentes, cada um focado em uma funcionalidade específica:

### 1. Sistema de Irrigação Remota (IoT)
[cite_start]Este módulo é responsável pela irrigação automatizada do jardim[cite: 1, 2, 3, 4, 5, 6]. [cite_start]Utilizando um microcontrolador NodeMCU (ESP8266), servomotores e sensores, ele pode controlar a irrigação de duas áreas de forma independente, acionando a bomba apenas quando houver água no reservatório[cite: 1]. [cite_start]A comunicação com o microcontrolador é feita via protocolo MQTT, um protocolo leve e eficiente, ideal para projetos de IoT[cite: 1]. [cite_start]A segurança é uma prioridade, com a bomba de 110V sendo controlada por um relé e todas as conexões de alta tensão protegidas em uma caixa de passagem plástica[cite: 1].

-   **Tecnologias:** NodeMCU ESP8266, servomotores MG995, sensores de Efeito Hall, relé.
-   **Link do Repositório:** `https://github.com/pfmoro/HestiaIrrigacaoAutomatica`

### 2. Smart Garden - Alertas Inteligentes
[cite_start]Este componente é um sistema de monitoramento que usa dados de sensores de temperatura, umidade e luz para gerar alertas personalizados[cite: 7]. [cite_start]Ele se integra com modelos de linguagem (LLMs) como **Gemini** e **Ollama** para criar mensagens contextuais e envia as notificações diretamente para o WhatsApp do usuário, garantindo que suas plantas e seu bem-estar estejam sempre em foco[cite: 7, 8, 9]. [cite_start]O projeto suporta múltiplos usuários e tem um sistema de agendamento automatizado para execução regular[cite: 10, 11].

-   **Tecnologias:** Python, LLMs (Gemini, Ollama), ThingSpeak, Callmebot WhatsApp API.
-   **Link do Repositório:** `https://github.com/pfmoro/HestiaSmartGarden`

### 3. Héstia Sensores

Este repositório consolida a parte de coleta de dados ambientais, atuando como o "olho" do sistema. Ele inclui o firmware para os sensores e a lógica para enviar os dados para a API do ThingSpeak, que por sua vez, são consumidos pelo módulo de alertas inteligentes.

-   **Link do Repositório:** `https://github.com/pfmoro/Hestia_Sensores`
