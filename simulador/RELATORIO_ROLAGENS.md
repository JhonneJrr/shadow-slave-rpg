# Relatório de Rolagens e Equilíbrio — Shadow Slave RPG (regras v2)

*Simulador em `sim/ssrpg/` · probabilidades exatas por enumeração · Monte Carlo com 10.000 combates por cenário (976 cenários) · **padrão = regras v2** já aplicadas nos Livros 1–4; a coluna "v1" reproduz as regras antigas para comparação.*

## Resumo em 1 minuto

- **Testes ficaram jogáveis:** a CD Moderada agora é 7. Um novato passa em média em **31%** das 12 Subcategorias na CD 7 (antes, na Moderada 9: **8%**, e impossível em 9 de 12).
- **Combates ficaram menos letais sem ficar triviais:** 4 novatos contra os encontros escalados vencem **99%** (v1: 96%) e alguém cai em **18%** (v1: 38%). Contra os encontros como estão no livro (feitos para 7), vencem **84%** (v1: 64%); por isso o Livro 3 agora tem o **Orçamento de Ameaça**.
- **Rank acima virou rampa, não parede:** 4 novatos contra UMA criatura Desperta vencem em média **47%** (v1: 12%). Demônios e Diabos Despertos continuam quase invencíveis para novatos.
- **Teste extra do Jhonne:** 4 Adormecidos **saturados** (Marco 10, Memórias, 2 Ecos) vencem a ficha comum do Demônio Desperto em **100%**. Com o **Perfil de Chefe** agora nos livros (CD 11, 2× PV, +1 de Dano), a briga direta vence **22%**; com plano tático + Relógio de Preparação, **94%** (−1 CD) a **91%** (−1 alvo). O Derrubar revisado passou de 2% para 55% contra esse chefe (seção 7).

## 1. Regras v2 aplicadas (resumo exato para repassar)

### 1.1 Escala de CDs de tarefa (Livro 1 §1.3)

| Dificuldade | CD v2 | CD v1 |
| :--- | :--- | :--- |
| Trivial | **3** | 5 |
| Fácil | **5** | 7 |
| Moderada (padrão) | **7** | 9 |
| Difícil | **9** | 11 |
| Extrema | **11** | 13 |
| Divina | **13** | 15 |

- CDs intermediárias para ajuste fino: **4, 6, 8, 10, 12**. **CD mínima: 3.**
- Toda CD **fixa de teste** dos livros (perícia, sobrevivência, ofício, ambiente) caiu **2 pontos**. Exemplos: primeiros socorros e estabilizar **CD 7** (**9** sem kit); Culinária **CD 5 + 1 por Rank** do ingrediente acima do cozinheiro; Iniciativa/CD de Reação **CD 7 ± 1 por Rank** (**9** contra inimigos muito velozes); Choque de Vontades **CD 7 ± 1 por Rank**; perseguição **CD 7 ± 1 por Rank**.
- **CDs de criatura não mudam** (CD da ficha = CD de combate contra o próprio Rank): Adormecida **6–8**, Desperta **9–10**, Caída **10–11**, Corrompida **12**, Grande **13+**. CDs de efeitos dentro das fichas do Bestiário também ficam como estão.
- **CD Estática de NPC / Percepção da presa / Fintar:** `7 + Pilar (ou Astúcia) relevante ± 1 por Rank`.

### 1.2 Diferença de Rank (Livro 1 §1.3)

- **±1 na CD por Rank de diferença** (antes ±2), sempre com mínimo 3.
| Situação | CD da ficha | CD v2 | CD v1 |
| :--- | :--- | :--- | :--- |
| Adormecido contra criatura Desperta | 9 | **10** | 11 |
| Adormecido contra criatura Caída | 10 | **12** | 14 |
| Adormecido contra criatura Corrompida | 12 | **15** | 18 |
| Desperto contra criatura Adormecida | 7 | **6** | 5 (mínimo) |
| Ascendido contra criatura Adormecida | 7 | **5** | 5 (mínimo) |

### 1.3 Orçamento de Ameaça (Livro 3, antes da Regra dos 5 Segundos)

- **Ameaça de uma criatura** = `nº de jogadores que ela ataca por rodada × Dano por alvo` (Dano normal da ficha; enxames e matilhas: 1 alvo por indivíduo; Dano de Alma conta igual; quem só prende/controla conta 0).
- **Ameaça do encontro** = soma de todas as criaturas que agem na rodada. **Regra: Ameaça ≤ 1 × nº de jogadores.**
| Jogadores | 3 | 4 | 5 | 6 | 7 |
| :--- | :--- | :--- | :--- | :--- | :--- |
| Orçamento | 3 | 4 | 5 | 6 | 7 |

- Acima do Orçamento: retire lacaios, reduza alvos do chefe, divida em ondas ou ofereça gargalo/cobertura/emboscada.
- **Criatura de Rank acima num encontro acima do Orçamento → ⚠️ Fuga/Evitar.** Criatura **2+ Ranks acima → sempre Fuga/Evitar.** Mesmo Rank acima do Orçamento → marcado **⚖️ Acima do Orçamento** (dividir em ondas).
- Matrizes do Livro 3 e as 10 tabelas `1d6` de encontros do Livro 4 foram marcadas com essas tags (Livro 4: Coorte de referência por região, mesa de 7).

### 1.4 PV (Livro 1 §2.1 e §6.1)

