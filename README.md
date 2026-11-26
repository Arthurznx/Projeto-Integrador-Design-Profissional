# Projeto-Integrador-Design-Profissional

# Oxente, é Golpe?

> Investigação do mercado de TI, ética digital e prototipação de um sistema de detecção de golpes em mensagens e links.

**Projeto Integrador · Design Profissional · Turma F**
Curso Superior de Tecnologia em Análise e Desenvolvimento de Sistemas — Unipê, Centro Universitário de João Pessoa
João Pessoa – PB · Novembro de 2026

---

## Sumário

1. [Sobre o projeto](#sobre-o-projeto)
2. [O problema](#o-problema)
3. [A solução](#a-solução)
4. [Funcionalidades](#funcionalidades)
5. [Requisitos do sistema](#requisitos-do-sistema)
6. [Arquitetura](#arquitetura)
7. [Protótipo e telas](#protótipo-e-telas)
8. [Privacidade e ética (LGPD)](#privacidade-e-ética-lgpd)
9. [Testes de usabilidade e resultados](#testes-de-usabilidade-e-resultados)
10. [Metodologia: as seis etapas](#metodologia-as-seis-etapas)
11. [Equipe](#equipe)
12. [Status e limitações](#status-e-limitações)
13. [Próximos passos](#próximos-passos)
14. [Uso de Inteligência Artificial no projeto](#uso-de-inteligência-artificial-no-projeto)
15. [Referências](#referências)

---

## Sobre o projeto

O **Oxente, é Golpe?** é um aplicativo *mobile-first* pensado para que qualquer pessoa, inclusive idosos e quem tem pouca familiaridade com tecnologia, consiga verificar rapidamente se uma mensagem ou um link recebido é suspeito, e saiba o que fazer em seguida.

O nome vem de uma expressão nordestina do dia a dia, que traduz bem a reação de desconfiança diante de uma abordagem estranha. A ideia é aproximar a segurança digital do cidadão comum, sem jargões técnicos.

O projeto nasceu como Projeto Integrador da disciplina de Design Profissional e percorreu seis etapas: pesquisa de mercado, planejamento de carreira, ética em IA, investigação de um problema social, prototipação e testes de usabilidade. Esta documentação reúne o que foi produzido, com base no Relatório Técnico-Científico e na apresentação final da equipe.

**Questão norteadora:** como uma equipe multidisciplinar pode unir competências técnicas e éticas para criar uma solução simples e acessível contra golpes em mensagens e links?

## O problema

Entre março de 2025 e fevereiro de 2026, o Brasil registrou:

| Indicador | Valor |
|---|---|
| Tentativas de golpe | ~34 bilhões |
| Vítimas | 16,5 milhões |
| Perdas financeiras | R$ 21,2 bilhões |

Outros dados levantados pela equipe reforçam a gravidade do cenário:

- **76%** das vítimas relatam impacto na saúde mental.
- **41%** das pessoas não se sentem confiantes para identificar uma fraude.
- **408%** foi o crescimento dos crimes virtuais entre 2018 e 2024.
- O celular está presente em **93%** dos lares brasileiros, o que torna o smartphone o canal natural para a solução.

Os golpistas exploram gatilhos de **medo e urgência**, e os alertas disponíveis costumam ser técnicos demais ou chegar tarde demais.

### Escopo

O sistema atua contra golpes de **engenharia social** recebidos por aplicativos de mensagens e navegadores, como falso Pix, falsa central bancária, entrega pendente e links falsos.

### Por que golpes digitais?

A equipe comparou três problemas sociais em uma matriz com cinco critérios (abrangência, gravidade, urgência, viabilidade tecnológica e dados disponíveis):

| Problema avaliado | Pontuação (máx. 25) |
|---|---|
| **Golpes digitais** | **24** |
| Inclusão digital | 19 |
| Mapeamento urbano | 17 |

A escolha também considerou que mecanismos oficiais como **MED 2.0**, **Celular Seguro**, **BC Protege+** e **Registrato** podem ser integrados às orientações do aplicativo.

## A solução

O usuário cola a mensagem ou o link suspeito, informa a origem (WhatsApp, SMS, Instagram, e-mail ou outro) e recebe um veredito em linguagem simples, com a explicação dos sinais encontrados e um guia do que fazer.

Os três resultados possíveis são:

| Veredito | Significado |
|---|---|
| **É golpe!** | Alto risco: foram encontrados sinais claros de fraude. |
| **Atenção!** | Sinais parciais. **Não significa que a mensagem é segura:** confirme a fonte por um canal oficial. |
| **Sem indícios** | Nenhum sinal conhecido foi identificado. |

## Funcionalidades

- **Verificação multicanal:** análise de mensagens e links vindos de WhatsApp, SMS, redes sociais ou e-mail.
- **Veredito claro de risco** em três níveis.
- **Gatilhos explicados:** o app mostra por que o alerta foi disparado (urgência artificial, domínio não oficial, pedido de senha, falso Pix etc.).
- **Guia de Proteção rápida:** passos ordenados para não interagir, bloquear, denunciar, acionar o MED e registrar B.O.
- **Roteiro pós-clique:** orientação urgente para quem já clicou ou já pagou.
- **Base de padrões de golpes** conhecidos e a "regra de ouro" de verificação.
- **Histórico local**, salvo apenas no aparelho, com botão para limpar tudo.
- **Relato anônimo** por categoria, sem pedir nome, CPF ou telefone.
- **Uso imediato, sem cadastro**, com alto contraste e linguagem acessível.
- **Painel de indicadores anônimos** para acompanhar métricas agregadas.

## Requisitos do sistema

Foram especificados **12 requisitos funcionais (RF)** e **8 não funcionais (RNF)**. Resumo:

| Código | Tipo | Requisito | Descrição |
|---|---|---|---|
| RF01 | Funcional | Verificação multicanal | Colar ou inserir mensagem/link de WhatsApp, SMS, redes sociais ou e-mail. |
| RF02 | Funcional | Veredito claro de risco | Classificar em "É golpe", "Atenção" ou "Sem indícios". |
| RF03 | Funcional | Identificação de gatilhos | Apontar sinais como urgência artificial, domínio não oficial, pedido de senha ou falso Pix. |
| RF04 | Funcional | Guia imediato de defesa | Mostrar passos ordenados: não interagir, bloquear, denunciar, acionar MED e B.O. |
| RF05 | Funcional | Histórico local | Salvar consultas apenas no aparelho, com botão para limpar tudo. |
| RF06 | Funcional | Relato anônimo | Reportar tentativas por categoria, sem pedir dados pessoais. |
| RF07–RF08 | Funcional | Base de padrões e pós-clique | Consultar golpes comuns e acessar roteiro para quem já clicou ou pagou. |
| RF09–RF12 | Funcional | Acessibilidade, sem login e BI | Uso sem cadastro, alto contraste, painel anônimo e gestão de regras. |
| RNF01–RNF03 | Não funcional | Desempenho, mobile-first e clareza | Resposta em até 3 segundos; layout responsivo em grade sóbria. |
| RNF04–RNF08 | Não funcional | LGPD, segurança e acessibilidade | Zero coleta indevida de dados pessoais, HTTPS, sanitização de links e baixo consumo de dados. |

## Arquitetura

A solução foi projetada em quatro camadas integradas:

1. **Interface:** mobile-first (390 × 844 px), HTML5, CSS3 e JavaScript/React, prototipada no Figma.
2. **API REST:** servida via HTTPS (Node.js ou Python), contendo o motor de regras e a sanitização das entradas.
3. **Banco de dados relacional SQL** (PostgreSQL ou MySQL): padrões de golpes, domínios suspeitos e relatos anônimos.
4. **Módulo de BI e análise** (SQL e Python/Pandas): métricas agregadas, sem identificar os usuários.

```
Usuário ──► Interface (React) ──► API REST (regras + sanitização) ──► Banco SQL
                                                                         │
                                                  Módulo de BI ◄─────────┘
                                                (métricas anônimas)
```

> Os diagramas de arquitetura e de fluxo de navegação estão no Relatório (Figuras 3 e 4).

## Protótipo e telas

O protótipo navegável foi desenhado no **Figma** (com apoio do Figma AI) e passou por duas versões.

**Versão inicial (Etapa 5):** estética de matriz sóbria e grade técnica, com oito telas: 01 Comando, 02 Entrada, 03 Matriz (varredura em 5 etapas), 04 Golpe, 05 Atenção, 06 Defesa, 07 Referência e 08 Indicadores.

**Versão final (Etapa 6):** evoluída após os testes de usabilidade, com oito telas:

| # | Tela | Descrição |
|---|---|---|
| 1 | Início | Tela inicial com atalho de **Proteção rápida** em destaque. |
| 2 | Verificar conteúdo | Entrada da mensagem ou link e seleção de origem por ícones. |
| 3 | Analisando | Feedback visual durante a verificação. |
| 4 | Resultado "É Golpe!" | Alerta crítico com gatilhos explicados. |
| 5 | Resultado "Atenção!" | Alerta intermediário com orientação de verificação. |
| 6 | Guia de Proteção rápida | Passo a passo de defesa. |
| 7 | Padrões de golpes | Base de referência de golpes conhecidos. |
| 8 | Histórico de verificações | Consultas salvas localmente. |

> As imagens do protótipo estão nas Figuras 5 a 7B do Relatório. Se desejar, adicione-as a uma pasta `docs/` ou `assets/` e referencie aqui com `![Telas finais](assets/telas-finais.png)`.

## Privacidade e ética (LGPD)

Os estudos de caso da Etapa 3 foram a base de decisões de projeto concretas:

- **ANPD × Meta (2024):** suspensão cautelar do uso de dados públicos no treinamento de IA, por falta de transparência, uso de dados de menores e dificuldade de *opt-out*.
- **Amazon (2014–2017):** ferramenta de recrutamento por IA que penalizava currículos de mulheres, descontinuada pela empresa.

Dessas análises saiu uma **matriz com oito riscos éticos e suas mitigações**, alinhada à LGPD (Lei nº 13.709/2018). No produto, isso se traduziu em *privacy by design*:

| Princípio | Como o sistema o aplica |
|---|---|
| **Privacidade** | Sem cadastro e sem coleta de dados pessoais. |
| **Controle do usuário** | Histórico salvo apenas no aparelho, com botão para limpar tudo. |
| **Transparência** | O app mostra quais gatilhos dispararam cada alerta. |
| **Inclusão** | Linguagem simples, pensada para idosos e pessoas com pouca familiaridade digital. |
| **Supervisão humana** | A decisão final é sempre do usuário; o alerta "Atenção" nunca é apresentado como garantia de segurança. |

## Testes de usabilidade e resultados

Foi elaborado um plano com **6 tarefas (T01 a T06)** e **5 critérios de sucesso** (conclusão por pelo menos 5 de 6 participantes, tempo de até 2 minutos e satisfação média igual ou superior a 4,0 em 5,0).

A avaliação foi feita em cenário demonstrativo, com **6 perfis fictícios** de 22 a 63 anos (estudante, assistente administrativo, comerciante, motorista, auxiliar de serviços gerais e aposentado).

| Métrica | Resultado |
|---|---|
| Tarefas concluídas | **35 de 36** |
| Taxa de conclusão | **97,2%** |
| Conclusões sem ajuda | **77,8%** |
| Satisfação média | **4,2 / 5** |

### Melhorias aplicadas

1. Atalho de **Proteção rápida** em destaque na tela inicial.
2. Reforço no alerta **Atenção**: "Pode ser um golpe. Verifique a fonte e confirme por um canal oficial."
3. Seleção de origem com **ícones intuitivos** (WhatsApp, SMS, Instagram, E-mail, Outro).
4. **Barra inferior fixa** com rótulos explícitos: Início, Referência, Histórico e Configurações.

## Metodologia: as seis etapas

O trabalho seguiu uma abordagem aplicada, exploratória e descritiva.

| Etapa | Tema | O que foi feito |
|---|---|---|
| 1 | Mercado | 20 anúncios reais de vagas júnior (Front-end, Back-end, Dados e UX/UI, 5 de cada), coletados no LinkedIn e padronizados em 38 categorias. |
| 2 | Carreira | Autoavaliação de competências e Plano Individual de Desenvolvimento (PDI) com metas de 3, 6 e 9 meses para cada integrante. |
| 3 | Ética | Análise dos casos Meta e Amazon e matriz de 8 riscos com mitigações. |
| 4 | Problema social | Comparação de três temas em matriz de 25 pontos. |
| 5 | Protótipo | 12 RF, 8 RNF, arquitetura em camadas e 8 telas no Figma. |
| 6 | Testes | 6 tarefas com 6 perfis, melhorias e protótipo final. |

### Principais achados da pesquisa de mercado

- **12 de 20** vagas citam SQL e bancos de dados, a competência técnica mais cobrada (inclusive em vagas de Front-end e Dados).
- **16 de 20** pedem colaboração e trabalho em equipe.
- **13 de 20** citam ensino superior, cursando ou completo.

## Equipe

Os quatro perfis são complementares e cobrem o ciclo completo de um produto digital:

| Integrante | Área | Contribuição no projeto |
|---|---|---|
| **Raphael** | Back-end | Lógica interna, API e persistência no banco de dados. |
| **Arthur** | Front-end | Transformar os protótipos em interfaces responsivas e acessíveis. |
| **Luis** | Dados | Indicadores agregados e métricas de funcionamento do sistema. |
| **Guto** | UX/UI | Pesquisa com usuários, fluxos de navegação e telas. |

## Status e limitações

Este repositório documenta um **protótipo navegável e a pesquisa que o sustenta**. É importante ser transparente sobre o que o projeto ainda **não** é:

- Os testes de usabilidade foram uma **simulação exploratória com perfis fictícios**, sem recrutamento de usuários reais. Eles avaliam a **interface**, e não a precisão de um motor de detecção real.
- O motor de detecção por IA/regras **ainda não foi implementado**; os resultados exibidos no protótipo são demonstrativos.
- Os números de usabilidade, portanto, indicam a clareza do fluxo, e não a eficácia do sistema contra golpes reais.

## Próximos passos

- Desenvolver um **MVP** com a API de detecção (Python ou Node.js).
- Integrar **listas públicas de domínios maliciosos**.
- Realizar **testes com usuários reais**, incluindo idosos e a comunidade acadêmica.
- Integrar as orientações aos mecanismos oficiais (MED 2.0, Celular Seguro, BC Protege+ e Registrato).

## Uso de Inteligência Artificial no projeto

Em linha com as práticas de transparência discutidas na disciplina, a equipe registra que usou ferramentas de IA como **apoio**, sempre com supervisão e revisão crítica dos integrantes: pesquisa inicial de tópicos (depois conferida em fontes oficiais), planejamento de tarefas, revisão de coerência dos documentos e verificação dos requisitos funcionais e não funcionais. O protótipo foi desenhado no Figma com apoio do Figma AI.

## Referências

- ANPD. *Despacho Decisório nº 20/2024/PR/ANPD*. Diário Oficial da União, 02 jul. 2024.
- ANPD. *Voto nº 11/2024/DIR-MW* (suspensão cautelar do tratamento de dados pessoais para treinamento de IA da Meta). 2024.
- BANCO CENTRAL DO BRASIL. *Golpes e fraudes*. <https://www.bcb.gov.br/golpes>
- BRASIL. *Lei nº 13.709/2018 (LGPD)*.
- CERT.br. *Cartilha de Segurança para Internet – Fascículo Golpes: Evite Fraudes*. <https://cartilha.cert.br/fasciculos/>
- DASTIN, Jeffrey. *Amazon scraps a secret AI recruiting tool that showed bias against women*. Reuters/CNBC, 2018.
- WINICK, Erin. *Amazon's sexist hiring algorithm could still be better than a human*. MIT Technology Review, 2018.
- MDN Web Docs. <https://developer.mozilla.org/>

A lista completa de referências está no Relatório Técnico-Científico.

---

<sub>Projeto acadêmico desenvolvido no Unipê — Centro Universitário de João Pessoa · Análise e Desenvolvimento de Sistemas · Turma F · 2026.</sub>
