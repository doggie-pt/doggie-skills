---
name: doggie-banner-factory
description: >
  Cria banners hero de alta conversão para a loja Shopify da Doggie (petshop premium de Lisboa)
  e para campanhas promocionais. Gera JSON pronto a importar no NanoBanana — APENAS fundo, animal
  e gradiente, com zona limpa reservada — e entrega à parte a copy (headline, subheadline, oferta, CTA)
  para overlay manual no Canva com as fontes reais da marca e o logo PNG real.
  Produz sempre versão desktop (1920×800) e mobile (1080×1350).

  ACIONAR quando o utilizador pedir: banner, banner Shopify, hero, banner de homepage, banner de campanha,
  arte de promoção para o site, banner desktop/mobile, banner de Black Friday/Natal/Verão/aniversário,
  banner de portes grátis, banner de lançamento de produto. Também: "cria um banner", "faz um hero",
  "gera o banner da campanha", "preciso de um banner para o site".

  NÃO usar para posts de Instagram/stories/reels — esses vão para o skill doggie-content-factory.
---

# Doggie Banner Factory

Banners hero para Shopify, em **duas camadas**:

1. **Camada IA (NanoBanana):** fundo + animal + gradiente da marca, com **zona limpa** reservada para o texto. Sem texto. Sem logo.
2. **Camada Canva (manual):** headline, subheadline, oferta, CTA e o **logo PNG real** por cima, com as fontes reais.

> **Porquê assim:** a IA não reproduz fielmente o logo Doggie nem tipografia de marca. Texto gerado por IA sai com erros, acentos partidos e fontes erradas. Por isso o texto e o logo entram sempre em pós-produção no Canva. Isto é regra, não preferência.

---

## 1. Referência da Marca

```
NOME:        Doggie — much more than a pet
LOJA ONLINE: store.doggie.pt  (ATIVA — linkar produtos/coleções reais)
LOJA FÍSICA: Av. Óscar Monteiro Torres 29C, 1000-215 Lisboa
CONTACTO:    +351 911 030 615 · info@doggie.pt
```

**Gradiente principal:** `#4B0C62 → #92278F → #DA1C5C → #EE2A7B → #F15A29`

| Cor | HEX | Uso |
|-----|-----|-----|
| Roxo profundo | `#4B0C62` | Âncora do gradiente, fundos escuros |
| Magenta | `#92278F` | Transição |
| Crimson | `#DA1C5C` | Acentos, botão CTA |
| Pink | `#EE2A7B` | Destaques |
| Laranja | `#F15A29` | Glow, sparkle ✦, energia |

**Tipografia (no Canva, não no prompt):**
- Headline → **Indigo Regular**
- Tagline / apoio → **Caviar Dreams**

**Mascote:** French Bulldog com óculos quadrados oversized. *Não pedir à IA para reproduzir o logo* — usar cães/gatos reais na fotografia e sobrepor o logo PNG depois.

---

## 2. O que vai no prompt vs. o que vai no Canva

| Vai no prompt NanoBanana | Vai no Canva (depois) |
|---|---|
| Fotografia do animal (cão, gato, etc.) | Headline (Indigo Regular) |
| Iluminação, cenário, mood | Subheadline (Caviar Dreams) |
| Gradiente da marca (glow/zona) | Oferta / badge de desconto |
| **Zona limpa** vazia para texto | Botão CTA |
| Profundidade, qualidade editorial | **Logo PNG real** |
| — | Código promocional |

❌ **Nunca no prompt:** texto, palavras, números, percentagens, logo, wordmark "doggie", tagline, watermark.

---

## 3. Tamanhos e zonas seguras

### Desktop — 1920×800
- Composição: **animal à esquerda, zona limpa à direita** para o texto.
- Zona de texto: terço direito (~640 px de largura útil).

### Mobile — 1080×1350
- Composição: **animal em baixo/centro, zona limpa em cima** para o texto.
- Zona de texto: terço superior.

Gerar **sempre os dois**.

---

## 4. JSON NanoBanana — estrutura de output

Parâmetros fixos: `model: flux-2-pro`, `steps: 44`, `guidance: 9.5`.
(Como **não há texto na imagem**, mantém-se 9.5 — não é preciso subir para 10.)

Acentos removidos das palavras PT dentro do `prompt` (mantidos só na copy do Canva).