- **PV Máximo = (2 × Corpo) + 4** (antes +2), +1 nos Marcos 2 e 6, +1 por Núcleo Divino extra (+2 no 7º).
| Corpo | 1 | 2 | 3 | 4 | 5 |
| :--- | :--- | :--- | :--- | :--- | :--- |
| PV v2 | 6 | 8 | 10 | 12 | 14 |
| PV v1 | 4 | 6 | 8 | 10 | 12 |

### 1.5 Sombras e Ecos (Livro 1 §7.5 G; Livro 2 cap. 8)

- **Sombra Evolutiva sobe de Rank: +2 na CD e +1 de Dano Base** (antes +1 CD). A rolagem continua `1d6 + ⌊CD/2⌋`, então +2 de CD = +1 na rolagem.
- **Eco reforjado** continua **+1 CD e +4 PV** por reforja (teste de reforja `Alma [Canalizar]` **CD 9**, Relógio 4).
- As 12 fichas de Sombra do Livro 2 cap. 8 mostram a trilha como `CD X (Eco Y)`.

### 1.5b Regras da 2ª rodada (aprovadas e aplicadas)

- **Perfil de Chefe** (Livro 3 §5.2): Demônio ou Diabo **Desperto** como chefe contra Coorte **Adormecida**: **CD 11** na ficha (12 na mesa, pelo `+1` por Rank), **PV × 2** (Demônio da Matriz 28, Diabo 36), **Dano +1** por alvo, mesmos alvos e habilidades. Aplicado a 6 fichas do Bestiário do L3 e às matrizes do L4 (Centurião da Carapaça, Troll de Casca Vermelha, Salamandra Ígnea).
- **Relógio de Preparação** (Livro 1 §1.7; guia do Mestre no Livro 3 §5.1): **4 segmentos**, sempre ao lado de um **Relógio de Ameaça** de 4. Completo = **1 Vantagem de Plano**: *Fraqueza Estudada* (−1 na CD da criatura na cena), *Terreno Escolhido* (−1 alvo por rodada, mínimo 1) ou *Emboscada Garantida* (Rodada de Surpresa sem teste). Máximo **1 por criatura de Rank acima**.
- **Derrubar** (Livro 1 §5.3): CD de Defesa (+1 se quadrúpede ou Grande), **dano normal da arma** (+2 no Crítico) e *Derrubado*. A criatura derrubada **gasta a Ação Maior para se levantar** (não ataca nessa rodada) e fica **Firme** até o fim da rodada seguinte. Personagens continuam levantando com metade do Movimento.
- **CDs do L4 alinhadas ao Bestiário do L3:** Centurião da Carapaça 11 → 10; Aranhas de Ferro 10 → 9.

### 1.6 Esclarecimentos aprovados junto

- **CD Exata na Defesa:** você **não sofre dano**, mas paga **1 Infortúnio** (padrão: **I1 Guarda Aberta**: Desvantagem na sua próxima Defesa).
- **Mariposa Devoradora de Sonhos:** **1 Dano de Alma** por alvo (texto alinhado à linha de stats) e cura **1 PV por alvo drenado**.
- **Esqueleto da Legião Imortal:** remonta **uma vez** (com 3 PV no turno seguinte); **fogo, esmagamento ou Crítico** impedem a remontagem.

### 1.7 Antes × depois (números do simulador)

