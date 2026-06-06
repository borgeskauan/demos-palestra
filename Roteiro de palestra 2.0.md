# Roteiro completo — videoaula/palestra de 1h

**Tema: Uso prático da Inteligência Artificial em programação**

## Abertura

> Nesta apresentação, a proposta é falar sobre Inteligência Artificial de uma forma prática, olhando para o contexto de desenvolvimento de software.
>
> Hoje, a IA aparece em praticamente toda discussão sobre produtividade, automação, geração de código e futuro do trabalho. Mas, para quem programa, o ponto mais importante não é tratar a IA como algo abstrato ou distante. O ponto é entender como ela pode ser aplicada de forma concreta, no dia a dia, para resolver problemas reais.
>
> Então, ao longo desta apresentação, o foco será mostrar a IA em duas frentes: primeiro, como parte de um produto de software; depois, como apoio ao próprio processo de desenvolvimento.

## Parte 1 — O que é IA, de forma simples

> Antes de ir para a prática, vale alinhar rapidamente o que estamos chamando de Inteligência Artificial aqui.
>
> De forma simples, podemos pensar em IA como sistemas capazes de receber uma entrada, interpretar contexto e gerar uma saída útil. Essa saída pode ser texto, resumo, classificação, resposta, organização de conteúdo ou até código.
>
> No contexto atual, isso ficou muito mais acessível com os modelos generativos, que conseguem trabalhar bem com linguagem natural, interpretar instruções e produzir conteúdo a partir de contexto.

## Parte 2 — Diferença entre automação tradicional e IA

> Também é importante separar dois conceitos que às vezes aparecem juntos: automação tradicional e Inteligência Artificial.
>
> Na automação tradicional, a lógica normalmente é mais fixa: se determinada condição acontecer, então o sistema executa uma ação específica.
>
> Já a IA entra melhor em cenários em que existe linguagem natural, ambiguidade, grande volume de informação ou necessidade de gerar uma saída nova a partir de uma base menos estruturada.
>
> Em outras palavras: a automação tradicional executa regras; a IA ajuda a interpretar contexto e produzir respostas quando o problema não está totalmente estruturado.

## Parte 3 — Por que IA importa para desenvolvimento de software

> Do ponto de vista de desenvolvimento, isso importa porque a IA já pode atuar em várias etapas do ciclo de software.
>
> Ela pode ajudar na escrita de código, na explicação de trechos já existentes, em sugestões de refatoração, na criação de documentação, no apoio à prototipação e também na integração de funcionalidades inteligentes dentro do próprio sistema.
>
> Esse é um ponto importante: a IA pode estar tanto no processo de desenvolvimento quanto dentro do produto em si.

## Parte 4 — Benefícios práticos

> Quando falamos dos benefícios da IA para programação, um dos primeiros pontos é produtividade.
>
> Muitas tarefas repetitivas podem ser aceleradas: geração de estruturas iniciais, documentação, exemplos de uso, organização de lógica, apoio em testes e até exploração de soluções possíveis.
>
> Outro benefício muito importante é a prototipação. Com IA, muitas vezes fica mais fácil validar ideias, testar abordagens e chegar mais rápido a uma primeira versão funcional.
>
> Existe também um ganho forte no reaproveitamento de conhecimento. Informações que antes estavam dispersas em atendimentos, documentação, textos ou bases internas podem ser reorganizadas e transformadas em algo mais útil.
>
> Então, em muitos casos, o maior valor da IA não é apenas “fazer mais rápido”, mas reduzir atrito, acelerar experimentação e ampliar a capacidade de entrega.

## Parte 5 — Riscos, limites e cuidados

> Ao mesmo tempo, é importante adotar uma visão equilibrada. A IA traz ganhos reais, mas também traz riscos.
>
> Um dos principais é a possibilidade de gerar saídas convincentes, porém erradas. Isso vale para texto, análise e também para código. Um exemplo muito forte apareceu na área jurídica: em fevereiro de 2025, a Reuters relatou que advogados apresentaram citações jurídicas inexistentes produzidas por IA, e que o escritório Morgan & Morgan chegou a alertar internamente mais de mil advogados sobre esse risco após um caso envolvendo uma ação contra o Walmart. A própria reportagem aponta que tribunais nos Estados Unidos vinham questionando ou punindo advogados em pelo menos sete casos desse tipo nos dois anos anteriores. ([Reuters][1])
>
> Esse exemplo é ótimo porque mostra uma lição que vale também para desenvolvimento de software: saída convincente não significa saída correta. Em código, isso pode significar uma regra de negócio implementada de forma errada, uma biblioteca usada de forma incorreta, uma suposição insegura ou uma solução aparentemente boa, mas inadequada para o contexto.
>
> Outro risco importante é a velocidade sem validação técnica. Em fevereiro de 2026, a Reuters noticiou que a rede social Moltbook, voltada para agentes de IA, teve uma falha que expôs mensagens privadas, mais de 6 mil e-mails de proprietários e mais de 1 milhão de credenciais, segundo a Wiz. A falha foi corrigida depois do contato da empresa de segurança, e o cofundador da Wiz descreveu o problema como um subproduto clássico de “vibe coding”, quando se desenvolve muito rápido com apoio de IA, mas sem o mesmo cuidado com fundamentos básicos de segurança. ([Reuters][2])
>
> Então, quando falamos em uso prático de IA, não estamos falando só de produtividade. Estamos falando também de validação, revisão, teste, segurança, privacidade e responsabilidade.
>
> A ideia central até aqui é a seguinte: a IA pode ser extremamente útil, mas funciona melhor quando existe problema claro, contexto suficiente e supervisão humana.

