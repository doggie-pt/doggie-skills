# SKILL: doggie_banner_factory_noflux

## Objetivo

Gerar automaticamente campanhas completas de banner para a loja Shopify da Doggie.

Esta skill funciona como um estúdio criativo de marketing, produzindo:

- conceito de campanha
- copy para banners
- prompts para geração de imagem por IA
- orientações de layout
- versões desktop e mobile
- variações A/B

O objetivo é criar hero banners para Shopify de alta conversão, consistentes com a identidade visual da Doggie.

---

# Contexto da Marca

Doggie é uma loja premium para animais de estimação localizada em Lisboa.

Público-alvo:

Proprietários de animais que:

- tratam os seus animais como família
- valorizam produtos de qualidade
- apreciam experiências premium
- estão dispostos a investir no bem-estar dos seus animais

A comunicação deve transmitir:

- calor humano
- confiança
- alegria
- ligação emocional com os animais

---

# Identidade Visual

Os banners devem seguir o estilo Doggie.

### Cores principais

Roxo
Rosa
Laranja

Aplicação típica:

- fundos em gradiente
- acentos com glow
- botões CTA com gradiente

---

# Tom Emocional

As cenas devem transmitir:

- felicidade
- celebração
- afeição entre donos e animais
- ambientes acolhedores
- momentos de brincadeira

Os animais devem parecer:

- expressivos
- saudáveis
- alegres
- amigáveis

---

# Estilo de Layout

Estrutura preferida:

Desktop:

ESQUERDA  
Imagem hero

DIREITA  
Conteúdo de texto

Mobile:

TOPO  
Headline

CENTRO  
Animais ou produto

FUNDO  
Botão CTA

---

# Tamanhos de Banner

## Desktop

1920 × 800 px

Zona segura de conteúdo:
1200 px central

Composição:
imagem à esquerda  
texto à direita

---

## Mobile

1080 × 1350 px

Composição:

texto centrado  
animais ou produto abaixo

---

# Parâmetros de Entrada

O utilizador pode fornecer:

Campanha (tipo)
Promoção
Produto
Cupão
Estação
Oferta
CTA

Exemplos:

Black Friday
Campanha de Natal
Aniversário da loja
Envio grátis
Lançamento de produto

---

# Estrutura de Saída

A skill deve devolver os seguintes blocos:

- Conceito de Campanha
- Copy do Banner (Headline, Subheadline, Oferta, CTA)
- Prompt de Imagem — Desktop
- Prompt de Imagem — Mobile
- Guia de Layout (posicionamento dos elementos)
- Variações A/B (pelo menos 2 alternativas)

---

# Banner Copy

Campos esperados:

Headline  
Subheadline  
Oferta  
CTA

Exemplo:

Headline
Um Natal cheio de mimo para o teu patudo

Subheadline
Presentes especiais para quem está sempre ao teu lado

Oferta
-10% em produtos selecionados

CTA
Ver presentes de Natal

---

# Prompt de Imagem — Desktop

Gere um prompt detalhado para geração de imagem contendo:

- cena
- iluminação
- animais (espécies / atitudes)
- composição (espaço negativo para texto quando necessário)
- cores (incluir acentos de marca: roxo/rosa/laranja)
- mood visual
- colocação do(s) produto(s)
- qualidade técnica (cinematic lighting, soft depth of field, high realism)

Exemplo de estrutura:

premium pet lifestyle scene, cozy living room with warm lights and soft textures, a joyful golden retriever interacting with owner, premium pet products artfully placed near the pet, purple-pink-[...]

---

# Prompt de Imagem — Mobile

Adaptar o prompt para composição vertical, com os animais/produto(s) centralizados e espaço superior para o headline.

Exemplo:

same premium pet lifestyle scene but vertical composition, pets centered, cozy background, space above for headline, purple-pink-orange glow accents, studio lighting, soft depth of field, ultra r[...]

---

# Guia de Layout

Descrever onde cada elemento deve aparecer na arte:

- Headline: posição (ex.: top right / top center)
- Subheadline: abaixo do headline
- Oferta: próxima ao texto principal, com destaque visual
- CTA button: posição e estilo (gradiente roxo→laranja, sombra suave, padding generoso)
- Imagem/Animais: lado esquerdo (desktop) ou centro (mobile)
- Zona segura: manter todo o texto dentro dos 1200 px centrais (desktop)

---

# Variações A/B

Gerar pelo menos duas variações que alterem o foco criativo:

Variação A: foco na emoção (ex.: momentos afetivos entre dono e animal)
Variação B: foco na oferta (ex.: destaque ao desconto / cupões)
Variação C (opcional): foco no produto (ex.: close-up do produto em uso)

Para cada variação, fornecer: conceito curto, headline alternativo, subheadline e CTA alternativos, e pequenas mudanças no prompt de imagem/layout.

---

# Estilo de CTA

Botões CTA devem usar:

gradiente roxo → laranja

Exemplos de textos de CTA:

Ver ofertas
Comprar agora
Descobrir coleção
Ver campanha

---

# Requisitos de Qualidade de Imagem

Todos os prompts devem incluir e reforçar as seguintes qualidades técnicas e visuais:

- cinematic lighting
- soft depth of field
- high realism
- expressive animals
- premium product placement
- brand color glow accents
- warm festive mood when relevant

Palavras-chave recomendadas:

premium pet lifestyle
festive atmosphere
cozy environment
studio lighting
clean composition
brand color gradients

---

# Padrão de Qualidade

As imagens geradas e os banners finais devem parecer:

- campanhas profissionais de e-commerce
- marcas premium para animais de estimação
- secções hero de homepage para Shopify

---

# Saída Final

A skill deve entregar, por campanha solicitada:

- Conceito de campanha (texto)
- Copy completo do banner (headline, subheadline, oferta, CTA)
- Prompt de imagem para Desktop (detalhado)
- Prompt de imagem para Mobile (detalhado)
- Guia de layout (instruções de posicionamento)
- 2–3 variações A/B prontas para teste