| Encontro | Jog. | Versão | Ameaça / Orçamento | Vitória v1 → v2 | Alguém cai v1 → v2 | Grupo todo cai v1 → v2 | Rodadas (v2, vitórias) |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| E1 | 4 | livro (7) | 3 / 4 (ok) | 100% → **100%** | 1% → **0%** | 0% → **0%** | 3,0 |
| E1 | 4 | escalado | 3 / 4 (ok) | 100% → **100%** | 1% → **0%** | 0% → **0%** | 3,0 |
| E1 | 3 | livro (7) | 3 / 3 (ok) | 100% → **100%** | 0% → **0%** | 0% → **0%** | 3,9 |
| E1 | 3 | escalado | 2 / 3 (ok) | 100% → **100%** | 0% → **0%** | 0% → **0%** | 3,1 |
| E2 | 4 | livro (7) | 6 / 4 (⚖️ acima) | 54% → **81%** | 94% → **74%** | 46% → **19%** | 5,3 |
| E2 | 4 | escalado | 6 / 4 (⚖️ acima) | 80% → **95%** | 79% → **47%** | 20% → **5%** | 4,3 |
| E2 | 3 | livro (7) | 6 / 3 (⚖️ acima) | 29% → **50%** | 91% → **77%** | 71% → **50%** | 5,6 |
| E2 | 3 | escalado | 6 / 3 (⚖️ acima) | 87% → **95%** | 33% → **16%** | 13% → **5%** | 3,7 |
| E3 | 4 | livro (7) | 8 / 4 (⚖️ acima) | 46% → **84%** | 98% → **89%** | 54% → **16%** | 8,2 |
| E3 | 4 | escalado | 5 / 4 (⚖️ acima) | 99% → **100%** | 62% → **30%** | 1% → **0%** | 4,7 |
| E3 | 3 | livro (7) | 8 / 3 (⚖️ acima) | 19% → **46%** | 98% → **91%** | 81% → **54%** | 9,9 |
| E3 | 3 | escalado | 4 / 3 (⚖️ acima) | 98% → **100%** | 28% → **13%** | 2% → **0%** | 5,0 |
| E4 | 4 | livro (7) | 6 / 4 (⚖️ acima) | 51% → **88%** | 96% → **76%** | 48% → **10%** | 10,5 |
| E4 | 4 | escalado | 3 / 4 (ok) | 100% → **100%** | 11% → **1%** | 0% → **0%** | 5,0 |
| E4 | 3 | livro (7) | 6 / 3 (⚖️ acima) | 15% → **42%** | 97% → **85%** | 85% → **56%** | 12,2 |
| E4 | 3 | escalado | 2 / 3 (ok) | 100% → **100%** | 0% → **0%** | 0% → **0%** | 4,6 |
| E5 | 4 | livro (7) | 16 / 4 (⚠️ Fuga/Evitar) | 0% → **0%** | 100% → **100%** | 100% → **100%** | — |
| E5 | 4 | escalado | 10 / 4 (⚠️ Fuga/Evitar) | 0% → **0%** | 100% → **100%** | 100% → **100%** | 6,4 |
| E5 | 3 | livro (7) | 16 / 3 (⚠️ Fuga/Evitar) | 0% → **0%** | 100% → **100%** | 100% → **100%** | — |
| E5 | 3 | escalado | 8 / 3 (⚠️ Fuga/Evitar) | 0% → **0%** | 100% → **100%** | 100% → **100%** | 5,2 |
| E6 | 4 | livro (7) | 11 / 4 (⚖️ acima) | 7% → **34%** | 100% → **99%** | 93% → **66%** | 9,5 |
| E6 | 4 | escalado | 8 / 4 (⚖️ acima) | 90% → **99%** | 87% → **47%** | 10% → **1%** | 5,4 |
| E6 | 3 | livro (7) | 11 / 3 (⚖️ acima) | 1% → **5%** | 100% → **100%** | 99% → **94%** | 11,2 |
| E6 | 3 | escalado | 7 / 3 (⚖️ acima) | 92% → **99%** | 51% → **20%** | 8% → **1%** | 5,6 |
| E7 | 4 | livro (7) | 6 / 4 (⚖️ acima) | 100% → **100%** | 40% → **8%** | 0% → **0%** | 5,0 |
| E7 | 4 | escalado | 3 / 4 (ok) | 100% → **100%** | 1% → **0%** | 0% → **0%** | 3,0 |
| E7 | 3 | livro (7) | 6 / 3 (⚖️ acima) | 99% → **100%** | 25% → **5%** | 1% → **0%** | 6,5 |
| E7 | 3 | escalado | 2 / 3 (ok) | 100% → **100%** | 0% → **0%** | 0% → **0%** | 3,1 |
| E8 | 4 | livro (7) | 7 / 4 (⚖️ acima) | 89% → **99%** | 86% → **57%** | 11% → **1%** | 6,4 |
| E8 | 4 | escalado | 4 / 4 (ok) | 100% → **100%** | 23% → **4%** | 0% → **0%** | 3,1 |
| E8 | 3 | livro (7) | 7 / 3 (⚖️ acima) | 59% → **87%** | 84% → **60%** | 41% → **13%** | 8,2 |
| E8 | 3 | escalado | 4 / 3 (⚖️ acima) | 100% → **100%** | 4% → **1%** | 0% → **0%** | 3,1 |

Encontros: **E1** Pântano dos Sinos — Ato 1 (L3 §3.5 A (Roteiro Pronto 1)); **E2** Pântano dos Sinos — Ato 4 (Sanguessuga-Sino) (L3 §3.5 A (Roteiro Pronto 1)); **E3** Alcateia das Ruínas (L3 §4.3 Matriz A 8–9); **E4** Emboscada Noturna da Maré (L3 §4.3 Matriz A 3–4); **E5** Patrulha da Carapaça (L3 §4.3 Matriz A 5–6); **E6** Caçadores do Céu (L3 §4.3 Matriz B 3–4); **E7** Encontro Rápido (modelo) (L3 §5.1 Modelo 1); **E8** Encontro Tático (modelo) (L3 §5.1 Modelo 2 + Matriz §5.2).

![quedas v1 x v2](graficos/06_ajustes_quedas.png)

## 2. Probabilidades exatas dos graus

Tabela completa em `resultados/probabilidades_graus.csv`. O resultado depende só de **Pilar + bônus**.

![chance de sucesso](graficos/01_chance_sucesso_heatmap.png)

### 1d6: chance de Total ≥ CD (Normal / Vantagem / Desvantagem)

| Pilar+bônus | CD 3 | CD 5 | CD 7 | CD 9 | CD 11 | CD 13 |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| +1 | 83 / 97 / 69 | 50 / 75 / 25 | 17 / 31 / 3 | 0 / 0 / 0 | 0 / 0 / 0 | 0 / 0 / 0 |
| +2 | 100 / 100 / 100 | 67 / 89 / 44 | 33 / 56 / 11 | 0 / 0 / 0 | 0 / 0 / 0 | 0 / 0 / 0 |
| +3 | 100 / 100 / 100 | 83 / 97 / 69 | 50 / 75 / 25 | 17 / 31 / 3 | 0 / 0 / 0 | 0 / 0 / 0 |
| +4 | 100 / 100 / 100 | 100 / 100 / 100 | 67 / 89 / 44 | 33 / 56 / 11 | 0 / 0 / 0 | 0 / 0 / 0 |
| +5 | 100 / 100 / 100 | 100 / 100 / 100 | 83 / 97 / 69 | 50 / 75 / 25 | 17 / 31 / 3 | 0 / 0 / 0 |
| +6 | 100 / 100 / 100 | 100 / 100 / 100 | 100 / 100 / 100 | 67 / 89 / 44 | 33 / 56 / 11 | 0 / 0 / 0 |

