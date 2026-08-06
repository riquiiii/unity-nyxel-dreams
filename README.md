# 🌙 Nyxel Dreams

[![Unity](https://img.shields.io/badge/Unity-2D_Engine-blue?logo=unity)](https://unity.com/)
[![C#](https://img.shields.io/badge/C%23-Language-purple?logo=c-sharp)](https://docs.microsoft.com/en-us/dotnet/csharp/)
[![Play Web](https://img.shields.io/badge/Play_Online-GitHub_Pages-brightgreen?logo=github)](https://riquiiii.github.io/unity-nyxel-dreams/)
[![Genre](https://img.shields.io/badge/Genre-2D_Platformer-orange)]()

> **Nyxel Dreams** é um jogo de plataforma 2D desenvolvido em **C#** na engine **Unity**, criado originalmente como Trabalho de Conclusão de Curso (TCC) do ensino médio no curso Técnico em Informática do Colégio Cruzeiro do Sul (2023).

---

## 🎮 Jogar no Navegador

O jogo está disponível para jogar diretamente no seu navegador através do GitHub Pages!

👉 **[Clique aqui para jogar o Nyxel Dreams via WebGL](https://riquiiii.github.io/unity-nyxel-dreams/)**

---

## 📖 Sobre o Projeto

O projeto conta com cerca de **10 fases** projetadas com progressão gradual de dificuldade, explorando diversas mecânicas de física, tempo e precisão.

---

## ✨ Funcionalidades e Mecânicas de Jogo

- **🎮 Controle Multiplataforma Adaptativo:**
  - Suporte completo a **Teclado e Controle (Gamepad)** no PC.
  - **Interface Touch On-Screen:** Botões virtuais na tela para movimentação e pulo em dispositivos móveis e telas portáteis (ocultos automaticamente na versão para computador).
- **🏃 Movimentação e Física do Jogador:**
  - Sistema de movimentação horizontal fluida.
  - Mecânica de **Pulo Duplo** (limitação de pulos controlada por física e estados de colisão com o solo).
- **⏳ Seções de Corrida Contra o Tempo (Blocos Caindo):**
  - Plataformas e blocos que despencam ao toque ou ao passar por baixo.
  - Trechos inteiros da fase compostos por blocos quebradiços que exigem agilidade extrema antes que a rota fique inacessível (a queda resulta em morte instantânea).
- **⚙️ Obstáculos e Armadilhas Dinâmicas:**
  - **Serras Giratórias Orbitais:** Serras que orbitam blocos específicos usando movimento circular.
  - **Serras e Espinhos Fixos:** Gatilhos de colisão que reiniciam o nível imediatamente ao contato.
  - **Trampolins:** Impulsionam o jogador a grandes alturas para alcançar áreas elevadas.
- **🏗️ Plataformas Móveis e Interativas:**
  - Plataformas com levitação vertical senoidal suave.
  - Plataformas com movimentação horizontal de translação.
- **⏸️ Sistema de Pausa:** Menu de pausa.

---

## 🎨 Arte e Sprites

- **Personagem Principal (Nyxel):** **Autoria própria** (design e animação em Pixel Art criados do zero para o jogo utilizando LibreSprite/Aseprite e mesa digitalizadora Wacom).
- **Cenários e Obstáculos:** Utilização de pacotes de sprites gratuitos da comunidade (*Pixel Adventure 1* e adicionais).

---

## ⚠️ Status do Projeto & Limitações Conhecidas

Por se tratar de um projeto acadêmico de TCC desenvolvido em prazo delimitado, o jogo possui algumas limitações técnicas e pequenos comportamentos inconsistentes dos quais temos total ciência:

- **Menu Principal:**
  - Os botões **"Opções"** e **"Sair"** possuem caráter meramente ilustrativo/decorativo nesta versão de demonstração.
  - O botão **"Sair"** é funcional apenas na versão executável compilada para desktop (`.exe`), visto que rodando no navegador (WebGL) não é permitido fechar a aba por restrições do próprio browser.
- **Hitbox de Obstáculos:** A *hitbox* de colisão dos espinhos é ligeiramente maior do que o sprite visual, exigindo maior precisão do jogador nos saltos.
- **Glitch Eventual de Pulo:** Em raras situações de colisão específica com quinas ou trocas rápidas de plataforma, pode ocorrer um comportamento atípico onde o jogo permite executar mais pulos do que o limite padrão establishedo (pulo duplo).
- **Versão Web (WebGL):** A compilação para o GitHub Pages pode apresentar pequenas variações no tempo de carregamento ou no áudio dependendo do navegador utilizado.

---

## 🛠️ Tecnologias e Ferramentas Utilizadas

| Categoria | Ferramenta / Recurso | Descrição |
|---|---|---|
| **Game Engine** | Unity 2D | Desenvolvimento da física, cenas, câmeras e build WebGL |
| **Linguagem** | C# (.NET) | Programação de scripts de movimentação, mecânicas e lógica |
| **IDE** | Visual Studio | Escrita e depuração de código |
| **Arte do Jogador** | LibreSprite / Aseprite | Design autoral e animação do personagem Nyxel |
| **Asset Pack (Ambiente)** | Pixel Adventure 1 | Tilesets e sprites gratuitos para cenários e armadilhas |
| **Trilha Sonora** | FL Studio | Composição de trilha sonora autoral Lo-Fi (80 BPM) |
| **Hardware de Arte** | Wacom CTL472 | Mesa digitalizadora para auxílio na criação dos cenários/artes |

---

## 📂 Estrutura de Scripts Principais (`/Assets/Scripts`)

- `Player.cs`: Controla movimentação horizontal, pulo, pulo duplo, inversão de sprite (*flip*) e transições do `Animator`.
- `Camera.cs`: Segue o jogador com suavização suave via `Vector3.SmoothDamp`.
- `LevitarPlataforma.cs`: Aplica oscilação vertical baseada na função senoidal (`Mathf.Sin`).
- `MovimentoPlataforma.cs`: Realiza o deslocamento horizontal de vaivém de plataformas.
- `blococaindo.cs`: Detecta a presença do jogador via `Trigger2D` e ativa a queda do bloco em direção ao abismo.
- `rotvolta.cs` & `roda.cs`: Calculam a rotação contínua e a trajetória orbital das serras giratórias em torno do cenário.
- `Trampolim.cs`: Aplica uma força vertical instantânea no `Rigidbody2D` do jogador.
- `Espinhos.cs`: Recarrega a cena atual via `SceneManager` ao colidir com o jogador.

## 👥 Créditos e Autoria

Projeto desenvolvido como Trabalho de Conclusão do Curso Técnico em Informática do **Colégio Cruzeiro do Sul** (São Paulo - 2023), sob orientação do **Prof. Ricardo Bonini de Oliveira**.

### Equipe de Desenvolvimento
- **Programação Principal & Level Design:** Henrique Araujo
- **Design de Personagem & Pixel Art (Nyxel):** Nicolas Ferreira
- **Desenvolvimento Colaborativo:** João Gabriel & Kauan Angelin

### Assets de Terceiros
- **Cenários, Tilesets e Armadilhas:** Pacote *Pixel Adventure 1* por *Pixel Frog* (Unity Asset Store)
