# 🛡️ Estudo de Caso: Teste de Invasão e Mitigação em Serviço FTP

[cite_start]Este documento detalha um exercício de **Teste de Invasão (Penetration Test)** focado na identificação e exploração de vulnerabilidades em um serviço FTP (File Transfer Protocol), utilizando o Kali Linux como sistema atacante e o Metasploitable 2 como máquina alvo vulnerável[cite: 2]. O objetivo é educacional, visando a compreensão das técnicas ofensivas e o fortalecimento das medidas de defesa.

---

## 📚 Ambiente do Estudo de Caso

| Componente | Detalhe | Função |
| :--- | :--- | :--- |
| **Sistema Operacional Atacante** | Kali Linux | Hospeda as ferramentas de varredura e força bruta. |
| **Máquina Alvo** | Metasploitable 2 | Máquina virtual notoriamente vulnerável, utilizada como alvo. |
| **Serviço Alvo** | FTP (vsftpd 2.3.4) | O serviço que foi varrido e alvo do ataque de força bruta. |

---

## 1. 🌐 Reconhecimento e Varredura (Nmap)

[cite_start]O reconhecimento é o estágio inicial onde um testador de segurança identifica *hosts* ativos e os serviços rodando neles[cite: 4]. [cite_start]O **Nmap** (Network Mapper) é a ferramenta padrão para este fim[cite: 5].

* [cite_start]**Objetivo:** Identificar se a porta **21 (FTP)** está aberta e acessível[cite: 6].
* [cite_start]**Comando Utilizado:** O comando com a flag `-sV` é usado para detecção de versão[cite: 8].

```bash
nmap -sV -p 21 192.168.56.101