### 1d8: chance de Total ≥ CD (Normal / Vantagem / Desvantagem)

| Pilar+bônus | CD 3 | CD 5 | CD 7 | CD 9 | CD 11 | CD 13 |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| +1 | 88 / 98 / 77 | 62 / 86 / 39 | 38 / 61 / 14 | 12 / 23 / 2 | 0 / 0 / 0 | 0 / 0 / 0 |
| +2 | 100 / 100 / 100 | 75 / 94 / 56 | 50 / 75 / 25 | 25 / 44 / 6 | 0 / 0 / 0 | 0 / 0 / 0 |
| +3 | 100 / 100 / 100 | 88 / 98 / 77 | 62 / 86 / 39 | 38 / 61 / 14 | 12 / 23 / 2 | 0 / 0 / 0 |
| +4 | 100 / 100 / 100 | 100 / 100 / 100 | 75 / 94 / 56 | 50 / 75 / 25 | 25 / 44 / 6 | 0 / 0 / 0 |
| +5 | 100 / 100 / 100 | 100 / 100 / 100 | 88 / 98 / 77 | 62 / 86 / 39 | 38 / 61 / 14 | 12 / 23 / 2 |
| +6 | 100 / 100 / 100 | 100 / 100 / 100 | 100 / 100 / 100 | 75 / 94 / 56 | 50 / 75 / 25 | 25 / 44 / 6 |

### Distribuição dos 6 graus em casos típicos (rolagem normal)

| Caso | Falha c/ Infortúnio | Falha Simples | Falha c/ Dádiva | Sucesso c/ Custo | Sucesso Pleno | Sucesso Crítico | Máx. Natural |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 1d8+3 vs CD 5 | 0,0% | 0,0% | 12,5% | 12,5% | 37,5% | 37,5% | 12,5% |
| 1d8+3 vs CD 7 | 0,0% | 25,0% | 12,5% | 12,5% | 37,5% | 12,5% | 12,5% |
| 1d8+3 vs CD 9 | 25,0% | 25,0% | 12,5% | 12,5% | 25,0% | 0,0% | 12,5% |
| 1d8+3 vs CD 10 | 37,5% | 25,0% | 12,5% | 12,5% | 12,5% | 0,0% | 12,5% |
| 1d8+2 vs CD 7 | 12,5% | 25,0% | 12,5% | 12,5% | 37,5% | 0,0% | 12,5% |
| 1d6+3 vs CD 7 | 0,0% | 33,3% | 16,7% | 16,7% | 33,3% | 0,0% | 16,7% |
| 1d6+1 vs CD 5 | 0,0% | 33,3% | 16,7% | 16,7% | 33,3% | 0,0% | 16,7% |
| 1d6+1 vs CD 7 | 33,3% | 33,3% | 16,7% | 16,7% | 0,0% | 0,0% | 16,7% |

![graus](graficos/02_graus_empilhados.png)

### Chance de sucesso de cada ficha de novato nas 12 Subcategorias (escala v2)

| Ficha (Livro 2 §1.1) | CD 3 Trivial | CD 5 Fácil | CD 7 Moderada | CD 9 Difícil | CD 11 Extrema | CD 13 Divina |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Baluarte (Dorian) | 92% (impossível em 0/12) | 63% (impossível em 0/12) | 31% (impossível em 0/12) | 8% (impossível em 9/12) | 2% (impossível em 10/12) | 0% (impossível em 12/12) |
| Executor | 92% (impossível em 0/12) | 63% (impossível em 0/12) | 30% (impossível em 0/12) | 6% (impossível em 9/12) | 1% (impossível em 11/12) | 0% (impossível em 12/12) |
| Olho de Falcão | 92% (impossível em 0/12) | 64% (impossível em 0/12) | 33% (impossível em 0/12) | 10% (impossível em 8/12) | 2% (impossível em 10/12) | 0% (impossível em 12/12) |
| Canalizador | 92% (impossível em 0/12) | 63% (impossível em 0/12) | 31% (impossível em 0/12) | 8% (impossível em 9/12) | 2% (impossível em 10/12) | 0% (impossível em 12/12) |

- Na v1, a Moderada era a CD 9: a coluna "CD 9" acima é o "antes" do teste padrão.
- CD 13 (Divina) continua impossível no `1d6` sem bônus e exige `1d8 + Pilar 3 + bônus 2` ou mais; é o teto planejado.

## 3. Novato sozinho contra cada criatura

![solo](graficos/03_solo_vitoria.png)

