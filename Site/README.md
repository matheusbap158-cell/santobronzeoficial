# Santo Bronze — Landing Page

Landing page do **Santo Bronze**, salão de bronzeamento natural e a jato de **Diana Alice**, na Vila Joaquim de Sales, Lavras – MG.

## Estrutura

| Arquivo | O que é |
|---|---|
| `index.html` | A landing page completa — HTML, CSS e JS em um único arquivo. |
| `assets/` | A logo otimizada, os ícones da aba, o vídeo de fundo do hero, a imagem de capa dele e as 9 fotos da página (recortadas em 4:5 e otimizadas), vindas do Instagram @santobronzeoficial. |
| `design-system-bronzeamento.html` | Design system da marca (tokens, tipografia, componentes, regras de conversão). Base visual da página. |
| `Info maps.txt` | Dados públicos do perfil no Google Maps: endereço, telefone, nota e avaliações. |
| `Bio insta.txt` | Bio do perfil no Instagram. |
| `Logo/` | Arquivo original da logo nova (PNG com fundo transparente, 1254×1254). |
| `Fotos de fundo/` | Arquivos originais das 3 fotos de fundo das seções (versões otimizadas em `assets/`). |

## Como visualizar

Abra `index.html` no navegador. Não há build nem dependências. **Para publicar, suba o `index.html` junto com a pasta `assets/`** — o vídeo e as fotos são referenciados por caminho relativo.

## Seções

A ordem segue exatamente a prescrita na seção **Conversão** do design system:

1. **Hero** — **vídeo de fundo em reprodução automática** (ombro em luz dourada com sombra de palmeira), título "Santo Bronze" em Bodoni com itálico e script, assinatura "Bri / lho", CTA do WhatsApp e selo "1º lugar no Sales Pesquisa · 3 anos consecutivos" e faixa de prova (4,9 · 79 avaliações · +5.000 · 1º lugar por 3 anos).
2. **Manifesto** (`#manifesto`) — "O bronze vem de dentro para fora": melanina, o que ajuda e o que atrapalha o bronze (texto baseado no post educativo da própria Diana) + **escala interativa de fototipos de pele (I a VI, escala de Fitzpatrick)**, com o que esperar do sol e do bronze em cada um.
3. **Serviços** (`#servicos`) — só atendimentos para clientes: Bronzeamento natural e artificial, Banho de lua e Esfoliação corporal. CTA.
4. **Como funciona** (`#como-funciona`) — as 4 etapas do design system + **gráfico SVG da linha do tempo** do bronze a jato.
5. **Prova social** (`#resultados`) — **medidor da nota 4,9**, **gráfico das palavras mais citadas**, depoimentos reais, **galeria "Resultados reais"** (6 fotos de clientes) e o bloco do **prêmio Sales Pesquisa 2026**. CTA.
6. **Quem aplica** (`#quem-aplica`) — Diana Alice com o troféu, frase dela, números da marca e selos.
7. **Cursos** (`#cursos`) — seção separada, em fundo escuro, para profissionais: Curso de bronzeamento (conteúdo, bônus, 3 certificados, suporte vitalício) e Mentoria, cada um com seu CTA.
7. **Dúvidas** (`#duvidas`) — 8 perguntas em acordeão (`<details>`), abrindo uma por vez.
8. **Formulário** (`#contato`) — 3 campos que abrem o WhatsApp com a mensagem pronta + **ilustração SVG do mapa**.
9. **Fechamento** — "Transformando autoestima" + CTA final. Rodapé com endereço, WhatsApp e Instagram.

São **4 CTAs ao longo da rolagem + o botão flutuante**, como manda o design system. Todos levam ao mesmo WhatsApp; **o Instagram aparece só no rodapé**.

## Fotos e vídeo

