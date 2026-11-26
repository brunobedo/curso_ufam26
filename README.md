# Programação Computacional para Análise de Dados em Educação Física e Esporte

**Universidade Federal do Amazonas (UFAM)** · Seminários em Ciências do Movimento Humano
**Docente:** Prof. Dr. Bruno Luiz de Souza Bedo
**Apoio:** Prof. Dr. João Machado
**Formato:** 5 encontros de 6 horas (08:00–11:00 e 14:00–17:00) · novembro de 2026

Este repositório reúne os dados e os materiais de apoio da disciplina. A ideia é que vocês consigam, a qualquer momento, voltar aqui, baixar as bases usadas em aula e conferir as orientações do trabalho final.

---

## Sobre a disciplina

A quantidade de dados disponível na educação física e no esporte cresceu muito: monitores de frequência cardíaca, GPS, testes de campo, questionários, estatísticas de jogo. O problema raramente é falta de dado, e sim saber organizar, analisar e interpretar o que se tem em mãos.

A disciplina é uma introdução prática a esse caminho, usando **Python**. Não é preciso saber programar nem ter experiência com análise de dados. Começamos do zero (o que é uma variável, como funciona um `if`) e terminamos com cada grupo respondendo a uma pergunta de pesquisa a partir de uma base de dados própria do seu tema.

Ferramentas de inteligência artificial (ChatGPT, Claude, Gemini, Copilot etc.) fazem parte do curso. Elas ajudam bastante a escrever e entender código, mas erram, inventam e às vezes produzem análises que parecem corretas e não são. Por isso, o foco é usar essas ferramentas com senso crítico: saber pedir, saber conferir e saber quando não confiar.

### O que se espera ao final

- Escrever análises simples em Python: importar uma base, limpar, filtrar, agrupar, resumir e fazer gráficos.
- Ler e interpretar tabelas e gráficos produzidos por vocês mesmos.
- Usar IA como apoio à programação, sabendo identificar e corrigir erros.
- Enxergar onde essas ferramentas podem entrar nos próprios projetos de pesquisa ou na prática profissional.

---

## Cronograma

| Encontro | Tema | Principais conteúdos |
|---|---|---|
| **1** | Introdução à ciência de dados e fundamentos de programação | Tecnologias digitais no esporte; o que é ciência de dados; fontes de dados na área; ambiente Python e Jupyter; variáveis, tipos e operadores; `if`, `for` e `while`; funções e bibliotecas |
| **2** | Organização, manipulação e tratamento de dados | NumPy e pandas; importação de arquivos; DataFrames; seleção, filtragem e transformação; agrupamento e agregação (`groupby`); valores ausentes e inconsistências |
| **3** | Análise exploratória e visualização | Estatística descritiva; comparação entre grupos; tabelas; Matplotlib e Seaborn; como interpretar e comunicar resultados |
| **4** | Inteligência artificial aplicada à educação física e ao esporte | IA, aprendizado de máquina e IA generativa; aplicações em pesquisa e desempenho; programar com apoio de IA; revisar código gerado; vieses, reprodutibilidade e ética |
| **5** | Integração e aplicações práticas | Desenvolvimento e apresentação do trabalho final; interpretação crítica dos resultados; como continuar aprendendo depois da disciplina |

Cada encontro tem um notebook de aula (conteúdo + exemplos) e uma lista de exercícios para praticar.

---

## Estrutura do repositório

```
curso_ufam26/
├── data/
│   ├── dia1/data.csv                       # scouts do Brasileirão 2021
│   ├── dia2/data.csv                       # mesma base, usada no encontro 2
│   ├── dia3/data.csv                       # mesma base, usada no encontro 3
│   └── dia4/
│       ├── dados_educacao_fisica.csv       # perfil de saúde e atividade física
│       └── dados_educacao_fisica.xlsx      # a mesma base em Excel
└── trabalhofinal/
    ├── data/                               # uma base por grupo
    │   ├── grupo1_cardiopatas.csv
    │   ├── grupo2_lombalgia.csv
    │   ├── grupo3_educacao_fisica_escolar.csv
    │   ├── grupo4_idosos.csv
    │   └── grupo5_futebol.csv
    └── instrucoes/                         # orientações em PDF de cada grupo
        ├── grupo1_orientacoes.pdf
        ├── ...
        └── grupo5_orientacoes.pdf
```