| Criatura | CD contra Adormecido | Baluarte (Dorian) | Executor | Olho de Falcão | Canalizador |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1. Larva do Pesadelo | Adormecida CD 6 | 100% → **100%** | 100% → **100%** | 100% → **100%** | 100% → **100%** |
| 2. Carniçal das Ruínas | Adormecida CD 7 | 100% → **100%** | 100% → **100%** | 87% → **97%** | 92% → **99%** |
| 3. Carniçal Alfa | Adormecida CD 8 | 68% → **83%** | 57% → **74%** | 2% → **5%** | 4% → **15%** |
| 4. Saqueador da Carapaça | Adormecida CD 8 | 79% → **87%** | 81% → **90%** | 4% → **8%** | 15% → **31%** |
| 5. Escavador de Coral | Adormecida CD 8 | 96% → **99%** | 96% → **99%** | 22% → **43%** | 36% → **72%** |
| 6. Aranha de Ferro | Adormecida CD 8 | 96% → **99%** | 96% → **99%** | 23% → **43%** | 36% → **71%** |
| 7. Afogado do Mar Amaldiçoado | Adormecida CD 8 | 96% → **99%** | 96% → **99%** | 23% → **43%** | 36% → **70%** |
| 8. Vespa Carmesim | Adormecida CD 8 | 99% → **100%** | 97% → **99%** | 72% → **86%** | 77% → **93%** |
| 9. Harpia de Penas de Bronze | Adormecida CD 8 | 96% → **99%** | 96% → **99%** | 22% → **42%** | 37% → **71%** |
| 10. Boneco de Porcelana | Adormecida CD 8 | 26% → **43%** | 18% → **35%** | 0% → **0%** | 0% → **0%** |
| 11. Lobo das Sombras Profundas | Desperta CD 9 → 10 | 0% → **1%** | 1% → **3%** | 0% → **0%** | 0% → **0%** |
| 12. Verme da Podridão Cinzenta | Desperta CD 9 → 10 | 0% → **0%** | 0% → **0%** | 0% → **0%** | 0% → **0%** |
| 13. Centurião da Carapaça | Desperta CD 10 → 11 | 0% → **0%** | 0% → **0%** | 0% → **0%** | 0% → **0%** |
| 14. Gárgula da Névoa Branca | Desperta CD 10 → 11 | 0% → **0%** | 0% → **0%** | 0% → **0%** | 0% → **0%** |
| 15. Esqueleto da Legião Imortal | Desperta CD 9 → 10 | 0% → **0%** | 0% → **2%** | 0% → **0%** | 0% → **0%** |
| 16. Sereia dos Sussurros | Desperta CD 10 → 11 | 0% → **0%** | 0% → **0%** | 0% → **0%** | 0% → **0%** |
| 17. Salamandra de Magma | Desperta CD 9 → 10 | 0% → **0%** | 0% → **1%** | 0% → **0%** | 0% → **0%** |
| 18. Besta de Espelho | Desperta CD 10 → 11 | 0% → **0%** | 0% → **0%** | 0% → **0%** | 0% → **0%** |
| 19. Mariposa Devoradora de Sonhos | Desperta CD 10 → 11 | 0% → **0%** | 0% → **0%** | 0% → **0%** | 0% → **0%** |
| 20. Flor Carnívora Gigante | Desperta CD 9 → 10 | 0% → **0%** | 0% → **0%** | 0% → **0%** | 0% → **0%** |

Vitória 1 contra 1, v1 → v2. Lutar sozinho contra uma criatura Desperta continua uma péssima ideia, como na obra.

## 4. 4 novatos contra UMA criatura Desperta do Bestiário

![desperta](graficos/07_grupo_vs_desperta.png)

| Criatura | v1 | v2 se o Rank ainda desse +2 | v2 | alguém cai (v2) |
| :--- | :--- | :--- | :--- | :--- |
| Lobo das Sombras Profundas | 88% | 97% | **100%** | 6% |
| Verme da Podridão Cinzenta | 7% | 19% | **64%** | 77% |
| Centurião da Carapaça | 0% | 0% | **4%** | 100% |
| Gárgula da Névoa Branca | 1% | 4% | **43%** | 85% |
| Esqueleto da Legião Imortal | 0% | 94% | **100%** | 9% |
| Sereia dos Sussurros | 0% | 0% | **3%** | 100% |
| Salamandra de Magma | 23% | 47% | **91%** | 43% |
| Besta de Espelho | 1% | 4% | **43%** | 85% |
| Mariposa Devoradora de Sonhos | 0% | 0% | **0%** | 100% |
| Flor Carnívora Gigante | 0% | 2% | **21%** | 99% |

O Esqueleto passou de 0% para quase 100% por causa da remontagem limitada; a Mariposa continua a 0% (4 alvos de Dano de Alma + cura).

## 5. Orçamento de Ameaça e Sombras

![orçamento](graficos/05_orcamento_vs_queda.png)

Dentro do Orçamento (Ameaça ≤ nº de jogadores), alguém cai em menos de 5% dos combates escalados. Acima de ~2× o Orçamento, alguém cai na maioria das lutas.

![sombras](graficos/08_sombras_por_rank.png)

| Regra | Rank da Sombra | CD | Rolagem | CD das criaturas do Rank | Chance de Total ≥ CD |
| :--- | :--- | :--- | :--- | :--- | :--- |
| v1 (+1 CD) | Desperta | 10 | 1d6+5 | 9–10 | 42% |
| v1 (+1 CD) | Ascendida/Caída | 11 | 1d6+5 | 10–11 | 25% |
| v1 (+1 CD) | Transcendente/Corrompida | 12 | 1d6+6 | 12–12 | 17% |
| v1 (+1 CD) | Suprema/Grande | 13 | 1d6+6 | 13–14 | 0% |
| **v2 (+2 CD)** | Desperta | 10 | 1d6+5 | 9–10 | 42% |
| **v2 (+2 CD)** | Ascendida/Caída | 12 | 1d6+6 | 10–11 | 42% |
| **v2 (+2 CD)** | Transcendente/Corrompida | 14 | 1d6+7 | 12–12 | 33% |
| **v2 (+2 CD)** | Suprema/Grande | 16 | 1d6+8 | 13–14 | 25% |

