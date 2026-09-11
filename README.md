# Santo Bronze — Landing Page

Landing page do **Santo Bronze**, salão de bronzeamento natural e a jato de **Diana Alice**, na Vila Joaquim de Sales, Lavras – MG.

## Estrutura

| Arquivo | O que é |
|---|---|
| `index.html` | A landing page completa — HTML, CSS e JS em um único arquivo, com a logo embutida em base64. |
| `assets/` | O vídeo de fundo do hero, a imagem de capa dele e as 9 fotos da página (recortadas em 4:5 e otimizadas), vindas do Instagram @santobronzeoficial. |
| `design-system-bronzeamento.html` | Design system da marca (tokens, tipografia, componentes, regras de conversão). Base visual da página. |
| `Info maps.txt` | Dados públicos do perfil no Google Maps: endereço, telefone, nota e avaliações. |
| `Bio insta.txt` | Bio do perfil no Instagram. |
| `Logo/` | Arquivo original da logo. |

## Como visualizar

Abra `index.html` no navegador. Não há build nem dependências. **Para publicar, suba o `index.html` junto com a pasta `assets/`** — o vídeo e as fotos são referenciados por caminho relativo.

## Seções

A ordem segue exatamente a prescrita na seção **Conversão** do design system:

1. **Hero** — **vídeo de fundo em reprodução automática** (ombro em luz dourada com sombra de palmeira), título em Bodoni com itálico e script, assinatura "Na / tu / ral", CTA do WhatsApp e faixa de prova (4,9 · 79 avaliações · +5000 · 1º lugar Sales Pesquisa 2026).
2. **Manifesto** (`#manifesto`) — "Cada pele carrega um momento" + **gráfico interativo da escala de tons** do bronze a jato.
3. **Serviços** (`#servicos`) — Bronzeamento natural e a jato, Curso de bronzeamento e Mentoria, cada um com foto real. CTA.
4. **Como funciona** (`#como-funciona`) — as 4 etapas do design system + **gráfico SVG da linha do tempo** do bronze a jato.
5. **Prova social** (`#resultados`) — **medidor da nota 4,9**, **gráfico das palavras mais citadas**, depoimentos reais, **galeria "Resultados reais"** (4 fotos) e o bloco do **prêmio Sales Pesquisa 2026**. CTA.
6. **Quem aplica** (`#quem-aplica`) — Diana Alice com o troféu, frase dela, números da marca e selos.
7. **Dúvidas** (`#duvidas`) — 8 perguntas em acordeão (`<details>`), abrindo uma por vez.
8. **Formulário** (`#contato`) — 3 campos que abrem o WhatsApp com a mensagem pronta + **ilustração SVG do mapa**.
9. **Fechamento** — "Transformando autoestima" + CTA final. Rodapé com endereço, WhatsApp e Instagram.

São **4 CTAs ao longo da rolagem + o botão flutuante**, como manda o design system. Todos levam ao mesmo WhatsApp; **o Instagram aparece só no rodapé**.

## Fotos e vídeo

| Arquivo | Onde aparece | Post de origem |
|---|---|---|
| `hero-video-pele-sol.mp4` | Fundo do hero | Arquivo enviado na pasta do projeto (antes `Woman_breathing_in_sunlight_20260911074807.mp4`) |
| `hero-video-poster.jpg` | Capa do vídeo (e imagem de compartilhamento) | Quadro extraído do próprio vídeo |
| `resultado-colo-marquinha.jpg` | Galeria | instagram.com/p/DX4nF6THMQs |
| `servico-bronzeamento.jpg` | Card de bronzeamento | instagram.com/p/DUd8OaHAZzu |
| `servico-curso-alunas.jpg` | Card do curso | instagram.com/p/DYAW494HL7S |
| `servico-mentoria-diana.jpg` | Card da mentoria | instagram.com/p/DbrgbW7Tdj2 (recortada sem o texto do post) |
| `resultado-diana-e-cliente.jpg` | Galeria | instagram.com/p/DUn8rGajvOD |
| `resultado-marquinha-cliente.jpg` | Galeria | instagram.com/p/DUn8rGajvOD |
| `aplicacao-biquini-de-fita.jpg` | Galeria | instagram.com/p/DYAW494HL7S |
| `premio-sales-pesquisa-2026.jpg` | Bloco do prêmio | instagram.com/p/DcZC99poHK- |
| `diana-alice-trofeu.jpg` | Quem aplica | instagram.com/p/DcZC99poHK- |