---

## Bases de dados usadas nas aulas

### Encontros 1 a 3: futebol (Brasileirão 2021)

Arquivo: `data/diaX/data.csv` (o mesmo arquivo nas três pastas)

Cerca de 30 mil linhas, cada uma correspondendo a um atleta em uma rodada do Campeonato Brasileiro de 2021 (38 rodadas, 20 clubes, quase mil atletas). As colunas seguem a nomenclatura de scouts usada em fantasy games de futebol:

| Coluna | Significado |
|---|---|
| `slug`, `atleta_id` | Nome e identificador do atleta |
| `rodada_id` | Rodada (1 a 38) |
| `clube`, `clube_id` | Clube do atleta |
| `posicao_id` | Posição (1 = goleiro, 2 = lateral, 3 = zagueiro, 4 = meia, 5 = atacante, 6 = técnico) |
| `G`, `A` | Gols e assistências |
| `FD`, `FT` | Finalizações defendidas e finalizações na trave |
| `DS`, `FC` | Desarmes e faltas cometidas |
| `PI` | Passes incompletos |
| `PC`, `PS` | Pênaltis cometidos e pênaltis sofridos |
| `CA`, `CV` | Cartões amarelo e vermelho |
| `SG`, `DE`, `DP`, `GS` | Jogo sem sofrer gol, defesas, defesas de pênalti e gols sofridos |
| `I`, `PP`, `GC` | Impedimentos, pênaltis perdidos e gols contra |
| `opponent`, `team_goals`, `opp_goals` | Adversário e placar da partida |

É uma base boa para começar porque todo mundo entende o contexto e dá para fazer perguntas simples logo de cara: quem fez mais gols? Que time finaliza mais? Time que finaliza mais ganha mais?

### Encontro 4: saúde e atividade física

Arquivo: `data/dia4/dados_educacao_fisica.csv` (também em `.xlsx`)

3.000 participantes **fictícios** com dados sociodemográficos (idade, sexo, estado, escolaridade, renda), medidas corporais (massa, estatura, cintura), hábitos (exercício, esporte praticado, sono, tempo de tela, água, tabagismo) e indicadores de saúde (frequência cardíaca de repouso, pressão arterial, saúde percebida).

Os exercícios do encontro 4 usam essa base para trabalhar, por exemplo: perfil de atividade física, cálculo de IMC, proporção de pessoas que atingem a meta de exercício, comparação entre estados e correlação entre idade e pressão arterial.

---

## Trabalho final

O trabalho final é a **atividade prática integradora** (60% da nota). Cada grupo recebe uma base de dados sobre um tema diferente e precisa formular uma pergunta de investigação e respondê-la com os dados.

| Grupo | Tema | Base |
|---|---|---|
| 1 | Cardiopatas | `grupo1_cardiopatas.csv` |
| 2 | Lombalgia | `grupo2_lombalgia.csv` |
| 3 | Educação física escolar | `grupo3_educacao_fisica_escolar.csv` |
| 4 | Idosos | `grupo4_idosos.csv` |
| 5 | Futebol | `grupo5_futebol.csv` |

Todas as bases têm 6.000 registros e cerca de 20 variáveis. O dicionário completo de cada uma (nome da coluna, descrição e unidade) está no PDF de orientações do grupo, em `trabalhofinal/instrucoes/`.

### Como desenvolver

O PDF de cada grupo traz dez sugestões de pergunta. São pontos de partida, não uma lista a ser respondida inteira. Vocês podem escolher uma, adaptar, juntar duas ou criar outra, desde que dê para responder com as variáveis disponíveis.

O caminho sugerido tem quatro etapas:

1. **Explorar**: entender a base, as variáveis, as unidades e os grupos que existem nela.
2. **Delimitar**: definir a pergunta, justificar e listar as variáveis necessárias.
3. **Analisar**: organizar, filtrar, transformar e resumir os dados em função da pergunta.
4. **Comunicar**: apresentar os resultados em tabelas e gráficos e interpretar o que foi encontrado.

A análise pode ser só descritiva. Testes estatísticos são opcionais e só fazem sentido se forem pertinentes e se o grupo entender o que está fazendo. Código complicado não é critério de qualidade.