## Transição para a prática 1

> Com esse contexto em mente, faz sentido sair da teoria e olhar agora para um caso prático de IA integrada a uma aplicação.
>
> A primeira demonstração mostra um cenário em que a IA não está apenas ajudando o desenvolvedor a programar, mas faz parte da própria solução entregue.

---

# Prática 1 — Support FAQ Generator com Gemini API

## Introdução da prática 1

> O primeiro exemplo é um projeto chamado Support FAQ Generator.
>
> A ideia desse projeto é relativamente simples, mas muito útil: a partir de casos de suporte já resolvidos, agregados de diferentes fontes, a aplicação interage com uma IA para gerar FAQs que possam ser reutilizadas para resolver dúvidas ou problemas recorrentes.
>
> Ou seja, em vez de deixar o conhecimento espalhado em históricos de atendimento, o sistema reorganiza esse conteúdo e transforma esse material em algo mais acessível.

## Problema de negócio

> O problema aqui é bastante comum.
>
> Equipes de suporte normalmente acumulam muito conhecimento ao longo do tempo, mas esse conhecimento fica disperso. Parte está em tickets, parte em textos, parte em históricos de conversa, parte em bases pouco organizadas.
>
> O resultado é que dúvidas semelhantes continuam aparecendo, respostas continuam sendo repetidas e o processo de transformar isso em uma FAQ útil costuma ser manual e demorado.

## Solução proposta

> A proposta da aplicação é justamente atacar esse ponto.
>
> O fluxo, de forma resumida, é: coletar os casos resolvidos, consolidar esse material, preparar a entrada, enviar para a API do Gemini, receber a resposta da IA e gerar uma estrutura de FAQ que depois pode ser validada e reaproveitada.
>
> Então aqui a IA entra como parte da solução do produto, e não apenas como apoio ao desenvolvedor.

## O que mostrar na demo

> Nessa demonstração, o mais importante não é mostrar todos os detalhes do projeto, mas o fluxo principal.
>
> Primeiro, a entrada: alguns exemplos de casos de suporte resolvidos.
>
> Depois, a preparação desse conteúdo: como esses dados são organizados para virar uma entrada útil para o modelo.
>
> Em seguida, a chamada para a API do Gemini: o endpoint, o payload, a instrução enviada e a forma como a aplicação trata a resposta.
>
> E por fim, o resultado: as FAQs geradas a partir daquele material.

## Comentário sobre a API

> Aqui vale destacar um ponto importante: integrar uma API de IA, do ponto de vista técnico, não é algo tão distante quanto às vezes parece.
>
> Em muitos casos, a base é parecida com outras integrações que já fazemos no dia a dia: autenticação, envio de payload, tratamento de resposta e validação da saída.
>
> O diferencial está menos na mecânica da requisição e mais no desenho da entrada, na clareza da instrução, na forma de validar a resposta e em como isso se encaixa no fluxo do sistema.

## Ganhos desse caso

> O ganho desse tipo de solução está em reaproveitar conhecimento já existente e transformar informação espalhada em algo mais útil para atendimento, documentação e autosserviço.
>
> É um bom exemplo de IA aplicada a um problema concreto, com valor claro para o negócio.

## Limites dessa prática

> Ao mesmo tempo, esse caso também mostra que a IA não substitui curadoria.
>
> Se os dados de entrada estiverem ruins, incompletos ou inconsistentes, a saída também tende a perder qualidade.
>
> Então, mesmo com uma boa integração, continuam sendo importantes a revisão humana, a definição de formato esperado e, quando necessário, algum pós-processamento ou validação.

## Transição para a prática 2

> Até aqui, vimos a IA atuando como parte de um produto.
>
> Agora vamos olhar para a outra frente: a IA como apoio ao próprio processo de desenvolvimento.

---

# Prática 2 — Agente de codificação alterando um frontend

## Introdução da prática 2

> Na segunda demonstração, a ideia é mostrar a IA apoiando uma tarefa de desenvolvimento de forma mais direta.
>
> Aqui o foco não é uma aplicação que usa IA para atender o usuário final, mas um agente de codificação ajudando a implementar uma modificação em um projeto existente.

## Contexto da demo

> O projeto usado como base é um frontend de dashboard de investimentos.
>
> É um exemplo bom porque tem elementos visuais claros, alguma lógica de apresentação e uma estrutura fácil de entender.
>
> A aplicação lê dados de um arquivo JSON e exibe essas informações em formato de dashboard.

