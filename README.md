# Conversor de Notebooks: IPYNB para HTML Interativo

Ferramenta para transformar Jupyter Notebooks (`.ipynb`) em relatórios HTML profissionais — sem instalação local, rodando inteiramente no Google Colab.

Ideal para entregas acadêmicas, portfólios de dados e relatórios executivos onde o foco é a narrativa e o código deve estar acessível sem poluir a leitura.

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/)

---

## Sumário

1. [O Problema que Resolve](#o-problema-que-resolve)
2. [Como Funciona](#como-funciona)
3. [Funcionalidades](#funcionalidades)
4. [Como Usar](#como-usar)
5. [Antes e Depois](#antes-e-depois)
6. [Contribuição](#contribuição)

---

## O Problema que Resolve

A exportação padrão do Jupyter para HTML gera um documento onde blocos de código extensos interrompem o fluxo de leitura da análise. Para quem precisa apresentar resultados — não implementação — esse formato é inadequado.

Este conversor resolve isso em quatro etapas automáticas:

1. Converte o `.ipynb` para HTML.
2. Oculta todas as células de código (inputs) por padrão.
3. Preserva intactos textos em Markdown, tabelas e gráficos.
4. Injeta botões interativos acima de cada bloco de código, permitindo que o leitor expanda apenas o que quiser inspecionar.

---

## Como Funciona

```
arquivo.ipynb
      │
      ▼
[ nbconvert ]  →  HTML base gerado pelo Jupyter
      │
      ▼
[ Injeção CSS/JS ]  →  células de código ocultadas por padrão
                        botões "Ver Código" adicionados
                        textos Markdown protegidos
      │
      ▼
Relatorio_Final.html  →  abre em qualquer navegador, sem Python ou Jupyter
```

O script de injeção CSS/JS é customizável: cores, tipografia e comportamento dos botões podem ser ajustados diretamente no arquivo de configuração.

---

## Funcionalidades

**Interface limpa**
O relatório final tem aparência de artigo ou página web — sem elementos de interface do Jupyter expostos.

**Proteção de texto**
Algoritmos de detecção garantem que células Markdown nunca sejam ocultadas, independentemente da estrutura do notebook.

**Código expansível**
Cada bloco de código recebe um botão "Ver Código" que expande o conteúdo sob demanda, preservando o fluxo narrativo para leitores não técnicos.

**Zero instalação**
Funciona inteiramente no Google Colab. Nenhuma dependência local é necessária.

**Portabilidade total**
O HTML gerado abre em qualquer navegador moderno sem Python, Jupyter ou extensões instaladas.

---

## Como Usar

Nenhuma instalação é necessária. O processo completo leva menos de um minuto.

1. Acesse o notebook via botão **Open in Colab** no topo deste documento.
2. No Google Colab, execute a célula de código clicando em **▶**.
3. Clique no botão de upload e selecione seu arquivo `.ipynb`.
4. Aguarde alguns segundos. O arquivo `Relatorio_Final.html` será baixado automaticamente.

> O arquivo gerado pode ser compartilhado diretamente por e-mail ou publicado em qualquer serviço de hospedagem estática (GitHub Pages, Netlify, etc.).

---

## Antes e Depois

**Antes — exportação padrão do Jupyter**
Código Python intercalado com texto, células de input visíveis e interface do ambiente exposta. A análise fica fragmentada por blocos técnicos.

**Depois — com o conversor**
Apenas títulos, textos explicativos, tabelas e gráficos visíveis. Cada bloco de código fica recolhido e pode ser expandido com um clique, sem interromper a leitura.

---

## Contribuição

Contribuições são bem-vindas. Para sugerir melhorias ou reportar problemas:

1. Faça um fork do repositório.
2. Crie uma branch com a sua alteração (`git checkout -b minha-melhoria`).
3. Abra um Pull Request descrevendo o que foi modificado.

O principal ponto de customização é o script de injeção de CSS/JS — alterações nele afetam diretamente a aparência e o comportamento dos botões no relatório final.
