# Changelog da Revisão de Qualidade — Shadow Slave RPG (18/11/2026)

## Geral (os 4 livros)
- **Notação corrigida:** removidos todos os artefatos de LaTeX (`$\rightarrow$`, `$\leftrightarrow$`, `$$\text{…}$$`, `\times`, `\textbf`, `\longrightarrow`) e as setas/comparadores em ASCII (`->`, `>=`, `<=`). Agora aparecem →, ↔, ×, ≥ e ≤. As fórmulas viraram linhas em negrito legíveis, como **PV Iniciais = (2 × Corpo) + 2**.
- **Tabelas:** barras `|` dentro de código quebravam colunas (ex.: Tabela 9-2 do Livro 1). Foram trocadas por `·`.
- **Navegação:** os links `file:///C:/…` no fim dos livros foram trocados por uma tabela com links relativos para os 4 livros em HTML, os 4 PDFs e a Central.
- **Sumários:** as âncoras dos sumários clicáveis (Livros 1 e 3) foram consertadas, e todos os links internos agora funcionam.
- **Conteúdo conferido:** todas as contagens prometidas batem. Livro 1: 30 Dádivas + 30 Infortúnios, 15 Manobras, 15 Condições. Livro 2: 12 Origens, 28 Aspectos, 60 + 12 Atributos, 35 Encantamentos, 40 Memórias, 25 Atributos de Eco, 12 Ecos. Livro 3: 20 Perigos, 15 Armadilhas, Matrizes A–E, 60 Defeitos, 16 Inimigos Humanos, 32 Criaturas + 10 Chefes. Livro 4: 10 Regiões, 12 NPCs, 10 Relíquias, 20 Rumores. Não há TODOs nem seções vazias, e todas as referências cruzadas apontam para capítulos que existem.

## Livro 1 — Sistema
- Novo **Exemplo de Mesa** de Relógio de Progresso + Relógio de Ameaça + Coorte Unida (Seção 1.7).
- Novo **Exemplo de Mesa** de Primeiros Socorros e Regra das 24 Horas (Seção 6.2).
- Novo **Exemplo de Mesa** de Dupla Colheita e Marcos de Saturação, com o cálculo da Reserva (Seção 4.3).
- Corrigido: sequência de Ranks Humanos "→ Santo →" → "→ Transcendente →", alinhada ao restante do livro.
- Corrigido: exemplo confuso na tabela de rendimento de Estilhaços ("Besta Dormida? Não existe").
- Corrigida a marcação quebrada do exemplo de Soren (`*Evocar [X]`).
- Final do livro reescrito sem o link quebrado.

## Livro 2 — Jogador
- **Livro completado:** Aspectos 16–28, Parte C (Oficina Modular) e Capítulos 5–8, que faltavam no arquivo compilado. Eles vieram dos módulos L2_Parte3 e L2_Parte4.
- **Costuras da junção removidas:** o título solto "LIVRO 2 — PARTE 4" e o sumário duplicado foram retirados. "CAPÍTULO 4 (PARTES B E C)", "PARTE B" e "PARTE C" viraram subtítulos do Capítulo 4, então a hierarquia de títulos ficou correta.
- **Contradição corrigida:** a fórmula de Essência dos Aspectos Divinos usava termos diferentes dos do Livro 1. Foi unificada com a fórmula canônica: (Alma × 2) + Marcos Ímpares + Bônus de Rank + 3 × Núcleos Extras. O exemplo continua dando o mesmo resultado.
- Fechamento e navegação adicionados ao fim do livro.

## Livro 3 — Mestre
- **Livro completado:** o resto do Capítulo 4.3 (Matrizes C–E) e os Capítulos 5–8, vindos do módulo L3_Parte2.
- Nova seção **"Como Usar as Matrizes na Prática"**, com passo a passo e exemplo narrado (Seção 4.3).
- **Contradição corrigida:** XP por sessão era "2 a 3" e passou a "1 a 3", como no Livro 1, Seção 12.3.
- Fechamento e navegação adicionados ao fim do livro.

## Livro 4 — Lore e Cenário
- Novo **Exemplo de Mesa** de Reputação entre facções rivais, com dica de uso na mesa (Seção 3.8).
- Navegação final trocada por links relativos.

