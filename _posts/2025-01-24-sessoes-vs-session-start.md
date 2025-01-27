---
layout: post
title: "GA4: Sessões vs. evento session_start"
categories: misc
published: true
excerpt: "Diferentemente da métrica Visualizações, que é a soma dos eventos page_view e screen_view, a métrica Sessões não é a simples contagem do evento session_start."
---

![Google Analytics 4 (GA4) logo](../imagens/Logo_Google_Analytics_1920x1080-1024x576.png)

Diferentemente da métrica **Visualizações**, que é a soma dos eventos `page_view` e `screen_view`, a métrica **Sessões** não é a simples contagem do evento `session_start` como podemos ser induzidos a pensar.

#### O que é a métrica Sessões?

A métrica **Sessões** é, na verdade, uma **contagem distinta** de todos os IDs de sessão que dispararam pelo menos um evento do GA4 em seu site ou app. Cada sessão possui um ID único, o que significa que:

- A métrica **Sessões** não depende exclusivamente do evento `session_start`.
- Sessões só são contabilizadas quando há eventos vinculados a elas.

#### Por que Sessões nem sempre bate com session_start?

Dependendo da análise que você está fazendo, os valores de **Sessões** e a contagem de `session_start` podem ser diferentes.

Por exemplo, se você estiver fazendo uma análise usando a dimensão **Local da página**, o valor da métrica **Sessões** provavelmente será maior quando comparada com a contagem do evento `session_start` (olhando para uma mesma página), pois nem toda sessão que passou por aquela página necessariamente fez um disparo desse evento.

Porém, se a análise estiver sendo feita apenas a nível de **Data** (dimensão) e o valor das duas métricas estiverem muito discrepantes entre si, pode estar ocorrendo alguma falha mais específica na implementação do GA4 em algumas páginas/telas do seu site/app.

#### O que fazer em caso de discrepância?

Se você identificar diferenças significativas entre as duas métricas fazendo a análise por **Data**, é recomendável:  

1. Revisar a implementação do GA4 para garantir que os eventos do GA4 estejam sendo disparados corretamente em todas as páginas ou telas.
2. Corrigir possíveis falhas **o mais rápido possível**, para evitar inconsistências nos relatórios e análises.

Ao entender como a métrica **Sessões** funciona, você estará mais preparado para interpretar os dados corretamente e identificar potenciais problemas na sua configuração do GA4.