### O que entregar

1. **Notebook (`.ipynb`)** com todo o processo, misturando células de código e de texto. Ele precisa rodar do início ao fim sem erro e explicar as decisões tomadas, não só mostrar os comandos. Estrutura sugerida: identificação do grupo e pergunta → justificativa → importação e exploração → preparação das variáveis → análise → resultados (tabelas e gráficos) → interpretação, conclusão e limitações.
2. **Apresentação** com a pergunta, a justificativa no contexto da educação física, do esporte ou da saúde, as etapas realizadas, os principais resultados com gráficos e, no fim, a resposta à pergunta e as limitações.

### Sobre os gráficos

Escolham o gráfico pelo que querem mostrar:

- **Histograma**: distribuição de uma variável numérica.
- **Boxplot**: comparar a distribuição entre grupos.
- **Barras**: frequências ou médias por categoria.
- **Dispersão**: relação entre duas variáveis numéricas (com reta de tendência, se fizer sentido).

Todo gráfico precisa de título que diga algo, eixos nomeados com unidade e legenda quando houver mais de uma série. Ao comparar grupos, informem quantas observações há em cada um e olhem para a variabilidade, não só para a média.

### Checklist antes de entregar

- [ ] A pergunta foi de fato respondida?
- [ ] O notebook roda inteiro sem erro (`Kernel > Restart & Run All`)?
- [ ] Os números da apresentação batem com os do notebook?
- [ ] As conclusões respeitam os limites dos dados?
- [ ] Todos do grupo entendem o que foi feito?

> **Atenção:** as bases do trabalho final (e a do encontro 4) são **sintéticas**, criadas para ensino. As associações que vocês encontrarem não são evidência clínica, epidemiológica ou esportiva, e correlação observada não é relação de causa e efeito.

---

## Avaliação

| Atividade | Peso |
|---|---|
| Exercícios práticos orientados (listas e atividades feitas ao longo dos encontros) | 40% |
| Atividade prática integradora (trabalho final) | 60% |

O uso de IA é **permitido** no trabalho final, com duas condições: deixar claro onde e como ela foi usada, e conferir criticamente o que ela produziu. O conceito final segue os critérios do programa de pós-graduação.

---

## Como usar os dados

### Opção 1: Google Colab (não precisa instalar nada)

Abram um notebook em [colab.research.google.com](https://colab.research.google.com) e leiam o arquivo direto do GitHub:

```python
import pandas as pd

url = "https://raw.githubusercontent.com/brunobedo/curso_ufam26/master/data/dia1/data.csv"
df = pd.read_csv(url)
df.head()
```

Para o trabalho final, troquem o caminho. Exemplo do grupo 4:

```python
url = "https://raw.githubusercontent.com/brunobedo/curso_ufam26/master/trabalhofinal/data/grupo4_idosos.csv"
df = pd.read_csv(url)
```

### Opção 2: no computador

Instalem o [Anaconda](https://www.anaconda.com/download) (já vem com Python, Jupyter, pandas, Matplotlib e Seaborn) ou, se já tiverem Python:

```bash
pip install pandas numpy matplotlib seaborn jupyter openpyxl
```

Depois, baixem o repositório (botão verde **Code > Download ZIP**, ou `git clone https://github.com/brunobedo/curso_ufam26.git`) e leiam os arquivos pelo caminho local:

```python
df = pd.read_csv("data/dia4/dados_educacao_fisica.csv")
```

---

## Para continuar estudando

- MENEZES, N. N. C. *Introdução à Programação com Python: algoritmos e lógica de programação para iniciantes*. Novatec.
- BORGES, L. E. *Python para Desenvolvedores*. 2. ed.
- JAMES, G.; WITTEN, D.; HASTIE, T.; TIBSHIRANI, R.; TAYLOR, J. *An Introduction to Statistical Learning with Applications in Python*. Springer, 2023. Disponível gratuitamente em [statlearning.com](https://www.statlearning.com).
- Documentação do [pandas](https://pandas.pydata.org/docs/getting_started/index.html) e galeria de exemplos do [Seaborn](https://seaborn.pydata.org/examples/index.html).

---

Dúvidas sobre o conteúdo ou sobre o trabalho: falem comigo em sala ou pelos canais da turma.
