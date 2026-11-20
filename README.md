# Lamina Rubra

Motor novo, escrito do zero, para rodar o jogo J2ME *God of War: Betrayal* (Glu Mobile, 2007) no PC e no Android, com os arquivos
originais do jogo que **você já tem**. Tem dois modos:

- **Clássico**: 240×320, com o comportamento e a interface do celular.
- **Remaster**: tela larga em 1080p, interface nova, fundos novos, som novo, vídeo de prólogo, movimentos novos (esquiva, corrida,
  contra-ataque) e modo difícil.

> **O Lamina Rubra não traz o jogo.** Nenhum gráfico, som, texto ou mapa do jogo vem junto. Para jogar, você precisa do arquivo
> `.jar` original do jogo (MIDlet versão 1.4.20, do Sony Ericsson K800i, ou 1.4.8). O motor lê esse arquivo na hora de jogar e não o envia para lugar nenhum.

## Baixar

Na página de [releases](../../releases/latest):

| arquivo | para | precisa |
|---|---|---|
| `lamina-rubra-1.0.3-windows-x64-setup.exe` | **Windows** (instalador) | nada (Java embutido) |
| `lamina-rubra-1.0.3-x86_64.AppImage` | **Linux** (um arquivo só) | nada (Java embutido) |
| `lamina-rubra-1.0.3.apk` | **Android** 7.0 ou mais novo | — |
| `lamina-rubra-1.0.3.zip` | PC (Linux e Windows) | Java 21 ([adoptium.net](https://adoptium.net/)) |
| `lamina-rubra-1.0.3-linux-x64.tar.gz` | Linux | nada (Java embutido) |

O remaster completo (interface, fundos, som e o vídeo do prólogo) já vem nos pacotes; o jogo abre nele.

## PC

- **Windows**: rode o instalador `.exe` (não pede administrador; cria atalhos no Menu Iniciar e na área de trabalho).
- **Linux**: marque o `.AppImage` como executável (`chmod +x` ou nas propriedades do arquivo) e abra com dois cliques.

Na primeira abertura, uma janela pede o `.jar` do jogo; ele é conferido (avisa se for de outra versão) e lembrado para as próximas
vezes. O jogo abre no remaster, em tela cheia 1080p (F11 alterna com janela).

Nos pacotes `.zip` e `.tar.gz`, o jogo abre por `bin/lamina-rubra` (Linux) ou `bin\lamina-rubra.bat` (Windows); o caminho do `.jar`
também pode vir na linha de comando (`bin/lamina-rubra /caminho/do/gow.jar`) ou como `jar=/caminho/do/gow.jar` em
`~/.config/gow-motor/gow-motor.properties` (no Windows, `C:\Users\<você>\.config\gow-motor\gow-motor.properties`). O arquivo
`gow-motor.properties.exemplo` do pacote mostra as outras opções.

O save, a configuração e os arquivos do remaster ficam em `~/.config/gow-motor/`.

### Controles no teclado (remaster)

| ação | tecla |
|---|---|
| andar, subir, descer | setas (ou WASD) |
| pular | Espaço |
| atacar (golpe, agarrar, magia) | J, X ou Enter |
| interagir (baú, alavanca, inimigo atordoado) | E |
| bloquear (segurado) | Shift |
| esquiva / corrida (segurando para a frente) | Ctrl |
| trocar de arma | Q |
| evolução | U |
| pausa / voltar | Esc |
| tela cheia | F11 |

Controle (gamepad) também funciona: A pula, X ataca, B interage, LT bloqueia, RT esquiva, RB troca a arma, Start pausa.

## Android

1. Instale o `.apk` (permita instalar de fontes desconhecidas, se o aparelho pedir). Se tiver a 1.0.0, desinstale-a antes; a 1.0.1
   atualiza direto.
2. Na primeira abertura, toque em **Escolher o arquivo .jar** e escolha o `.jar` do jogo. Ele é conferido (outra versão é avisada) e
   copiado para a pasta privada do app; das próximas vezes o jogo abre direto. Se o jogo não abrir com o arquivo escolhido, o app
   volta à tela de escolha mostrando o erro. Para trocar de `.jar`, limpe os dados do app nas configurações do Android.
3. Na primeira abertura o app também prepara os arquivos do remaster (alguns segundos). O vídeo do prólogo toca no reprodutor do
   Android; um toque o pula.
4. Controles de toque: direcional à esquerda; **PULAR**, **ATACAR**, **AGIR** e **ARMA** à direita; **BLOQ.** e **ESQUIVA** acima deles;
   **EVOL.** e **PAUSA** no alto. O botão voltar do Android pausa e volta nos menus.

Limitação desta versão: no Android, a música MIDI do modo clássico não toca (o Android não tem sintetizador MIDI). Relatos de
problema são bem-vindos nas [issues](../../issues).

## Aviso legal

Lamina Rubra é um projeto de fãs, sem fins lucrativos e sem nenhuma ligação com a Sony Interactive Entertainment, o Santa Monica Studio
ou a Glu Mobile. *God of War* é marca dos seus donos; o nome aparece aqui só para dizer com qual jogo o motor é compatível. O motor foi
escrito do zero e não contém código, gráficos, sons, textos nem mapas do jogo. Use somente uma cópia do jogo que você tenha obtido
legalmente.
