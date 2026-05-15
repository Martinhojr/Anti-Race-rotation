<p align="center">
  <img src="Screenshot 2026-05-15 at 23-01-17 🏦 Banc..." alt="Dashboard Banco Seguro" width="700px">
</p>

---

# 🏦 Banco Seguro — Anti-Race Rotation System

![Python Version](https://img.shields.io/badge/python-3.12+-blue.svg)
![Platform](https://img.shields.io/badge/platform-Linux%20%7C%20macOS-lightgrey.svg)

O **Banco Seguro** é um motor de transações financeiras de alta performance focado em segurança transacional, resiliência e tratamento de concorrência em ambientes de alta carga. O sistema mitiga ativamente cenários de *Race Conditions*, garante os princípios ACID e oferece uma interface visual rica para observabilidade de métricas.

---

## 🚀 Funcionalidades Principais

* **Anti-Race Rotation (Controlo de Concorrência):** Mecanismos inspirados em *Two-Phase Locking* (2PL) para impedir a corrupção de saldos em acessos simultâneos.
* **Idempotência Activa:** Validação via `Idempotency Key` para mitigar ataques de replay ou reprocessamento acidental.
* **Circuit Breaker Integrado:** Proteção automatizada que interrompe operações se a taxa de falha interna ultrapassar os limites de segurança.
* **Deteção de Fraude em Tempo Real:** Monitorização de padrões suspeitos como fracionamento de valores (*Structuring*).
* **Write-Ahead Log (WAL):** Gravação imutável de eventos para garantir a recuperabilidade do estado do banco.
* **Dashboard Web Real-time:** Interface gráfica responsiva (Dark Mode / Cyberpunk Neon) com KPIs de vazão (TX/s), latência (ms) e logs ativos.

---

## 📂 Estrutura do Projeto

```text
bank_system/
│
├── main.py                  # Lógica central do sistema e simulações
├── run.py                   # Ponto de entrada (orquestrador de threads)
│
├── dashboard/
│   └── web_dashboard.py     # API Flask e código do Dashboard Web
│
└── logs/
    └── bank_system.log      # Ficheiros de log (gerados automaticamente)