| Arquivo | Onde aparece | Post de origem |
|---|---|---|
| `logo-santo-bronze.png` | Cabeçalho e selo na foto da Diana | `Logo/` — recortada sem as margens vazias e reduzida de 1,1 MB para 50 KB |
| `logo-santo-bronze-escuro.png` | Rodapé | Versão para fundo escuro, gerada a partir da logo: sem o brilho claro em volta das letras e com o slogan em champanhe |
| `favicon-64.png` / `favicon-180.png` | Ícone da aba e da tela inicial do iPhone | Emblema do sol, recortado da logo |
| `hero-video-pele-sol.mp4` | Fundo do hero | Arquivo enviado na pasta do projeto (antes `Woman_breathing_in_sunlight_20260911074807.mp4`) |
| `hero-video-poster.jpg` | Capa do vídeo (e imagem de compartilhamento) | Quadro extraído do próprio vídeo |
| `servico-bronzeamento.jpg` | Card de bronzeamento | instagram.com/p/DUd8OaHAZzu |
| `servico-banho-de-lua.jpg` | Card de banho de lua | `Conteúdos/Imagens/` (…100233) |
| `servico-esfoliacao.jpg` | Card de esfoliação | `Conteúdos/Imagens/` (…100214), recortada sem o rótulo do pote |
| `servico-curso-alunas.jpg` | Curso (seção Cursos) | instagram.com/p/DYAW494HL7S |
| `servico-mentoria-diana.jpg` | Mentoria (seção Cursos) | instagram.com/p/DbrgbW7Tdj2 (recortada sem o texto do post) |
| `resultado-real-1.jpg` a `resultado-real-6.jpg` | Galeria "Resultados reais" | Fotos enviadas em `Site/Resultados Reais/` (1.png a 6.png), recortadas em 4:5 |
| `premio-sales-pesquisa-2026.jpg` | Bloco do prêmio | instagram.com/p/DcZC99poHK- |
| `diana-alice-trofeu.jpg` | Quem aplica | instagram.com/p/DcZC99poHK- |
| `fundo-como-funciona-pele-sol.jpg` | Fundo de "Como funciona" | `Site/Gere_uma_imagem_ultra_realista_2K_20260913082011.jpeg`, de 1,9 MB para 94 KB |
| `fundo-contato-pernas-agua.jpg` | Fundo da seção do formulário | `Fotos de fundo/` — pernas na água (…085149.jpeg), de 2,2 MB para 90 KB |
| `fundo-fechamento-tons-de-pele.jpg` | Fundo do fechamento | `Fotos de fundo/` — dois tons de pele (…085125.jpeg), de 3,3 MB para 215 KB |

Critério de escolha, seguindo o design system: luz dourada, pele real com textura, diversidade de tons, sem banco de imagem e sem fundo branco de estúdio. Ficaram de fora os posts só de texto, os memes e as fotos com tapa-mamilo, que não combinam com uma página de conversão.

## Conversion pass (jornada e conversão)

Ajuste de copy, ordem e fricção feito sobre o site já polido. Não houve mudança de identidade visual e nenhum dado foi inventado: preços, durações e depoimentos continuam exatamente como estavam.

**Nova ordem da página:** Hero → Serviços → **Resultados reais** → Como funciona → **Sua pele** (fototipos) → Avaliações → Quem aplica → Dúvidas → Agendamento → Fechamento → **Cursos**.
- **Resultados** vieram para logo depois dos serviços, porque "como eu posso ficar?" é o que gera desejo e antes estava enterrado no meio das avaliações.
- **"Sua pele"** foi para depois de "Como funciona": responde à objeção "combina com o meu tom?", mas é técnico demais para abrir a página.
- **Cursos** foram para o fim. É outro público (profissionais) e interrompia a cliente logo antes das dúvidas e do agendamento.

**Hero:** o subtítulo virou benefício concreto ("Marquinha desenhada, cor por igual e aquele dourado de quem acabou de voltar das férias…"). O CTA secundário passou de "Ver serviços" para **"Ver resultados reais"**.

