# 🚛 Peças Faltantes — Station Group 139

### DLchassis | Industrial Automation · Chassis Logistics

Aplicação digital para monitoramento de peças faltantes no processo de abastecimento logístico da linha de produção, vinculada ao **Station Group 139 — Line Feeding 1**.

A ferramenta tem como objetivo proporcionar maior visibilidade operacional sobre as ocorrências de peças faltantes, permitindo o acompanhamento em tempo real dos registros, a identificação de materiais pendentes e o reconhecimento das ocorrências pela equipe responsável.

Desenvolvida como uma solução de apoio à logística industrial, a aplicação contribui para a digitalização dos processos, melhoria da comunicação operacional e redução do tempo de resposta diante de desvios no abastecimento.

---

## 🎯 Objetivo da Aplicação

Disponibilizar uma interface digital para acompanhamento das peças faltantes identificadas no processo de Line Feeding, permitindo que a operação logística tenha acesso rápido e estruturado às informações necessárias para a tratativa das ocorrências.

A ferramenta busca contribuir para:

- Maior visibilidade das ocorrências de peças faltantes;
- Identificação rápida de materiais pendentes de abastecimento;
- Agilidade na tomada de decisão operacional;
- Redução do tempo de identificação de desvios logísticos;
- Melhoria da comunicação entre logística e operação;
- Monitoramento contínuo das ocorrências;
- Digitalização das atividades de controle logístico;
- Apoio à continuidade do fluxo produtivo.

---

## 🏭 Contexto Logístico

A Logística de Chassis desempenha um papel fundamental na garantia do abastecimento correto e contínuo das linhas de produção.

Dentro desse contexto, o processo de **Line Feeding** é responsável pelo fornecimento dos materiais necessários à execução das atividades produtivas, respeitando os requisitos de identificação, localização e disponibilidade dos componentes.

A ocorrência de peças faltantes pode gerar desvios no fluxo logístico, necessidade de tratativas operacionais e riscos à continuidade do abastecimento.

A aplicação Peças Faltantes foi desenvolvida para apoiar esse cenário, centralizando as informações das ocorrências em uma interface de fácil visualização.

### Conceitos relacionados

| Conceito | Aplicação no contexto logístico |
|---|---|
| Line Feeding | Processo de abastecimento de materiais à linha de produção. |
| Peças Faltantes | Ocorrências de materiais identificados como pendentes no processo logístico. |
| Station Group | Agrupamento de estações utilizado para delimitar o monitoramento da aplicação. |
| POP ID | Identificador do registro operacional apresentado na ferramenta. |
| Caixa | Identificação da caixa relacionada à ocorrência. |
| Endereço | Referência de localização logística do material. |
| Part Number | Código de identificação do componente. |
| Station | Identificação da estação relacionada ao registro. |
| Digitalização | Transformação do acompanhamento operacional em uma interface digital. |
| Automação | Utilização de recursos tecnológicos para atualização e sinalização de ocorrências. |

---

## ⚙️ Funcionalidades

### 1. Monitoramento de Peças Faltantes

A aplicação realiza consultas periódicas à API responsável pelo fornecimento dos registros de peças faltantes.

As informações são apresentadas em uma tabela estruturada, permitindo o acompanhamento das ocorrências vinculadas ao Station Group 139.

### 2. Atualização Automática

Os dados são atualizados automaticamente a cada 30 segundos.

Essa funcionalidade permite que a interface acompanhe continuamente as novas ocorrências disponibilizadas pela API, sem a necessidade de atualização manual constante.

Também está disponível o botão **Atualizar**, que permite realizar uma nova consulta manualmente.

### 3. Filtro por Data

A ferramenta disponibiliza um filtro de data para facilitar a consulta das ocorrências.

Funcionalidades:
- Seleção de uma data específica;
- Aplicação do filtro;
- Visualização dos registros correspondentes;
- Opção de exibir todos os registros novamente.

