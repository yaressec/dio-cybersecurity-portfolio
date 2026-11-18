# 👋 Portfólio — DIO Cybersecurity

> Projetos práticos da formação de **Cybersecurity** da DIO. Cada repositório traz implementação, evidências reais de execução em laboratório e reflexão sobre defesa.

![Python](https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white)
![Kali Linux](https://img.shields.io/badge/Kali-Linux-557C94?logo=kalilinux&logoColor=white)
![VirtualBox](https://img.shields.io/badge/VirtualBox-7.2-183A61?logo=virtualbox&logoColor=white)
![Status](https://img.shields.io/badge/status-conclu%C3%ADdo-2ea043)

---

## 📂 Projetos

| # | Projeto | Tema | Stack | Link |
|---|---------|------|-------|------|
| 01 | **Medusa + Kali: força bruta em ambiente controlado** | Brute force FTP, DVWA e SMB, enumeração e password spraying | Medusa, Nmap, WSL Kali, Metasploitable 2 | [Ver repo](https://github.com/yaressec/dio-medusa-bruteforce-lab) |
| 02 | **Simulando malwares em Python** | Ransomware (Fernet) e keylogger (pynput/smtplib) com foco em defesa | Python, Cryptography, pynput, unittest | [Ver repo](https://github.com/yaressec/dio-malware-simulado-python) |
| 03 | **DIO Agent — especialização em AppSec** | Skill de análise de vulnerabilidades: contexto, risco e correção | Markdown, AGENTS.md, Hermes, sqlite3 | [Ver repo](https://github.com/yaressec/dio-agent-appsec) |

---

## 01️⃣ Medusa + Kali Linux — Força Bruta

🔗 **[github.com/yaressec/dio-medusa-bruteforce-lab](https://github.com/yaressec/dio-medusa-bruteforce-lab)**

**O que foi feito**
- Ambiente com Metasploitable 2 no VirtualBox e Kali via WSL.
- **FTP:** brute force com Medusa → `msfadmin:msfadmin`.
- **DVWA:** automação de formulário web com Python/urllib (com tratamento de CSRF) → `admin:password`.
- **SMB:** enumeração de 32 contas via NSE + password spraying → acesso `ADMIN$`.
- Documentação completa, wordlists, scripts, 8 evidências textuais e 4 capturas.

**Competências:** enumeração, brute force vs. password spraying, leitura de logs, análise de redes virtuais, redação técnica.

![DVWA autenticado](https://raw.githubusercontent.com/yaressec/dio-medusa-bruteforce-lab/master/images/04_dvwa_logged.png)

---

## 02️⃣ Malwares Simulados em Python

🔗 **[github.com/yaressec/dio-malware-simulado-python](https://github.com/yaressec/dio-malware-simulado-python)**

**O que foi feito**
- **Ransomware:** criptografia com Fernet, nota de resgate, backup original e descriptografia integral.
- **Keylogger:** pipeline de captura com `pynput`, modo demo com teclas sintéticas, log com permissão restrita e envio para SMTP **falso local**.
- Salvaguardas explícitas: lab isolado, nenhuma persistência, propagação ou exfiltração externa.
- Checklist de defesa (backup 3-2-1, MFA, egress filtering) + regras ilustrativas Sigma.
- 3 testes automatizados e 13 evidências reais.

**Competências:** criptografia simétrica, eventos de teclado, SMTP, testes unitários, pensamento de defesa em camadas.

![Ransomware simulado](https://raw.githubusercontent.com/yaressec/dio-malware-simulado-python/master/images/01_ransomware_encrypt.png)

---

## 03️⃣ DIO Agent — Especialização em AppSec

🔗 **[github.com/yaressec/dio-agent-appsec](https://github.com/yaressec/dio-agent-appsec)**

**O que foi feito**
- Especializei o DIO Agent com uma skill de **análise de vulnerabilidades** (SKILL.md + README), conhecimento em `agent/knowledge/security-basics.md`, trecho novo na persona e registro no `AGENTS.md`.
- O agente passou a **perguntar contexto antes de agir**, classificar vulnerabilidade/ameaça/risco e usar formato fixo com **impacto, probabilidade e severidade**.
- Validei com um `app.py` vulnerável (SQLi/CWE-89) e sua versão corrigida, com evidências dialogadas e prints.
- Melhoria extra: Regra 0 de autorização + formato padronizado para comparar casos.

**Competências:** AppSec, avaliação de risco, engenharia de prompt com arquivos, documentação técnica, ética em testes.

![Análise de vulnerabilidade](https://raw.githubusercontent.com/yaressec/dio-agent-appsec/master/images/02_analise.png)

---

## 🧠 Competências gerais demonstradas

- **Ataque & defesa:** compreensão de mecanismos ofensivos para desenhar controles preventivos e detectivos.
- **Laboratório:** montagem e troubleshooting de redes no VirtualBox/WSL (NAT, host-only, bridged).
- **Ferramentas:** Medusa, Nmap/NSE, Python (`cryptography`, `pynput`, `smtplib`, `unittest`), harness de agentes (AGENTS.md/skills).
- **Documentação:** READMEs estruturados, comandos reproduzíveis, evidências e decisões justificadas.
- **Segurança responsável:** uso exclusivo em ambientes autorizados; limites explícitos no código.

---

## 📁 Estrutura deste portfólio

```text
.
├── README.md     # visão geral e links
└── LICENSE       # MIT
```

Os projetos vivem em seus próprios repositórios para manter o histórico e as evidências organizados.

---

## ⚠️ Aviso

Todos os testes foram realizados em **ambientes isolados e autorizados** (VMs vulneráveis e WSL local). Nenhum ataque foi executado contra sistemas de terceiros.

---

<div align="center">
  <strong>Lucas Yares</strong> · <a href="https://github.com/yaressec">@yaressec</a><br>
  Feito com 🧠, ☕ e Responsible Disclosure — DIO Cybersecurity
</div>
