# Triagem_e_Analise_Pratica_de_Emails_Maliciosos-
# 🎣 Laboratório Prático: Triagem e Análise de Phishing (SOC N1)

[![Security - SOC N1](https://img.shields.io/badge/SOC-N1%20Analyst-0284c7?style=for-the-badge&logo=shield)](https://github.com)
[![Tools - VirusTotal & Any.Run](https://img.shields.io/badge/Tools-VirusTotal%20%7C%20Any.Run%20%7C%20MXToolbox-0f172a?style=for-the-badge)](https://github.com)
[![Status - Complete](https://img.shields.io/badge/Status-Conclu%C3%ADdo-emerald?style=for-the-badge)](https://github.com)

---

## 📌 Visão Geral do Projeto

Este projeto documenta um laboratório prático de **Triagem, Análise Técnica de Phishing e Resposta a Incidentes**, simulando a rotina real de um **Analista de SOC N1 (Security Operations Center)**.

O objetivo foi investigar um e-mail suspeito de captura de credenciais (*Credential Harvesting*), verificar a autenticidade dos cabeçalhos técnicos, extrair artefatos maliciosos de forma segura e gerar um relatório completo com **Indicadores de Comprometimento (IOCs)** para bloqueio.

---

## 📁 Estrutura do Repositório

```text
phishing-analysis-lab/
│
├── README.md                          <-- Documentação principal
├── headers/
│   └── email_header_sample.txt        <-- Cabeçalho bruto do e-mail analisado
├── iocs/
│   └── iocs_blocklist.txt             <-- Lista de IPs, URLs e Hashes para bloqueio
└── reports/
    └── incident_report.md             <-- Relatório técnico de Resposta a Incidentes