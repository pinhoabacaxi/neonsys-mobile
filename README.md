NeonSys Mobile

NeonSys é um app Android mobile com temática cyberpunk neon para análise básica do sistema do dispositivo.

O objetivo do projeto é criar um painel local simples, bonito e útil para visualizar informações de hardware, rede, armazenamento, recursos disponíveis e benchmarks leves diretamente no celular.

Este projeto também serve como experimento de desenvolvimento full mobile, usando GitHub, IA de coding, GitHub Actions e build de APK na nuvem.

---

Visão do produto

O NeonSys deve funcionar como um cockpit visual do aparelho Android.

A ideia é oferecer uma interface rápida para responder perguntas como:

- Qual é o modelo do aparelho?
- Qual versão do Android está rodando?
- Quanto armazenamento está disponível?
- A rede atual está funcionando?
- Quais informações básicas de hardware estão disponíveis?
- O aparelho consegue executar um benchmark leve?
- Posso exportar um relatório simples do sistema?

---

Tema visual

Estética desejada:

- cyberpunk neon;
- fundo escuro;
- bordas luminosas discretas;
- ciano, roxo e magenta como cores principais;
- verde neon para status positivo;
- vermelho/laranja para alertas;
- interface simples, sem poluição visual.

O app deve parecer uma ferramenta técnica futurista, mas continuar fácil de usar.

---

MVP

O MVP inicial deve conter:

- app Android funcional;
- navegação por abas;
- tema cyberpunk neon;
- tela Dashboard;
- tela Hardware;
- tela Rede;
- tela Armazenamento;
- tela Benchmark;
- tela Sobre;
- build debug gerado por GitHub Actions;
- APK baixável como artifact.

---

Abas planejadas

Dashboard

Resumo geral do dispositivo:

- modelo do aparelho;
- versão Android;
- status de rede;
- armazenamento usado/livre;
- status do último benchmark;
- cards de resumo.

Hardware

Informações básicas do dispositivo:

- fabricante;
- modelo;
- marca;
- versão Android;
- SDK;
- arquitetura/ABI;
- resolução da tela;
- densidade;
- memória disponível, se acessível;
- sensores disponíveis, se implementado.

Rede

Informações básicas de conexão:

- tipo de conexão;
- Wi-Fi ou dados móveis;
- IP local, quando disponível;
- status de internet;
- teste simples de conectividade;
- aviso quando alguma informação estiver bloqueada por permissão/API.

Armazenamento

Informações sobre armazenamento:

- espaço total;
- espaço livre;
- espaço usado;
- acesso seguro a diretórios permitidos;
- aviso sobre limitações do Android moderno.

Benchmark

Benchmark local leve e indicativo:

- teste curto de CPU;
- teste simples de I/O, se seguro;
- score local;
- histórico simples no futuro.

O benchmark não deve ser apresentado como medição científica. Ele é apenas uma referência local do próprio aparelho.

Sobre

Informações do projeto:

- nome;
- versão;
- objetivo;
- aviso de limitações;
- links do repositório;
- créditos.

---

Limitações conhecidas

O Android moderno limita várias informações do sistema, principalmente:

- processos em execução;
- consumo detalhado por app;
- administração real de processos;
- acesso amplo ao armazenamento;
- informações sensíveis de rede;
- temperatura e sensores específicos em alguns aparelhos.

O NeonSys deve ser honesto sobre essas limitações.

Quando uma informação não estiver disponível, o app deve exibir mensagens como:

- “Indisponível neste dispositivo”
- “Bloqueado pela versão do Android”
- “Permissão necessária”
- “Não suportado sem acesso especial”

---

Stack sugerida

- Kotlin
- Jetpack Compose
- Material 3
- Navigation Compose
- ViewModel
- StateFlow
- DataStore ou Room no futuro
- GitHub Actions para build debug
- Gradle Android Plugin

---

Fluxo de desenvolvimento full mobile

Fluxo pretendido:

1. Criar e gerenciar o repositório pelo GitHub.
2. Usar GitHub Mobile para issues, revisão e commits pequenos.
3. Usar GitHub Codespaces ou ambiente web/mobile para edição mais pesada.
4. Usar IA de coding para gerar patches incrementais.
5. Usar GitHub Actions para build do APK.
6. Baixar o APK pelo artifact do workflow.
7. Testar no celular.
8. Repetir.

---

Critérios de qualidade

O projeto deve seguir estes princípios:

- entregar pequenas versões funcionais;
- não prometer acesso que o Android não permite;
- manter UI simples e responsiva;
- validar build em cada sprint;
- gerar APK debug a cada marco;
- evitar código placeholder enganoso;
- documentar limitações reais.

---

Roadmap inicial

Sprint 1

Criar a base do app:

- projeto Android;
- tema cyberpunk neon;
- navegação por abas;
- telas vazias com cards iniciais;
- GitHub Actions para build debug.

Sprint 2

Implementar dados reais básicos:

- hardware info;
- dashboard com dados reais;
- rede básica;
- armazenamento básico;
- tela Sobre;
- primeiro APK testável.

Sprint 3

Adicionar benchmark leve e histórico local.

Sprint 4

Adicionar exportação de relatório TXT/JSON.

Sprint 5

Adicionar melhorias visuais, busca e cards avançados.

---

Status

Projeto em fase inicial.

Objetivo atual:

Gerar o primeiro APK debug funcional com navegação, tema neon e informações básicas reais do dispositivo.