O recurso facilita a análise das ocorrências por período e o acompanhamento de registros específicos.

### 4. Identificação de Novas Ocorrências

A aplicação identifica novos registros recebidos após a primeira consulta.

As ocorrências ainda não reconhecidas são destacadas visualmente por meio de uma sinalização intermitente na linha correspondente.

Esse mecanismo permite chamar a atenção da equipe para novos registros que necessitam de reconhecimento operacional.

### 5. Alerta Visual

As peças faltantes pendentes de reconhecimento recebem destaque visual.

O alerta utiliza uma sinalização intermitente em vermelho, facilitando a identificação de novas ocorrências na interface.

### 6. Alerta Sonoro — Sirene

A aplicação possui um recurso de sirene para sinalização de ocorrências pendentes de reconhecimento.

O usuário pode ativar ou desativar o recurso por meio do botão de controle de som.

Quando ativada, a sirene permanece funcionando enquanto existirem ocorrências pendentes de reconhecimento.

O alerta sonoro atua como um recurso adicional de atenção operacional.

### 7. Reconhecimento de Ocorrências

Cada nova ocorrência pode ser reconhecida individualmente por meio do botão `OK`.

Após o reconhecimento:
- A ocorrência deixa de apresentar o alerta intermitente;
- A sinalização de pendência é removida;
- O registro passa a ser identificado como `Visto`;
- O reconhecimento é armazenado localmente no navegador.

O reconhecimento tem como finalidade indicar que a ocorrência foi visualizada.

**Importante:** o reconhecimento não representa confirmação de abastecimento, resolução da falta ou encerramento da tratativa logística.

### 8. Indicador de Ocorrências Pendentes

A ferramenta apresenta um contador de ocorrências que aguardam reconhecimento.

Esse indicador permite identificar rapidamente a quantidade de registros que ainda necessitam de atenção visual da equipe.

### 9. Status de Conexão com a API

A interface apresenta informações sobre o estado da consulta aos dados.

Status disponíveis:
- Consultando API;
- API conectada;
- Erro ao consultar API.

Também é exibida a data e hora da última atualização realizada com sucesso.

---

## 📊 Informações Disponibilizadas

A tabela principal apresenta as seguintes informações:

| Campo | Descrição |
|---|---|
| Data / Hora | Data e horário do registro da ocorrência. |
| POP ID | Identificador do registro operacional. |
| Caixa | Identificação da caixa relacionada à peça. |
| Endereço | Endereço logístico associado ao registro. |
| Descrição | Descrição do componente identificado como faltante. |
| Part Number | Código do componente. |
| Estação | Estação relacionada à ocorrência. |
| Ação | Recurso para reconhecimento individual da ocorrência. |

A organização dessas informações facilita a identificação e localização dos materiais relacionados às ocorrências.

---

## 🔄 Fluxo de Funcionamento

O funcionamento da aplicação segue o seguinte fluxo:

1. A aplicação é iniciada no navegador.
2. É realizada uma consulta inicial à API.
3. Os registros de peças faltantes são carregados na interface.
4. As informações são organizadas por data e horário.
5. A aplicação passa a consultar a API automaticamente a cada 30 segundos.
6. Novas ocorrências recebidas são identificadas.
7. Os registros pendentes recebem sinalização visual.
8. A sirene pode ser ativada para reforçar o alerta operacional.
9. O usuário reconhece individualmente as ocorrências por meio do botão `OK`.
10. A ferramenta continua realizando o monitoramento periódico.

**Fluxo resumido:**

API → Consulta de Dados → Identificação de Ocorrências → Alerta Visual/Sonoro → Reconhecimento Operacional → Monitoramento Contínuo

---

## 🔗 Integração de Dados

A aplicação utiliza uma API corporativa para obtenção das informações relacionadas às peças faltantes.

A integração permite que a interface apresente os registros disponibilizados pelo sistema de origem.