## Como apresentar a demo

> O ideal aqui é mostrar primeiro o estado atual do projeto.
>
> Em seguida, apresentar a necessidade de mudança. Pode ser, por exemplo, adicionar um filtro, um card com indicador novo, uma busca por ativo ou algum ajuste visual com lógica de negócio simples.
>
> Depois disso, mostrar o pedido sendo feito ao agente de codificação, deixar claro qual alteração se espera, observar a modificação proposta e então revisar rapidamente o resultado no código e na interface.

## Mensagem principal dessa prática

> O ponto principal dessa demonstração não é mostrar “mágica”.
>
> O ponto é mostrar aceleração com supervisão.
>
> O agente ajuda a localizar partes do código, sugerir mudanças, organizar implementação e reduzir o esforço inicial. Mas o desenvolvedor continua responsável por revisar, validar e decidir se a alteração realmente atende ao objetivo.

## Ganhos observados

> Esse tipo de uso pode ajudar bastante em tarefas como:
>
> entender uma base já existente;
> localizar pontos de alteração;
> implementar mudanças pequenas e médias;
> acelerar prototipação;
> reduzir tempo gasto com tarefas repetitivas.

## Limites e cautelas

> Ao mesmo tempo, a mesma lógica dos riscos anteriores continua valendo aqui.
>
> Código gerado ou alterado por IA pode parecer correto e ainda assim trazer problemas de lógica, acessibilidade, segurança, estrutura ruim ou quebra de padrão do projeto.
>
> Então a melhor forma de usar esse tipo de ferramenta é como aceleração assistida, não como substituição de revisão técnica.

---

# Fechamento

## Retomada geral

> Para concluir, a proposta desta apresentação foi mostrar a Inteligência Artificial de forma aplicada ao desenvolvimento de software.
>
> Primeiro, vimos a base conceitual: o que é IA, onde ela ajuda, quais benefícios ela pode trazer e quais riscos precisam ser considerados.
>
> Depois, vimos duas frentes práticas bem diferentes e complementares.
>
> Na primeira, a IA apareceu integrada a um produto, ajudando a transformar conhecimento disperso em FAQs úteis por meio da API do Gemini.
>
> Na segunda, a IA apareceu como apoio ao próprio processo de desenvolvimento, ajudando a implementar alterações em um frontend existente.

## Lições principais

> Esses dois exemplos mostram uma coisa importante: a IA pode gerar valor tanto dentro do produto quanto dentro do processo de construção do software.
>
> Mas também mostram que o resultado depende muito de contexto, clareza do problema, qualidade da entrada e validação da saída.
>
> A IA pode acelerar bastante. Ela pode sugerir, organizar, gerar e prototipar. Mas ela não elimina a necessidade de análise técnica.

## Reforço com os casos reais

> E é justamente aí que os exemplos reais citados no começo ganham força.
>
> No caso jurídico relatado pela Reuters em fevereiro de 2025, a IA ajudou a produzir algo que parecia confiável, mas continha referências inexistentes. No caso do Moltbook, relatado pela Reuters em fevereiro de 2026, a velocidade de desenvolvimento associada a “vibe coding” veio acompanhada de uma falha séria de segurança, com exposição de mensagens privadas, milhares de e-mails e mais de um milhão de credenciais. Esses casos reforçam que produtividade sem validação aumenta risco. ([Reuters][1])

## Mensagem final

> Então, a mensagem final não é que a IA substitui o desenvolvimento.
>
> A mensagem final é que a IA amplia capacidade.
>
> Ela ajuda a experimentar mais rápido, organizar conhecimento, acelerar implementação e reduzir atrito em várias tarefas.
>
> Mas o diferencial continua sendo humano: entender o problema certo, decidir como aplicar a tecnologia, validar a saída, cuidar de segurança e garantir qualidade.
>
> Em outras palavras: IA não é mágica. É ferramenta. E, como toda ferramenta poderosa, gera mais valor quando usada com critério.

## Encerramento

> Então, mais do que perguntar se a IA vai substituir quem desenvolve software, talvez a melhor pergunta seja: como usar a IA de forma prática, responsável e útil para construir soluções melhores hoje?

---

# Versão curta de algumas frases de efeito para você encaixar durante a fala

* “IA não é mágica; é ferramenta.”
* “Saída convincente não significa saída correta.”
* “Produtividade sem validação vira risco.”
* “Velocidade sem fundamentos pode virar vulnerabilidade.”
* “O desenvolvedor continua no centro da decisão técnica.”
* “Nem toda automação precisa de IA.”

[1]: https://www.reuters.com/technology/artificial-intelligence/ai-hallucinations-court-papers-spell-trouble-lawyers-2025-02-18 "AI 'hallucinations' in court papers spell trouble for lawyers"
[2]: https://www.reuters.com/legal/litigation/moltbook-social-media-site-ai-agents-had-big-security-hole-cyber-firm-wiz-says-2026-02-02 "'Moltbook' social media site for AI agents had big security hole, cyber firm Wiz says"
