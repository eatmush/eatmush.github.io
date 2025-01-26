---
layout: post
title: "GA4: Sessões vs session_start"
categories: misc
published: true
---

A métrica "Sessões" no GA4 não é a contagem do evento “session_start”!

Diferentemente da métrica "Visualizações", que é a soma da contagem dos eventos "page_view" e "screen_view", a métrica "Sessões" não é a contagem do evento "session_start", como podemos ser induzidos a pensar.

A métrica "Sessões" é, na verdade, uma CONTAGEM DISTINTA de todos os IDs de sessões que fizeram o disparo de pelo menos um evento do GA4 dentro do seu site ou app (sim, cada sessão possui um ID único).

Essa forma como a métrica "Sessões" é calculada faz com que nem sempre ela bata com a contagem do evento "session_start", dependendo dos dados que estão sendo analisados.

Por exemplo, se você estiver fazendo uma análise usando a dimensão "Local da página", o valor da métrica "Sessões" provavelmente será maior quando comparada com a contagem do evento "session_start" (olhando para uma mesma página), pois nem toda sessão que passou por aquela página necessariamente fez um disparo desse evento.

Porém, se a análise estiver sendo feita apenas a nível de "Data" (dimensão) e o valor das duas métricas estiverem muito discrepantes entre si, pode estar ocorrendo alguma falha mais específica na implementação do GA4 em algumas páginas/telas do seu site/app. Não preciso nem dizer que, caso isso estiver ocorrendo, é recomendado que a implementação seja corrigida o mais rápido possível! 😉