Critério de escolha, seguindo o design system: luz dourada, pele real com textura, diversidade de tons, sem banco de imagem e sem fundo branco de estúdio. Ficaram de fora os posts só de texto, os memes e as fotos com tapa-mamilo, que não combinam com uma página de conversão.

## Decisões técnicas

- **Design system aplicado integralmente**: os 15 tokens de cor, as 3 famílias tipográficas (Bodoni Moda + Jost + Ms Madi), a escala de espaçamento base 8 (`--space-1` a `--space-8`), os raios por nível de interatividade (0 para blocos e fotos, 2px para botões e campos, circular só no flutuante), as sombras tingidas de marrom, as texturas e o **degradê âmbar sobre foto** para garantir leitura do texto claro.
- **Regras de tipografia respeitadas**: título em sílabas ("Na / tu / ral") usado **uma única vez**, no hero; itálico da Bodoni marcando uma palavra por título; script (Ms Madi) só em palavras do universo da marca — *glow*, *bronze*, *tom*, *autoestima* — e nunca em botão ou preço.
- **Mobile-first**, com três faixas: mobile (< 768px), **tablet (768–1023px)** e desktop (≥ 1024px). Sem overflow horizontal de 320px a 1366px (verificado).
- **Acessibilidade**: HTML semântico, link "pular para o conteúdo", um único `<h1>`, `alt` descritivo em todas as 12 imagens (o vídeo é decorativo e fica oculto para leitores de tela), `aria-label` nos ícones e gráficos, `aria-pressed` na escala de tons, `aria-live` no formulário, foco visível com anel Mel e **todos os alvos de toque com no mínimo 44px** (verificado).
- **Contraste**: todos os pares de texto usam as combinações aprovadas do design system ou melhores.
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
  - **1º lugar no Sales Pesquisa 2026, categoria Bronzeamento, Lavras-MG**, e "mais um ano recebendo o reconhecimento de Melhores do Ano".
  - A frase "A melhor parte do meu trabalho é ver o sorriso de quem chega e a confiança de quem sai." — legenda de um post dela.
  - Conteúdo do curso (do zero ao profissional, 3 em 1, 100% presencial, 3 certificados, suporte vitalício, vagas limitadas) e da mentoria — posts de divulgação.
  - "Não existe uma resposta única… É personalização" e a pergunta sobre Roacutan — posts educativos do próprio perfil.

## Pendências antes de publicar

- [ ] **Autorização de imagem das clientes.** As fotos são posts públicos do próprio Santo Bronze, mas duas clientes aparecem de rosto na galeria. Confirmar com a Diana que elas autorizam o uso também no site.
- [ ] **Revisar os textos com a cliente.** Não havia arquivo de copy na pasta; os textos foram escritos a partir da bio, das avaliações e das legendas do Instagram.
- [ ] **Respostas do FAQ**: melasma, gestantes, duração e primeiro banho foram redigidos de forma conservadora. A de Roacutan segue o post do próprio perfil. **Precisam do aval técnico da Diana.**
- [ ] **Escala de tons**: os 5 tons do gráfico interativo são uma construção didática. Ajustar para os tons que o Santo Bronze realmente trabalha no jato.
- [ ] **Preços**: omitidos de propósito (não havia esse dado). Os cards dizem "Valores pelo WhatsApp".
- [ ] **Peso do vídeo (opcional)**: o arquivo tem 3,3 MB para 8 segundos e ainda carrega uma faixa de áudio que nunca toca. Recomprimido sem áudio (por exemplo, com `ffmpeg -i hero-video-pele-sol.mp4 -an -vcodec libx264 -crf 28 -preset slow -movflags +faststart saida.mp4`), deve cair para cerca de 1 MB sem perda visível — bom para quem abre pelo 4G.
- [ ] **Horário de funcionamento**: omitido — o perfil do Google não tem esse dado. Vale preencher também no Google Meu Negócio.
- [ ] **Experience Bronze**: o selo diz "Convidada do Experience Bronze, em Fortaleza". O post fala da 10ª edição, em 2027 — confirmar se ela já participou ou se vai participar, e ajustar o texto se preciso.
