# 📊 Nugap Analytics Dashboard

Dashboard executivo interativo desenvolvido a partir de dados exportados do **Google Analytics 4 (GA4)** para o site [nugap.com.br](https://nugap.com.br/), laboratório de análise de alimentos com foco em água e café.

---

## 🗂️ Visão geral do projeto

Este projeto transforma cinco arquivos CSV exportados do GA4 em um dashboard HTML estático completo, com múltiplas abas temáticas, gráficos interativos, leituras executivas e hipóteses de negócio priorizadas para o gestor do site.

**Período analisado:** 23 de março de 2026 a 19 de abril de 2026 (28 dias)

---

## 🎯 Objetivos

- Interpretar os dados brutos do GA4 de forma executiva e orientada a decisão
- Identificar problemas de negócio a partir do comportamento do site
- Criar um artefato visual pronto para uso em reuniões com gestores
- Entregar o dashboard como arquivo HTML estático, sem dependência de servidor

---

## 📁 Fontes de dados

| Arquivo | Conteúdo |
|---|---|
| `Aquisicao_de_usuarios_...csv` | Canais de primeiro contato do usuário, tempo de engajamento, sessões por canal |
| `Aquisicao_de_trafego_...csv` | Canais da sessão, taxa de engajamento, eventos por sessão |
| `Publicos-alvo_...csv` | Público "All Users" com dados de sessão, duração e cidades |
| `Visao_geral_da_geracao_de_leads.csv` | Novos usuários, recorrentes, leads qualificados e convertidos por dia |
| `Resumo_dos_relatorios.csv` | Páginas mais acessadas, taxas de rejeição, origens e coorte de retenção |

---

## 🧩 Estrutura do dashboard

O HTML final é composto por **cinco abas navegáveis** via sidebar lateral:

### 1. Visão geral
- KPIs principais: usuários ativos, sessões, eventos, engajamento médio
- Gráfico de linha com evolução diária de novos usuários
- Distribuição de canais (doughnut chart)
- Engajamento médio por canal (bar chart)
- Painel de leitura executiva com alertas prioritários

### 2. Aquisição
- Tabela detalhada de canais com diagnóstico qualitativo
- Tabela de origem / mídia da sessão
- Gráfico de eficiência comparativa entre canais (taxa de engajamento e eventos/sessão)
- Recomendações diretas ao gestor

### 3. Conteúdo
- Ranking de páginas por visualizações
- Taxa de rejeição por página
- Tabela com diagnóstico por URL
- Identificação de oportunidades de SEO e UX

### 4. Audiência
- KPIs de profundidade de relacionamento
- Ranking das principais cidades
- Gráfico de coorte de retenção semanal
- Análise de comportamento da base

### 5. Problemas de negócio
- 6 perguntas estratégicas estruturadas para o gestor
- Prioridades divididas em **Alta**, **Média** e **Estratégica**

---

## 🔍 Principais achados

1. **Funil de leads não mensurado** — leads qualificados e convertidos aparecem zerados em todo o período, indicando falha de instrumentação no GA4
2. **Baixa retenção** — 214 de 215 usuários são novos, sinal de ausência de estratégia de recorrência
3. **Orgânico lidera em qualidade** — Organic Search tem 47s de engajamento médio, contra 5,9s do Direct
4. **Página "Água" é prioridade** — alto volume (80 visualizações) com rejeição elevada (59,5%), pedindo revisão de UX e CTA
5. **Descoberta via IA generativa** — chatgpt.com e gemini.google.com já aparecem como fontes, ainda residuais
6. **Concentração em BH e SP** — potencial de campanhas regionais segmentadas

---

## 🛠️ Tecnologias utilizadas

| Tecnologia | Uso |
|---|---|
| HTML5 semântico | Estrutura do dashboard |
| CSS custom properties | Design system com suporte a dark/light mode |
| Chart.js (CDN) | Todos os gráficos interativos |
| Fontshare (Satoshi + Cabinet Grotesk) | Tipografia |
| JavaScript vanilla | Navegação entre abas, tema e criação dos gráficos |

> Nenhuma dependência de servidor, build tool ou framework. O arquivo `.html` é autossuficiente.

---

## 🚀 Como usar

1. Faça o download do arquivo `nugap-analytics-dashboard.html`
2. Abra diretamente no navegador (duplo clique ou `File > Open`)
3. Navegue pelas abas no menu lateral
4. Use o botão de alternância de tema para modo escuro/claro

> Compatível com Chrome, Firefox, Safari e Edge em versões recentes.

---

## 📐 Decisões de design

- **Design system baseado no Nexus palette** — superfícies quentes em bege, acento teal, hierarquia de cores semântica
- **Dark mode nativo** via `prefers-color-scheme` com toggle manual
- **Mobile-first** — layout se reorganiza em tela única abaixo de 1100px
- **Dados inline** — todos os dados estão embutidos diretamente no JavaScript para garantir portabilidade total do arquivo

---

## 📌 Limitações e próximos passos

- Os dados estão fixos no arquivo. Para atualização, é necessário re-exportar os CSVs e refazer a ingestão
- A instrumentação de conversões no GA4 precisa ser corrigida antes da próxima coleta
- Sugere-se a criação de públicos segmentados (água, café, institucional) para análises futuras
- A comparação entre períodos (MoM / YoY) requer exportações adicionais do GA4

---

## 👤 Autor

**Vitor Campos**  
Analista de dados — Belo Horizonte, MG
---

## 📄 Licença

Este projeto foi desenvolvido para fins analíticos internos do Nugap. Não contém dados sensíveis de usuários. Os dados são agregados e anonimizados conforme exportado pelo Google Analytics 4.
