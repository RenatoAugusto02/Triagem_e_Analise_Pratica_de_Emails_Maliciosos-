# 📋 Relatório de Resposta a Incidentes (IR Report)

**ID do Incidente:** INC-2026-0091  
**Severidade:** Alta  
**Status:** Fechado / Mitigado  
**Analista Responsável:** Renato Augusto (SOC Analyst N1)  
**Data da Análise:** 26 de Julho de 2026  

---

## 1. Resumo Executivo
Em 26/07/2026, a equipe do SOC identificou uma tentativa de *phishing* via e-mail direcionada aos colaboradores da empresa. A investigação confirmou o uso de *Email Spoofing* e engenharia social com objetivo de capturar credenciais corporativas (*Credential Harvesting*).

---

## 2. Linha do Tempo
* **14:22** - Chegada da mensagem suspeita ao servidor de e-mail corporativo.
* **14:30** - Notificação do incidente e início da triagem SOC N1.
* **14:40** - Extração e análise do cabeçalho técnico (falhas em SPF/DKIM/DMARC).
* **14:50** - Análise passiva e dinâmica da URL (VirusTotal / Any.Run) confirmando a ameaça.
* **15:00** - Aplicação das regras de bloqueio perimetral e purga dos e-mails.

---

## 3. Achados Técnicos
* **Autenticação:** O servidor remetente (`198.51.100.42`) não possui autorização para disparar e-mails pelo domínio `@bancoseguro.com.br`, gerando falha no SPF.
* **Vetor de Ataque:** Redirecionamento para página falsa contendo formulário de login para roubo de senhas.

---

## 4. Plano de Ação Aplicado
- [x] Inclusão do IP `198.51.100.42` e do domínio `atualizacao-conta-segura[.]com` na lista de bloqueio do Firewall.
- [x] Remoção (purga) da mensagem de todas as caixas de e-mail corporativas.
- [x] Redefinição preventiva de credenciais de usuários impactados.
- [x] Envio de alerta de conscientização sobre engenharia social.