## 6. Teste extra (A): 4 Adormecidos contra 1 Desperto de cada Classe

**Como as fichas foram montadas** (`sim/extra.py`):

- **Novatos:** as 4 fichas recomendadas do Livro 2 §1.1 (Baluarte, Executor, Olho de Falcão, Canalizador), PV v2, sem Memórias nem Ecos.
- **Adormecidos saturados (Marco 10, Aspecto comum):** Pilar principal **4** (Marco 10), PV `2×Corpo + 4 + 2` (Marcos 2 e 6), Essência +5 (Marcos ímpares), 2 Atributos (Marcos 4 e 8). **Suposições:** arma de Memória com runa `+1` e 1 Atributo de `+1` no ataque (Canalizador: só `+1`, porque ataca com o Aspecto), 1 Atributo de `+1` na Defesa (Baluarte soma o escudo), armadura de Memória Tier I (2 níveis). Ecos: o Baluarte tem um **Eco Saqueador da Carapaça** e o Olho de Falcão um **Eco Lobo das Cinzas** (Tabela 7-4: CD 8, `1d6 + 4`, 5–6 PV, Dano 1), agindo com a Ação Menor do dono.
- **Regras de Rank aplicadas:** CD +1 por Rank; Memória Adormecida contra alvo Desperto (Tabela 7-1): arma com −1 na rolagem e armadura gastando 2 níveis por ponto de dano.
- **Criaturas:** faixa Desperta da Matriz Rank × Classe (L3 §5.2): Besta CD 9, 6 PV, Dano 2, 1 alvo; Monstro CD 9, 10 PV, Dano 2, 2 alvos; Demônio CD 10, 14 PV, Dano 2, 3 alvos (foca o mais frágil); Diabo CD 10, 18 PV, Dano 2, 3 alvos (foca o mais frágil). Mais 4 fichas do Bestiário como conferência.

| Criatura Desperta | 4 novatos | 4 saturados sem Ecos | 4 saturados + 2 Ecos |
| :--- | :--- | :--- | :--- |
| Besta Desperta (Matriz) | **100%** · cai 2% | **100%** · cai 0% | **100%** · cai 0% |
| Monstro Desperto (Matriz) | **96%** · cai 35% | **100%** · cai 0% | **100%** · cai 0% |
| Demônio Desperto (Matriz) | **8%** · cai 100% | **100%** · cai 29% | **100%** · cai 0% |
| Diabo Desperto (Matriz) | **1%** · cai 100% | **99%** · cai 65% | **100%** · cai 3% |
| Lobo das Sombras Profundas (nº 11) | **100%** · cai 5% | **100%** · cai 0% | **100%** · cai 0% |
| Gárgula da Névoa Branca (nº 14) | **38%** · cai 98% | **100%** · cai 15% | **100%** · cai 0% |
| Centurião da Carapaça (nº 13) | **4%** · cai 100% | **98%** · cai 60% | **100%** · cai 1% |
| Sereia dos Sussurros (nº 16) | **55%** · cai 88% | **100%** · cai 1% | **100%** · cai 0% |

"cai" = combates em que pelo menos um jogador chegou a 0 PV.

**Leitura:** para novatos, Besta e Monstro Despertos são vencíveis; Demônio e Diabo são paredes (como pede a obra). Para Adormecidos saturados, **qualquer criatura Desperta da Matriz cai em 3–4 rodadas**, quase sem ninguém cair. O salto vem do Pilar 4 + bônus de Memória, que com flanqueamento estoura o Cap +3 e vira **Vantagem em quase todo ataque**, e dos Ecos, que dão mais ataques e mais alvos para a criatura dividir.

## 7. Teste extra (B): saturados contra um Demônio Desperto, briga direta × estratégia

**Regras v2 usadas aqui (todas já nos livros):** Perfil de Chefe (L3 §5.2), Relógio de Preparação (L1 §1.7) e Derrubar revisado (L1 §5.3: dano normal, a criatura gasta a Ação Maior para se levantar e fica Firme 1 rodada; CD `+1` se quadrúpede/Grande — o simulador aplica o `+1`).

**Estratégias modeladas:**

- **Emboscada** (L1 §3.2): Vanguarda contra `7 + Astúcia da presa + 1` (Demônio da Matriz: 10; Perfil de Chefe: 11). "Coletivo" = 3 rolam e a maioria precisa passar; "líder" = o melhor rola com `+2` de Ajuda. Sucesso = Rodada de Surpresa com Vantagem; o Olho de Falcão faz **Ataque Furtivo**.
- **Runas-armadilha** (L1 Runas 6 e 8): Mina Ígnea (2 de Dano + Derrubado) e Dardo de Relâmpago (2 de Dano + Atordoado).
- **Posição Elevada:** +1 nos ataques à distância. **Gargalo:** a criatura alcança 1 alvo a menos por rodada (decisão do Mestre).
- **Mirar em Ponto Fraco** (Executor, CD +2): no Pleno/Crítico, +1/+2 de Dano e destrói uma parte (−1 alvo e fim da carapaça).
- **Derrubar** (Baluarte, regra nova e antiga), **Proteger Aliado**, **Ajuda Tática** dos Ecos.
- **Relógio de Preparação completo:** 1 Vantagem de Plano (*Fraqueza Estudada* −1 CD, *Terreno Escolhido* −1 alvo ou *Emboscada Garantida*).

