# Olist E-Commerce Analytics: Plataforma End-to-End de Inteligência de Dados

**Responsável Técnico:** Matheus Siqueira — *Especialista em Business Intelligence*
**Stack Tecnológica:** Power BI, Python (spaCy), SQL (Snowflake), Streamlit, Data Quality

---

## 🚀 Visão Geral do Projeto

Este repositório apresenta a construção de uma solução completa de Analytics para um ecossistema de e-commerce de alta volumetria (Dataset Olist, +100k pedidos). O projeto foi desenvolvido para demonstrar a implementação de uma esteira de dados moderna, cobrindo desde a ingestão bruta até a entrega de insights prescritivos via IA e Dashboards de UX avançado.

### 📅 Arquitetura e Fluxo de Entrega
- **Planejamento:** Organização focada em infraestrutura Bronze/Silver antes da camada Gold (Modelagem).
- **Ingestão & Governança:** Processamento de Big Data com catalogação técnica e funcional.
- **Qualidade de Dados:** Implementação de **Data Contracts** para garantir a integridade da camada de consumo.
- **Enriquecimento com IA:** Motor de **NLP** para extração de sentimento e calibração de Ground Truth.
- **Visualização:** Modelagem Dimensional (**Star Schema**) e Data App interativo.

---

## 🕵️ Data Quality e Observabilidade (Data Contracts)

Para garantir que a tomada de decisão seja baseada em dados íntegros, implementei um pipeline de auditoria automatizada fundamentado em observabilidade, utilizando lógica inspirada no framework *Great Expectations*.

**Regras de Auditoria (Script `data_quality.py`):**
* **Consistência de Domínio:** Validação estatística para assegurar que os scores de review estejam rigorosamente entre 1 e 5.
* **Integridade Referencial:** Monitoramento de nulos em chaves primárias (PKs) para evitar "dados órfãos".
* **Health Check:** Geração de métricas descritivas em tempo real para detecção de anomalias na carga.

---

## 🤖 Engenharia de Features com IA (Advanced NLP)

O diferencial desta solução é o processamento de textos desestruturados para transformar reviews em métricas acionáveis.

**Motor de Inferência Híbrida (`power_query_nlp.py`):**
* **NLP com spaCy:** Utilização de lematização para identificar a raiz semântica das reclamações e elogios.
* **Calibração de Sentimento:** Desenvolvimento do **"IA Score"**, que correlaciona a semântica do texto com a nota real deixada pelo cliente, eliminando vieses e entregando uma percepção fiel da experiência do usuário.

---

## 📐 Modelagem de Dados e Performance

Desenvolvi uma modelagem **Star Schema** (Fato/Dimensão) focada em alta performance de consulta no motor tabular.

### 🏗️ Engenharia de Analytics
1. **Governança de Dados:** Padronização em `snake_case` para garantir interoperabilidade entre sistemas.
2. **Vertical Partitioning:** Remoção estratégica de colunas de alta cardinalidade para otimizar o consumo de memória RAM e acelerar o refresh.
3. **Type Safety:** Tratamento de locale e tipagem explícita para evitar erros em campos monetários e geográficos.
4. **Data Enrichment:** Enriquecimento geográfico (Lat/Long) para análises de capilaridade de mercado.

---

## 📊 Dashboards e UX Avançado

A solução de visualização foi dividida em camadas estratégicas para diferentes níveis de decisão:

1. **Executive Insights:** Focado em faturamento, saúde financeira e breakdown de gargalos logísticos (Lead Time).
2. **Operational Intelligence:** Monitoramento de "Best Sellers", áreas de atenção crítica e diagnóstico automático de **Risco de Churn** baseado no sentimento.

**Destaques Técnicos:**
* Injeção de **HTML/SVG via DAX** para visuais customizados.
* Mapa de calor de alta densidade para logística de Last Mile.
* Glossário de métricas integrado para governança de dados.

---

## 📱 Interactive Data Application (Streamlit)

Além do BI tradicional, desenvolvi um **Data App** em Python para democratizar o acesso aos KPIs operacionais.
* Filtros dinâmicos por região e categoria.
* Monitoramento de NPS e metas de entrega.
* Interface otimizada para consulta rápida por gestores de campo.

---

**Desenvolvido por Matheus Siqueira**