**CTAs:** o principal é sempre "Agendar meu bronze pelo WhatsApp". Ele aparece no hero, depois dos serviços, depois dos resultados ("Quero esse resultado"), depois das avaliações, no formulário e no fechamento, além do botão flutuante, que agora diz "Agendar meu bronze". O microtexto "Resposta rápida" (não verificável) virou **"Abre o WhatsApp com a mensagem pronta · sem compromisso"**, que diz o que acontece ao tocar.

**Avaliações:** o depoimento em destaque agora é o da Valeria Rosa, que nunca tinha feito bronzeamento; ele responde à insegurança da primeira vez. Os textos dos depoimentos não foram alterados. A linha de selos repetidos embaixo dos serviços saiu, porque a mesma prova já aparece no hero, nos números e no prêmio.

**Sua pele:** a escala de fototipos ganhou o link "Descobrir qual bronze combina comigo", que abre o WhatsApp.

**Dúvidas:** as perguntas que mais travam o agendamento vêm primeiro (primeira vez, se fica artificial ou laranja, duração). As de saúde vêm depois. O destaque "Bronze e melasma" do título saiu; a pergunta continua no FAQ.

**Formulário:** saiu o campo "Seu WhatsApp", redundante, porque a conversa já acontece no WhatsApp da cliente. Agora são 2 campos. Escolher "curso" ou "mentoria" gera "quero saber sobre…" em vez da mensagem truncada "quero agendar um bronze para o curso".

**Menu:** acompanha a nova ordem (Serviços, Resultados, Como funciona, Sua pele, Avaliações, Dúvidas, Contato, Cursos).

## Premium polish (direção de arte)

Refinamento feito sobre o site pronto, sem reconstruir nada: mesmo HTML, mesmos textos, links, formulário e funcionalidades. Quase tudo está numa única camada CSS comentada, `PREMIUM POLISH`, no fim do `<style>`. Para desfazer, basta apagar esse bloco.

- **Menos caixas:** serviços, "ajuda/atrapalha", depoimentos, frases curtas, números e diferenciais do curso deixaram de ser cartões com borda e viraram composição editorial com fios finos. Continuam como cartão só os componentes de verdade: a escala de fototipos, o formulário e os blocos de curso.
- **Hero:** "Brilho" deixou de ser um segundo título gigante e virou legenda de campanha no canto da imagem, com o mesmo texto. O selo do prêmio ficou mais discreto e a faixa de números virou uma linha editorial, sem células de painel.
- **Serviços:** o bronzeamento é o destaque, em formato horizontal e ocupando a linha inteira. Banho de lua e esfoliação vêm lado a lado, e todos ganharam numeração editorial (01, 02, 03).
- **Resultados reais:** as colunas ficaram desencontradas, como numa revista, em vez da grade uniforme.
- **Tipografia e respiro:** as seções passaram de 96px para até 148px de espaçamento vertical. O eyebrow ganhou um fio e as legendas internas seguem um padrão único de caixa-alta.
- **CTAs e microinterações:** o hover dos botões ganhou elevação sutil, os links ganharam sublinhado que "desenha" e seta, o menu ganhou sublinhado animado e o topo ganhou sombra ao rolar. Imagens têm zoom lento no hover. O FAQ usa +/−, e a revelação na rolagem ficou mais suave.
- **Selos:** trocados de etiquetas cheias por contorno fino.
- **Depoimentos:** saíram as 5 estrelas de cada avaliação, porque o dado do Google não traz nota por avaliação. A nota 4,9 continua no painel.
- **Mobile:** o menu horizontal ganhou esmaecido à direita, indicando que rola. As fotos de serviço passaram a 4:3 para não ficarem altas demais, e os espaçamentos foram revistos.
- **Correções encontradas no QA:**
  - Os números da faixa do topo apareciam no tamanho da legenda (bug antigo).
  - A faixa encostava na borda da tela no celular.
  - A legenda do hero tinha contraste abaixo de AA sobre o brilho da pele; ganhou sombra localizada.

Conferido em 320, 390, 768, 1024 e 1440px, sem rolagem lateral e com todos os alvos de toque de pelo menos 44px. Formulário, FAQ, vídeo, escala de fototipos e os 14 links de WhatsApp continuam funcionando, sem erros no console. O texto visível é idêntico ao de antes.