### Saturados (4 + 2 Ecos)

| Estratégia | Demônio Desperto da Matriz (CD 10 → 11, 14 PV, Dano 2, 3 alvos) | Demônio Desperto em Perfil de Chefe (CD 11 → 12, 28 PV, Dano 3, 3 alvos) | Diabo Desperto em Perfil de Chefe (CD 11 → 12, 36 PV, Dano 3, 3 alvos) |
| :--- | :--- | :--- | :--- |
| briga direta | **100%** · cai 0% · 0,0 | **22%** · cai 100% · 2,2 | **5%** · cai 100% · 2,4 |
| emboscada, teste coletivo da Vanguarda (+ Ataque Furtivo) | **100%** · cai 0% · 0,0 | **22%** · cai 100% · 2,2 | **5%** · cai 100% · 2,4 |
| emboscada, líder + 2 ajudantes (+ Ataque Furtivo) | **100%** · cai 0% · 0,0 | **35%** · cai 100% · 2,0 | **11%** · cai 100% · 2,3 |
| 1 Runa de Mina Ígnea | **100%** · cai 0% · 0,0 | **60%** · cai 99% · 1,8 | **26%** · cai 100% · 2,2 |
| Mina Ígnea + Dardo de Relâmpago | **100%** · cai 0% · 0,0 | **72%** · cai 98% · 1,7 | **37%** · cai 100% · 2,1 |
| Posição Elevada (+1 à distância) | **100%** · cai 0% · 0,0 | **26%** · cai 100% · 2,2 | **9%** · cai 100% · 2,4 |
| gargalo (−1 alvo da criatura) | **100%** · cai 0% · 0,0 | **76%** · cai 100% · 2,2 | **38%** · cai 100% · 2,4 |
| Mirar em Ponto Fraco (Executor) | **100%** · cai 1% · 0,0 | **51%** · cai 100% · 2,2 | **22%** · cai 100% · 2,4 |
| Derrubar (Baluarte), regra antiga | **100%** · cai 2% · 0,0 | **2%** · cai 100% · 2,2 | **0%** · cai 100% · 2,2 |
| Derrubar (Baluarte), regra nova | **100%** · cai 0% · 0,0 | **55%** · cai 99% · 1,6 | **30%** · cai 100% · 1,9 |
| Proteger Aliado (Baluarte) | **100%** · cai 0% · 0,0 | **29%** · cai 93% · 1,6 | **10%** · cai 99% · 2,0 |
| Ecos dão Ajuda +1 em vez de atacar | **100%** · cai 0% · 0,0 | **30%** · cai 100% · 2,2 | **9%** · cai 100% · 2,4 |
| plano tático (emboscada líder + furtivo + Posição Elevada + Proteger) | **100%** · cai 0% · 0,0 | **47%** · cai 80% · 1,1 | **31%** · cai 91% · 1,5 |
| plano tático + Derrubar | **100%** · cai 0% · 0,0 | **73%** · cai 52% · 0,6 | **62%** · cai 64% · 0,8 |
| plano tático + gargalo | **100%** · cai 0% · 0,0 | **91%** · cai 61% · 1,0 | **80%** · cai 79% · 1,4 |
| plano completo (tático + gargalo + 2 runas) | **100%** · cai 0% · 0,0 | **99%** · cai 17% · 0,2 | **97%** · cai 34% · 0,5 |
| Relógio de Preparação: Fraqueza Estudada (−1 CD) | **100%** · cai 0% · 0,0 | **79%** · cai 100% · 1,8 | **56%** · cai 100% · 2,2 |
| Relógio de Preparação: Terreno Escolhido (−1 alvo) | **100%** · cai 0% · 0,0 | **76%** · cai 100% · 2,2 | **37%** · cai 100% · 2,4 |
| Relógio de Preparação: Emboscada Garantida | **100%** · cai 0% · 0,0 | **59%** · cai 99% · 1,8 | **24%** · cai 100% · 2,2 |
| plano tático + Fraqueza Estudada (−1 CD) | **100%** · cai 0% · 0,0 | **94%** · cai 33% · 0,5 | **90%** · cai 47% · 0,7 |
| plano tático + Terreno Escolhido (−1 alvo) | **100%** · cai 0% · 0,0 | **91%** · cai 61% · 1,0 | **81%** · cai 79% · 1,4 |
| plano tático + Emboscada Garantida | **100%** · cai 0% · 0,0 | **73%** · cai 59% · 0,8 | **52%** · cai 81% · 1,3 |
| (fora da regra) −2 na CD | **100%** · cai 0% · 0,0 | **100%** · cai 96% · 1,0 | **100%** · cai 100% · 1,2 |

Cada célula: **vitória** · combates em que alguém cai · média de jogadores caídos nas vitórias.

### Novatos (para comparação; ficha comum, sem Perfil de Chefe)