### Características da integração

- Método de consulta: GET;
- Atualização automática: 30 segundos;
- Formato de resposta esperado: JSON;
- Consulta direcionada ao Station Group 139;
- Atualização manual disponível;
- Tratamento de erros de conexão.

A aplicação utiliza os dados disponibilizados pela API, sem realizar alterações diretamente no sistema de origem.

---

## 🛠️ Tecnologias Utilizadas

| Tecnologia | Aplicação |
|---|---|
| HTML5 | Estrutura da interface e organização dos elementos. |
| CSS3 | Estilização visual, layout, cores e alertas intermitentes. |
| JavaScript | Lógica de funcionamento, atualização de dados, filtros e reconhecimento. |
| Fetch API | Comunicação com a API corporativa. |
| Web Audio API | Geração do alerta sonoro da sirene. |
| LocalStorage | Armazenamento local do reconhecimento das ocorrências. |
| JSON | Formato de recebimento dos dados da API. |

---

## 💡 Contribuição para a Logística

A aplicação está alinhada aos princípios de melhoria contínua, digitalização e automação dos processos logísticos.

### Benefícios esperados

**Visibilidade Operacional**
Centralização das ocorrências em uma interface única, facilitando o acompanhamento das peças faltantes.

**Agilidade na Identificação**
Sinalização visual e sonora para destacar novas ocorrências que necessitam de atenção.

**Redução do Tempo de Resposta**
Facilidade na identificação dos registros e das informações relacionadas aos materiais.

**Digitalização de Processos**
Substituição de formas manuais de acompanhamento por uma interface digital estruturada.

**Padronização**
Disponibilização de informações em um formato uniforme para acompanhamento operacional.

**Melhoria Contínua**
Possibilidade de evolução da ferramenta conforme as necessidades da operação logística.

**Apoio à Continuidade Produtiva**
Melhoria da visibilidade dos desvios de abastecimento que podem impactar o fluxo de materiais para a linha.

---

## 🚀 Evolução da Ferramenta

A aplicação faz parte da iniciativa de desenvolvimento de soluções digitais para a Logística de Chassis.

Seu desenvolvimento está alinhado a iniciativas de:

- Automação de processos logísticos;
- Digitalização do acompanhamento operacional;
- Integração de sistemas;
- Monitoramento de fluxo de materiais;
- Melhoria da eficiência do abastecimento;
- Desenvolvimento de aplicações internas;
- Transformação digital da logística industrial.

A ferramenta poderá evoluir conforme as necessidades operacionais e oportunidades identificadas pela área.

---

## 📌 Observações Técnicas

- A aplicação depende de conectividade com a API corporativa.
- O acesso à API pode depender da rede e das permissões corporativas.
- A atualização automática ocorre em intervalos de 30 segundos.
- O reconhecimento das ocorrências é armazenado localmente no navegador.
- O reconhecimento não é compartilhado automaticamente entre diferentes usuários ou dispositivos.
- A primeira consulta estabelece a referência inicial dos registros; os alertas de novas ocorrências são gerados nas consultas seguintes.
- A sirene depende da ativação pelo usuário e do suporte do navegador à Web Audio API.
- A ferramenta é destinada ao monitoramento e reconhecimento visual de ocorrências, não à confirmação da resolução da falta.

---

## 📁 Estrutura do Projeto

DLchassis/
│
├── index.html
│   └── Interface, estilos e funcionalidades
│       da aplicação Peças Faltantes
│
└── README.md
    └── Documentação do projeto

A aplicação está atualmente estruturada em um único arquivo HTML, contendo os recursos de interface, estilização e lógica JavaScript.

---

## 🏭 DLchassis

Este projeto integra o conjunto de soluções desenvolvidas para apoiar a Logística de Chassis por meio da tecnologia, automação e digitalização de processos.

**Industrial Automation · Logistics · Digitalization · Continuous Improvement**