## Pacote de Ajustes de Aspectos e Chefes (18/11/2026)
- **Escravo das Sombras (Livro 2):** Manto das Sombras sem custo e sem dano ao portador, `+1` nas rolagens físicas e `+1` de Dano por Sombra. As Sombras só se somam depois do Despertar: `1` Sombra no Adormecido (`+1/+1`), `2` no Desperto (`+2/+2`). Manto em aliados só a partir do Rank Desperto (contradição entre a Seção 1.3 A e a 1ª Habilidade corrigida). Evolução de Sombra Evolutiva corrigida para `+2` na CD por Rank.
- **Aspectos Divinos (Livros 1, 2 e 3):** o 2º Núcleo Divino só condensa no Despertar, e não mais no Marco 10 do Adormecido.
- **Portadora da Luz (Livro 2):** a Chama da Alma acende com Ação Menor, sem custo, e dura a cena. Acesa, dá `+2` de Dano e `+2` nas rolagens físicas como Adormecida e `+3/+3` como Desperta, mais autocura de `1 PV` por rodada. A chama é visível: sem furtividade, e os inimigos a incluem entre os alvos. Na Manipulação Solar, o disparo pode somar o bônus da chama, mas a consome; com a chama apagada, a Reação só serve para reacendê-la.
- **Perfil de Chefe (Livros 0, 1, 3 e 4):** Demônio e Diabo Despertos contra Adormecidos passam de 2× para **3× PV** (Demônio da Matriz: 42; Diabo: 54). CD e Dano continuam os mesmos.

## Pacote de Controle e Aspectos Ofensivos (18/11/2026)
- **Controle (Livros 0, 1 e 3):** criatura Derrubada fica **Firme por 2 rodadas** depois de se levantar. Criatura de Rank acima só perde a Ação Maior na **1ª queda da cena**; nas seguintes, levanta com o Movimento. Criatura Atordoada também fica Firme por 2 rodadas e não pode ser Atordoada de novo nesse tempo.
- **Sangrando e Queimando em criaturas (Livros 0, 1 e 2):** duram **3 turnos da criatura**.
- **Alquimista da Peste (Livro 2):** Destilar Toxina reveste a arma **1 vez por cena** (2 acertos).
- **Devorador Carmesim (Livro 2):** as garras causam **1 de Dano (2 em CD + 3)**, como as da Besta Lunar.
- **Predador Silencioso (Livro 2):** Golpe na Jugular só contra alvo **surpreso ou cercado por 3 ou mais**, e dá só **+1 de Dano** (sem bônus na rolagem).
- **Perfil de Chefe (Livros 1 e 3):** chances atualizadas para o pacote completo: cerca de 1 em 4 na briga direta e 93% com plano.

## Condições em Inimigos (18/11/2026)
- **Livros 0, 1, 2 e 3:** as condições baixam a CD de um inimigo **no máximo `-1` no total**, mesmo com várias ao mesmo tempo. O **dano contínuo** (Sangrando, Queimando, toxinas) **soma normalmente**: cada efeito causa o seu dano no início do turno do inimigo.

## Mesas de 7 e Portadora da Luz em Postos altos (18/11/2026)
- **Perfil de Chefe por tamanho de mesa (Livros 0, 1, 3 e 4):** até 5 jogadores, o chefe continua com **3× PV**. Com **6 ou 7 jogadores**, ele usa **6× PV** e ataca **até 5 alvos** (Demônio `84 PV`, Diabo `108 PV`). Contra 6–7 Despertos, um chefe Caído fica com cerca de `120 PV`, até 5 alvos e Dano `5`. Tabela nova no Livro 3, Seção 5.2, e notas nas fichas do bestiário e nos chefes do Livro 4. Nas simulações com 7 jogadores, a briga direta vence em `~24%` e o plano em `~91%` (eram `23%`/`93%` com 4 jogadores).
- **Orçamento de Ameaça em mesas grandes (Livros 0, 3 e 4):** o teto continua sendo `1 ×` o número de jogadores. Novo aviso: com 6–7 jogadores, uma luta dentro do Orçamento fica fácil; para assustar, use uma 2ª onda ou um chefe no Perfil de 6× PV, sem aumentar o Dano.
- **Portadora da Luz (Livro 2):** a Chama da Alma passa a dar `+8 / +9 / +10 / +11 / +12` de Dano do `[3/7]` ao `[7/7]` (eram `+4` a `+8`). As rolagens continuam travadas em `+3`. Assim ela fica cerca de `1` de Dano por rodada acima do Escravo das Sombras do mesmo Posto.
- **Defeito da Portadora (Livros 2 e 3):** depois de 3 turnos seguidos de chama acesa, ela rola `Mente [Vontade] CD 7` a cada turno. Se falhar, sofre `-1` em **todas** as suas rolagens naquele turno, inclusive Defesa.