| Estratégia | Demônio Desperto da Matriz | Centurião da Carapaça |
| :--- | :--- | :--- |
| briga direta | **8%** · cai 100% | **4%** · cai 100% |
| emboscada, teste coletivo da Vanguarda (+ Ataque Furtivo) | **9%** · cai 100% | **4%** · cai 100% |
| emboscada, líder + 2 ajudantes (+ Ataque Furtivo) | **14%** · cai 98% | **9%** · cai 99% |
| 1 Runa de Mina Ígnea | **32%** · cai 93% | **22%** · cai 97% |
| Mina Ígnea + Dardo de Relâmpago | **49%** · cai 84% | **39%** · cai 89% |
| Posição Elevada (+1 à distância) | **18%** · cai 98% | **6%** · cai 100% |
| gargalo (−1 alvo da criatura) | **23%** · cai 100% | **18%** · cai 100% |
| Mirar em Ponto Fraco (Executor) | **0%** · cai 100% | **0%** · cai 100% |
| Derrubar (Baluarte), regra antiga | **2%** · cai 100% | **0%** · cai 100% |
| Derrubar (Baluarte), regra nova | **6%** · cai 99% | **4%** · cai 100% |
| Proteger Aliado (Baluarte) | **11%** · cai 96% | **4%** · cai 98% |
| plano tático (emboscada líder + furtivo + Posição Elevada + Proteger) | **36%** · cai 78% | **17%** · cai 90% |
| plano tático + Derrubar | **36%** · cai 77% | **17%** · cai 89% |
| plano tático + gargalo | **62%** · cai 69% | **38%** · cai 84% |
| plano completo (tático + gargalo + 2 runas) | **92%** · cai 22% | **82%** · cai 39% |
| Relógio de Preparação: Fraqueza Estudada (−1 CD) | **45%** · cai 97% | **23%** · cai 100% |
| Relógio de Preparação: Terreno Escolhido (−1 alvo) | **23%** · cai 100% | **17%** · cai 100% |
| Relógio de Preparação: Emboscada Garantida | **26%** · cai 96% | **17%** · cai 98% |
| plano tático + Fraqueza Estudada (−1 CD) | **79%** · cai 43% | **50%** · cai 68% |
| plano tático + Terreno Escolhido (−1 alvo) | **62%** · cai 69% | **38%** · cai 84% |
| plano tático + Emboscada Garantida | **58%** · cai 60% | **35%** · cai 76% |
| (fora da regra) −2 na CD | **90%** · cai 88% | **67%** · cai 98% |

### O sistema recompensa estratégia? Sim, e quanto

- **Demônio em Perfil de Chefe:** briga direta **22%** (grupo todo cai em 78%); com o Relógio de Preparação sozinho, **79%** (−1 CD); plano tático **47%**; plano tático + Relógio **94%** (−1 CD, alguém cai em 33%) ou **91%** (−1 alvo, alguém cai em 61%); plano completo **99%**.
- **Diabo em Perfil de Chefe:** briga direta **5%**, plano tático + Relógio (−1 CD) **90%**.
- **Derrubar revisado:** 2% → **55%** contra o Demônio chefe (novatos contra o Demônio da Matriz: 2% → 6%). Deixou de atrapalhar e virou uma tática boa, sem travar o monstro, porque ele fica Firme depois de levantar.
- Novatos contra o Demônio da Matriz: **8% → 92%** com o plano completo.
- **Ainda fraca:** *Mirar em Ponto Fraco* nas mãos de novatos (0%): a CD +2 tira o dano principal do Executor por várias rodadas. Sugestão para uma próxima rodada: o `+2` só vale para partes minúsculas; para juntas e olhos, `+1`.
- **Alvo do Jhonne atingido:** o Demônio Desperto em Perfil de Chefe é bizarramente forte na briga direta e vencível por um grupo saturado e preparado, quase sempre a um custo alto.

## 8. Pontos ainda em aberto

| Tema | Situação |
| :--- | :--- |
| Habilidades de Aspecto e Papel | Só o ataque básico é modelado; Técnicas de Papel e Habilidades com Essência ficaram de fora. |
| Condições especiais | Teias, agarrões e hipnose não modelados; veneno, frenesi, carapaças, bote, rebote, remontagem e cura da Mariposa sim. |
| Fichas saturadas | Bônus de Memória e Atributos são suposições típicas (ver seção 6); os livros não trazem uma ficha pronta de Marco 10. |
| Gargalo e Posição Elevada | Dependem do Mestre; o simulador usa −1 alvo e +1 à distância. |
| Escala para 3–4 jogadores | Agora coberta pelo Orçamento de Ameaça (Livro 3). |

## 9. Arquivos

- `sim/ssrpg/regras.py`, `sim/ssrpg/combate.py`, `sim/ssrpg/dados.py`: motor com as regras v2 como padrão (`VARIANTE_V1` reproduz as antigas).
- `sim/simular.py` (`./venv/bin/python simular.py --n 10000`, cerca de 1 min) e `sim/extra.py` (teste extra, cerca de 15 s).
- `sim/graficos.py`, `sim/gerar_relatorio.py`, `sim/testes_regras.py` (exemplos de mesa v2: Kael CD 10, Iris CD 8, PV 6/8/10/12/14).
- `sim/resultados/resultados.json`, `sim/resultados/extra.json`, `sim/resultados/probabilidades_graus.csv`, `sim/graficos/*.png`.
- Relatório v1 arquivado em `review/v2/RELATORIO_ROLAGENS_v1.md`; mudanças nos livros em `review/BALANCO_v2.md`.