## Decisões técnicas

- **Design system aplicado integralmente**: os 15 tokens de cor, as 3 famílias tipográficas (Bodoni Moda + Jost + Ms Madi), a escala de espaçamento base 8 (`--space-1` a `--space-8`), os raios por nível de interatividade (0 para blocos e fotos, 2px para botões e campos, circular só no flutuante), as sombras tingidas de marrom, as texturas e o **degradê âmbar sobre foto** para garantir leitura do texto claro.
- **Regras de tipografia respeitadas**: título em sílabas ("Bri / lho") usado **uma única vez**, no hero; itálico da Bodoni marcando uma palavra por título; script (Ms Madi) só em palavras do universo da marca — *glow*, *bronze*, *tom*, *autoestima* — e nunca em botão ou preço.
- **Mobile-first**, com três faixas: mobile (< 768px), **tablet (768–1023px)** e desktop (≥ 1024px). Sem overflow horizontal de 320px a 1366px (verificado).
- **Acessibilidade**: HTML semântico, link "pular para o conteúdo", um único `<h1>`, `alt` descritivo em todas as 12 imagens (o vídeo é decorativo e fica oculto para leitores de tela), `aria-label` nos ícones e gráficos, `aria-pressed` na escala de tons, `aria-live` no formulário, foco visível com anel Mel e **todos os alvos de toque com no mínimo 44px** (verificado).
- **Contraste**: todos os pares de texto usam as combinações aprovadas do design system ou melhores.
- **Logo**: a arte original tem brilho claro em volta das letras e o slogan em vermelho escuro, que viram névoa e somem sobre fundo escuro. No cabeçalho (creme) ela vai direto; no selo sobre a foto, vai sobre fundo creme; no rodapé (espresso) usa a versão `logo-santo-bronze-escuro.png`, sem o brilho e com o slogan em champanhe.
- **Fotos de fundo**: três seções têm foto atrás de um véu de cor da paleta — o formulário em creme (o design system prevê "formulário sobre foto") e o fechamento em cacau. As opacidades mantêm o texto em contraste AA mesmo sobre as partes mais claras ou escuras de cada foto. São decorativas: `alt=""` e `aria-hidden`, para o leitor de tela não anunciar.
- **"Como funciona"**: fundo carvão com a foto de pele em luz dourada (`assets/fundo-como-funciona-pele-sol.jpg`, a partir de `Site/Gere_uma_imagem_ultra_realista_2K_20260913082011.jpeg`, de 1,9 MB para 94 KB) sob véu escuro, mais fechado no topo para o título e aberto no meio. A foto de esfoliação que ficava ali antes foi retirada a pedido.
- **Performance**: sem frameworks nem bibliotecas. Todas as fotos em JPEG otimizado, com `width`/`height` declarados (sem salto de layout) e `loading="lazy"`.
- **Vídeo do hero**: `autoplay muted loop playsinline` — sem som e em linha, que é o que o iPhone e o Chrome exigem para tocar sozinho. A capa (`poster`) aparece enquanto o vídeo carrega. Um botão de pausar/reproduzir fica no canto superior direito, porque conteúdo em movimento que se repete precisa poder ser parado (WCAG 2.2.2). O vídeo pausa sozinho quando sai da tela, para poupar bateria, e **não é carregado** com movimento reduzido ativado ou no modo economia de dados — nesses casos fica só a capa. Um degradê espresso por cima garante o contraste do texto.
- **Progressive enhancement**: sem JavaScript, todo o conteúdo continua visível — a escala de tons e o gráfico de palavras estão escritos no HTML; o JS só liga a interação e a animação.
- **Movimento reduzido**: `prefers-reduced-motion` desliga todas as transições, animações e a rolagem suave.

## Fontes

As 3 tags `<link>` marcadas no `<head>` (Google Fonts) são **o único recurso externo da página**. Para rodar 100% offline, remova-as: a página cai para os fallbacks já declarados nos tokens (Georgia + fonte de sistema).

