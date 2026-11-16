# Programa de GRC para um Escritório de Arquitetura

**Estudo de caso fictício · Governança, Risco e Conformidade · LGPD**

Avaliação de riscos, controles e plano de conformidade com a LGPD para uma empresa pequena que guarda dados confidenciais de clientes.

> O Estúdio Prumo é uma empresa fictícia. O cenário, os riscos, as notas e as metas foram criados para fins de estudo, a partir da rotina comum de escritórios de arquitetura.

📽️ **Apresentação completa:** [programa-grc-escritorio-arquitetura.pdf](programa-grc-escritorio-arquitetura.pdf)

---

## Sumário

1. [O cenário](#1-o-cenário)
2. [Por que GRC aqui?](#2-por-que-grc-aqui)
3. [Inventário de ativos e dados](#3-inventário-de-ativos-e-dados)
4. [Metodologia](#4-metodologia)
5. [Registro de riscos](#5-registro-de-riscos)
6. [Mapa de calor](#6-mapa-de-calor)
7. [Tratamento dos riscos](#7-tratamento-dos-riscos)
8. [Governança: políticas](#8-governança-políticas)
9. [Conformidade com a LGPD](#9-conformidade-com-a-lgpd)
10. [Plano de ação em 90 dias](#10-plano-de-ação-em-90-dias)
11. [Indicadores](#11-indicadores)
12. [Conclusão](#12-conclusão)
13. [Referências](#13-referências)

---

## 1. O cenário

**Estúdio Prumo: um escritório pequeno com dados grandes**

| | |
|---|---|
| **A empresa** | 12 pessoas, entre sócios, arquitetos e estagiários. Projetos residenciais, de interiores e laudos de avaliação. Trabalho híbrido, com freelancers em projetos maiores. |
| **Os dados** | Contratos com CPF e endereço, plantas e fotos do interior dos imóveis, laudos com valor do patrimônio e dados bancários para pagamentos. |
| **As ferramentas** | Nuvem compartilhada, e-mail, WhatsApp, AutoCAD e Revit em notebooks pessoais e da empresa. Nenhuma política formal de segurança. |

## 2. Por que GRC aqui?

Uma planta baixa mostra onde fica cada porta, cada janela e cada cômodo da casa de alguém.

Escritórios de arquitetura guardam informações que ajudam a entrar numa casa: acessos, posição de cofres e alarmes, rotina dos moradores. Mesmo uma empresa pequena precisa saber quais riscos corre e como tratá-los.

## 3. Inventário de ativos e dados

| Ativo | Dados envolvidos | Onde fica | Sensibilidade |
|---|---|---|---|
| Contratos | Nome, CPF, RG, endereço | Nuvem e arquivo em papel | 🔴 Alta |
| Projetos e plantas | Layout do imóvel, acessos, segurança | Nuvem, notebooks, WhatsApp | 🔴 Alta |
| Fotos e levantamentos | Interior do imóvel, objetos de valor | Celulares pessoais | 🔴 Alta |
| Laudos de avaliação | Valor do imóvel, dados do proprietário | Software de avaliação e PDFs | 🔴 Alta |
| Financeiro | Dados bancários de clientes e fornecedores | Planilha compartilhada | 🔴 Alta |
| Comunicação | Conversas, anexos, contatos | E-mail e WhatsApp | 🟡 Média |

**Achado principal:** os dados mais sensíveis estão espalhados em dispositivos pessoais e aplicativos de mensagem.

## 4. Metodologia

Processo inspirado na ISO/IEC 27005: **identificar, analisar, avaliar, tratar e monitorar**. Cada risco recebe uma nota de probabilidade (P) e uma de impacto (I).

| Probabilidade | Impacto | Nível = P × I |
|---|---|---|
| 1. Rara | 1. Insignificante | 1 a 5: Baixo |
| 2. Improvável | 2. Baixo | 6 a 11: Médio |
| 3. Possível | 3. Moderado | 12 a 19: Alto |
| 4. Provável | 4. Alto | 20 a 25: Crítico |
| 5. Quase certa | 5. Crítico | |

## 5. Registro de riscos

| ID | Risco | P | I | P × I | Nível |
|---|---|:-:|:-:|:-:|---|
| R3 | Phishing rouba o acesso à nuvem do escritório | 4 | 5 | 20 | 🟣 Crítico |
| R1 | Plantas enviadas por WhatsApp ou e-mail pessoal acabam vazando | 4 | 4 | 16 | 🔴 Alto |
| R2 | Notebook perdido ou roubado, sem criptografia | 3 | 4 | 12 | 🔴 Alto |
| R4 | Freelancer mantém acesso aos arquivos depois do fim do projeto | 4 | 3 | 12 | 🔴 Alto |
| R5 | Ransomware criptografa os projetos e não há backup testado | 2 | 5 | 10 | 🟡 Médio |
| R6 | Dados de clientes guardados por tempo indefinido | 5 | 2 | 10 | 🟡 Médio |
| R7 | Cliente pede acesso aos seus dados e o escritório não sabe responder | 3 | 2 | 6 | 🟡 Médio |

## 6. Mapa de calor

| Impacto ↓ / Probabilidade → | P1 | P2 | P3 | P4 | P5 |
|---|:-:|:-:|:-:|:-:|:-:|
| **I5** | | R5 | | **R3** | |
| **I4** | | | R2 | R1 | |
| **I3** | | | | R4 | |
| **I2** | | | R7 | | R6 |
| **I1** | | | | | |

| Nível | Ação |
|---|---|
| 🟣 Crítico | Tratar imediatamente |
| 🔴 Alto | Tratar em até 30 dias |
| 🟡 Médio | Tratar em até 90 dias |
| 🟢 Baixo | Aceitar e monitorar |

Quatro dos sete riscos estão nas faixas alta e crítica, e todos eles envolvem pessoas e acessos, não falhas de software.

## 7. Tratamento dos riscos

| ID | Estratégia | Controle proposto | Referência |
|---|---|---|---|
| R3 | Mitigar | MFA em todas as contas e treinamento contra phishing | ISO 27001 A.6.3, A.8.5 |
| R1 | Mitigar | Canal oficial de envio, com links que expiram. Plantas não circulam em apps pessoais | ISO 27001 A.5.14 |
| R2 | Mitigar | Criptografia de disco e bloqueio automático de tela | ISO 27001 A.8.1, A.8.24 |
| R4 | Mitigar | Roteiro de entrada e saída de freelancers e revisão mensal de acessos | ISO 27001 A.5.18 |
| R5 | Mitigar e transferir | Backup 3-2-1 testado todo mês e avaliação de seguro cibernético | ISO 27001 A.8.13 |
| R6 | Mitigar | Política de retenção: definir prazos e descartar o que não for mais necessário | LGPD arts. 15 e 16 |
| R7 | Mitigar | Canal de atendimento ao titular e roteiro de resposta | LGPD arts. 18 e 41 |

## 8. Governança: políticas

Seis documentos curtos, escritos para quem vai usar:

1. **Política de segurança:** regras básicas em linguagem simples, em até duas páginas.
2. **Uso aceitável:** o que pode e o que não pode em notebooks, celulares e WhatsApp.
3. **Aviso de privacidade:** explica ao cliente quais dados o escritório coleta e por quê.
4. **Retenção e descarte:** por quanto tempo cada tipo de documento fica guardado.
5. **Termo para freelancers:** confidencialidade, acesso mínimo e devolução dos arquivos ao fim do projeto.
6. **Resposta a incidentes:** uma página com quem avisar, o que fazer e em quanto tempo.

Para agentes de pequeno porte, a ANPD admite uma política de segurança simplificada, desde que cubra o essencial.

## 9. Conformidade com a LGPD

| Requisito | Referência | Hoje |
|---|---|---|
| Base legal definida para cada uso de dados (ex.: execução de contrato) | LGPD art. 7º | 🟡 Parcial |
| Registro das atividades de tratamento, mesmo que simplificado | LGPD art. 37; Res. CD/ANPD 2/2022 | 🔴 Ausente |
| Canal de comunicação com o titular (substitui o encarregado em empresas pequenas) | LGPD art. 41; Res. CD/ANPD 2/2022 | 🔴 Ausente |
| Contratos com quem trata dados em nome do escritório (nuvem, freelancers) | LGPD arts. 39 e 46 | 🔴 Ausente |
| Medidas de segurança proporcionais ao risco | LGPD art. 46 | 🟡 Parcial |
| Plano para comunicar incidentes à ANPD e aos titulares em até 3 dias úteis (6 para pequeno porte) | Res. CD/ANPD 15/2024 | 🔴 Ausente |

**Premissa:** o Estúdio Prumo é ME/EPP e não faz tratamento de alto risco. Por isso tem obrigações simplificadas e prazos em dobro, mas continua sujeito à LGPD.

## 10. Plano de ação em 90 dias

| Dias 1 a 30: Fechar as portas | Dias 31 a 60: Organizar a casa | Dias 61 a 90: Formalizar a conformidade |
|---|---|---|
| MFA em todas as contas | Canal oficial para envio de plantas | Registro das atividades de tratamento |
| Revisar e remover acessos antigos | Backup 3-2-1 com teste de restauração | Aviso de privacidade e canal do titular |
| Criptografar os notebooks | Termo para freelancers | Política de retenção e descarte |
| Treinamento rápido contra phishing | Política de segurança e de uso aceitável | Plano de resposta a incidentes |

## 11. Indicadores

| Meta | Indicador |
|---|---|
| **100%** | das contas com MFA ativado |
| **1 dia útil** | prazo máximo para remover o acesso de quem sai de um projeto |
| **Mensal** | teste de restauração do backup, com resultado registrado |
| **100%** | da equipe treinada contra phishing a cada semestre |
| **0** | plantas de clientes enviadas fora do canal oficial |
| **Trimestral** | revisão do registro de riscos pelos sócios |

Metas propostas para este estudo. Num escritório real, elas seriam definidas com os sócios.

## 12. Conclusão

**GRC não é só para grandes empresas.**

1. **Os maiores riscos estão nos hábitos.** WhatsApp, notebooks pessoais e acessos esquecidos pesam mais que falhas técnicas.
2. **Controles simples resolvem muito.** MFA, backup testado e revisão de acessos custam pouco e cobrem os riscos mais altos.
3. **Conformidade começa pelo inventário.** Sem saber quais dados existem e onde estão, não há como protegê-los nem cumprir a LGPD.
4. **Governança precisa caber na rotina.** Documentos curtos e práticos são seguidos. Manuais longos ficam na gaveta.

## 13. Referências

- ISO/IEC 27001:2022: requisitos e controles do Anexo A
- ISO/IEC 27005: gestão de riscos de segurança da informação
- NIST Cybersecurity Framework 2.0
- Lei nº 13.709/2018 (LGPD)
- Resolução CD/ANPD nº 2/2022: regulamento para agentes de tratamento de pequeno porte
- Resolução CD/ANPD nº 15/2024: comunicação de incidentes de segurança
- ANPD: Guia orientativo de segurança da informação para agentes de tratamento de pequeno porte

---

**Autora:** Bruna Grandes Rodrigues · Arquiteta e urbanista · Estudante de Governança, Risco e Conformidade
📧 brunagrandesr@gmail.com · Novembro de 2026