```json
{
  "banner_desktop": {
    "model": "flux-2-pro",
    "steps": 44,
    "guidance": 9.5,
    "width": 1920,
    "height": 800,
    "aspect_ratio": "21:9",
    "prompt": "[fundo + animal + gradiente + ZONA LIMPA — ver secção 5]",
    "negative_prompt": "[ver secção 6]"
  },
  "banner_mobile": {
    "model": "flux-2-pro",
    "steps": 44,
    "guidance": 9.5,
    "width": 1080,
    "height": 1350,
    "aspect_ratio": "4:5",
    "prompt": "[mesma cena, composicao vertical, ZONA LIMPA em cima]",
    "negative_prompt": "[ver secção 6]"
  }
}
```

---

## 5. Template de prompt (sem texto, sem logo)

```
Premium pet brand hero banner background, [formato] composition.
[ANIMAL]: a [raca] [expressao: happy/relaxed/playful], [posicao no frame],
healthy and well-groomed, looking at camera, professional advertising photography.
[ILUMINACAO]: [ex: warm golden-hour side light / bright clean studio light].
[CENARIO]: [ex: soft Mediterranean summer garden bokeh / cozy living room blur].
[GRADIENTE]: brand gradient glow of deep purple, magenta and orange (#4B0C62, #92278F, #DA1C5C, #EE2A7B, #F15A29)
flowing softly across the [zona], luminous but subtle, not covering the animal.
[ZONA LIMPA]: large empty negative space on the [direita / topo] of the frame,
clean and uncluttered, reserved for text overlay, nothing in this area.
[QUALIDADE]: ultra realistic, cinematic, shallow depth of field, 8k,
award-winning advertising photography.
```

---

## 6. Negative prompt padrão

```
text, words, letters, numbers, percentages, captions, labels, watermark, logo,
wordmark, brand name, tagline, typography, poster layout, frame, border,
deformed animal, extra limbs, bad anatomy, ugly, blurry, low quality,
oversaturated, harsh shadows, cluttered background, busy composition,
people, human hands, cheap stock photo
```

---

## 7. Regras de copy (camada Canva, PT-PT)

- **Registo "tu"** sempre.
- **Proibido "patudo".** Usar: "o teu cão", "o teu gato", "o teu animal", "o teu companheiro".
- Copy curta, emocional, orientada ao benefício.
- **Regra legal "ATÉ":** em badges de desconto variável, "ATÉ" aparece sempre por cima da percentagem (ex: `ATÉ\n-50%`). Em desconto fixo (ex: -15%), não usar "ATÉ".
- **CTA padrão:** `COMPRAR AGORA` ou `APROVEITAR A PROMOÇÃO`.
- Botão CTA: fundo `#DA1C5C` ou gradiente roxo→laranja, texto branco.
- Se houver código promo, mostrar o código (ex: `VERAO15`) e validade.

### Exemplos de copy (já sem "patudo")
- Headline: `Um verão fresco para o teu cão`
- Subheadline: `Hidratação, snacks gelados e segurança em viagem`
- Oferta: `-15% com o código VERAO15`
- CTA: `APROVEITAR A PROMOÇÃO`

---

## 8. Estrutura de output (o que entregar sempre)

1. **Conceito da campanha** — 1-2 linhas da ideia criativa.
2. **Copy para o Canva** — headline, subheadline, oferta, CTA (PT-PT, regras da secção 7).
3. **JSON NanoBanana desktop** (1920×800).
4. **JSON NanoBanana mobile** (1080×1350).
5. **Guia de layout Canva** — onde fica cada elemento + cor do CTA + recordar logo PNG real na zona limpa.
6. **Variações A/B de copy:**
   - A — foco emoção
   - B — foco desconto/urgência

---

## 9. Checklist antes de entregar

- [ ] Prompt **não** contém texto, números nem logo
- [ ] `negative_prompt` exclui texto/logo/watermark
- [ ] Zona limpa reservada e indicada (direita no desktop, topo no mobile)
- [ ] `flux-2-pro`, steps 44, guidance 9.5
- [ ] Acentos removidos no prompt
- [ ] Copy em PT-PT, "tu", **sem "patudo"**
- [ ] Regra "ATÉ" aplicada se desconto variável
- [ ] Desktop **e** mobile gerados
- [ ] Guia Canva lembra logo PNG real + fontes Indigo/Caviar Dreams