## Conteúdo verificado

- Nome, endereço, CEP, plus code e telefone — `Info maps.txt`.
- Nota **4,9** com **79 avaliações**, os depoimentos e o gráfico de palavras (resultado 6, autoestima 4, ambiente 4, educada 3, nota 2, atendimento 2) — avaliações públicas do Google.
- "Se identifica como uma empresa de empreendedoras" — atributo do perfil no Google.
- "+ de 5000 mulheres atendidas", "Transformando autoestima", "Cursos | Mentoria", "Garanta seu momento" e o WhatsApp — `Bio insta.txt`.
- Do Instagram @santobronzeoficial:
  - **Diana Alice** é a dona e especialista — apresentada como "referência na área do bronzeamento natural e artificial" no post do evento Experience Bronze, em Fortaleza.
  - **1º lugar no Sales Pesquisa, categoria Bronzeamento, Lavras-MG, por 3 anos consecutivos** (o mais recente em 2026). O troféu de 2026 está no Instagram; os "3 anos consecutivos" foram informados pela cliente em 13/09/2026.
  - A frase "A melhor parte do meu trabalho é ver o sorriso de quem chega e a confiança de quem sai." — legenda de um post dela.
  - Conteúdo do curso (do zero ao profissional, 3 em 1, 100% presencial, 3 certificados, suporte vitalício, vagas limitadas) e da mentoria — posts de divulgação.
  - "Não existe uma resposta única… É personalização" e a pergunta sobre Roacutan — posts educativos do próprio perfil.

## Pendências antes de publicar

- [ ] **Autorização de imagem das clientes.** As fotos são posts públicos do próprio Santo Bronze, mas uma cliente aparece de rosto na galeria (foto 2). Confirmar com a Diana que elas autorizam o uso também no site.
- [ ] **Revisar os textos com a cliente.** Não havia arquivo de copy na pasta; os textos foram escritos a partir da bio, das avaliações e das legendas do Instagram.
- [ ] **Respostas do FAQ**: melasma, gestantes, duração e primeiro banho foram redigidos de forma conservadora. A de Roacutan segue o post do próprio perfil. **Precisam do aval técnico da Diana.**
- [ ] **Preços**: omitidos de propósito (não havia esse dado). Os cards dizem "Valores pelo WhatsApp".
- [ ] **Peso do vídeo (opcional)**: o arquivo tem 3,3 MB para 8 segundos e ainda carrega uma faixa de áudio que nunca toca. Recomprimido sem áudio (por exemplo, com `ffmpeg -i hero-video-pele-sol.mp4 -an -vcodec libx264 -crf 28 -preset slow -movflags +faststart saida.mp4`), deve cair para cerca de 1 MB sem perda visível — bom para quem abre pelo 4G.
- [ ] **Rótulo na foto de esfoliação**: o pote da foto original traz o nome de uma marca ("CEMBRI"). No card de Esfoliação corporal o recorte deixa o rótulo de fora; se trocar o recorte, confirmar se não é uma marca real.
- [ ] **Novos serviços**: *Banho de lua* foi pedido pela cliente; *Esfoliação corporal* foi uma sugestão para completar os três cards. Confirmar se ela oferece a esfoliação como serviço avulso e revisar a descrição dos dois.
- [ ] **Textos dos fototipos**: as descrições de cada fototipo e os cuidados "no bronze" foram escritos de forma conservadora, a partir da escala de Fitzpatrick e do post da Diana sobre melanina. **Precisam do aval técnico dela** — principalmente a indicação de bronze a jato para os fototipos I e II.
- [ ] **Horário de funcionamento**: omitido — o perfil do Google não tem esse dado. Vale preencher também no Google Meu Negócio.
- [ ] **Experience Bronze**: o selo diz "Convidada do Experience Bronze, em Fortaleza". O post fala da 10ª edição, em 2027 — confirmar se ela já participou ou se vai participar, e ajustar o texto se preciso.
