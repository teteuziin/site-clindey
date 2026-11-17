# Site — CLINDEY Estética Avançada & Emagrecimento (@clindeyestetica)

Site-modelo da fase 2 da missão de prospecção (empresa nº4), construído a partir do portfólio real da clínica. **NÃO PUBLICAR sem aprovação do usuário** — publicação no GitHub/Pages somente após o OK dele.

## Conceito — "O Diamante Rosa"
As seções são as facetas da lapidação do diamante rosa dela: molduras de filete duplo em rosé com um losango no topo (a geometria do símbolo da logo), vinho profundo alternando com porcelana quente, serifada elegante (Fraunces) + Archivo. Um único acento: o rosé da marca.

## Estrutura
- `index.html` — página única (intro temática ≤1,8s pulável, hero, Método Pink Diamond com etapas interativas, Resultados + depoimento, Lipo sem cortes com carrossel Criodermys, Experiência premium, Dra. Deyse com linha do tempo interativa, Avaliação com montador de mensagem para o direct, Comunidade Florescer, endereço/horários, rodapé)
- `media/` — 10 vídeos reais dela (9 reels com áudio AAC + slide animado da Criodermys, sem áudio por natureza), pôsteres extraídos dos próprios vídeos, fotos reais (recepção, sala, consulta, espelho/robe), retrato da Dra. Deyse e foto dos fundadores (recortes limpos das artes dela, sem o texto das campanhas), logo em 2 versões produzidas a partir da oficial

## Logo sem fundo (instrução do usuário)
A oficial (`clindey-portfolio/marca/logo-clindey-fonte.jpg`) tem fundo vinho sólido (#5C0527). Produzidas:
- `media/logo-transparente.png` — fundo removido por distância de cor com desmultiplicação (bordas limpas conferidas sobre fundo escuro): símbolo rosé + "Clindey" branca + assinatura rosé. Usada nas seções vinho, na intro e no rodapé.
- `media/logo-vinho.png` — variante para seções claras: wordmark branca → vinho #570A22 e rosé aprofundado (×0,62) para não sumir no fundo claro. Usada no cabeçalho.

## Conteúdo — só o verificado (ficha: ../clindey-portfolio/README.md)
- Método Pink Diamond: promessa dela "até 2 números de roupa em 45 dias"; +10.000 pacientes
- Resultados publicados por ela: antes/depois com perdas de 10 kg a 29 kg (vídeo do treinamento da equipe)
- Lipo sem cortes — Criodermys 2.0; protocolos dela: diástase, pós-operatório, gordura localizada, flacidez, circulação, saúde da mulher
- Procedimentos SEM preço público (decisão dela — vídeo 09 explica): o site vende a avaliação. Único preço: Comunidade Florescer R$ 19,90/mês
- Horários DELA (post de 14/11/2026): terça a sexta 8h–19h; sábado 8h–14h (os do Google estão desatualizados — não usados)
- Endereço: Rua Dr. José Peroba, 325, Ed. Elite Comercial, sala 1606, Stiep, Salvador/BA

## Escolhas sinalizadas
- **Telefone/WhatsApp: NENHUM número exibido.** Circulam 3 números conflitantes (Google 71 98386-0692; Solutudo 71 99126-6429; arte de vaga/RH 71 99381-6429), nenhum confirmado como WhatsApp de agendamento dela. CTA único = direct do Instagram (com montador de mensagem que copia o texto e abre o perfil).
- **Vídeos 360×640** (03-resultados e 12-dez-anos): exibidos em moldura contida de no máximo 300px de largura — nunca esticados.
- **Domínio clindeyestetica.com.br**: é dela, mas está morto (não resolve) — não é linkado nem citado no site; é o gancho da abordagem comercial.
- Fora do site, de propósito: a promessa antiga "10–15 kg em 2 meses" (abr/2025, desatualizada), qualquer serviço facial/botox/laser (não são dela — foco 100% corporal), a segunda unidade (endereço não localizado) e a mentoria "Fisio Mentora" (lançamento não confirmado).
- Duas fotos do carrossel da Criodermys trazem palavras da campanha dela impressas na arte (consulta/antes-depois) — são as fotos oficiais publicadas por ela; as demais imagens do site são limpas (recortes sem o texto das artes).

## Checagens feitas na construção
- ffprobe: áudio AAC presente nos 9 reels; o slide animado da Criodermys é mudo por natureza (arte animada) e roda mudo no carrossel
- Interações testadas em jsdom (33 asserções): intro, menu mobile, abas das etapas do método, carrossel (setas/pontos/swipe/wrap), linha do tempo, montador de mensagem, players abrindo com som (controls + muted=false), hero em autoplay mudo (atributos HTML), zero base64, zero WhatsApp/telefone no texto, fatos sem duplicação (preço, endereço, horário, kg e promessa 1× cada)
- Contraste calculado: 9 pares texto×fundo, todos WCAG AA (pior caso 6,75:1 — kickers rosé-escuro sobre porcelana)
- Todas as 18 referências de mídia do HTML resolvem para arquivos do pacote; pacote total ~58 MB, maior arquivo 15 MB (abaixo do limite de 25 MB do upload web do GitHub)
