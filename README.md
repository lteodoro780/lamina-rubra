# Lamina Rubra

Motor novo, escrito do zero, para rodar o jogo J2ME *God of War: Betrayal* (Glu Mobile, 2007) no PC e no Android, com os arquivos
originais do jogo que **você já tem**. Tem dois modos:

- **Clássico**: 240×320, com o comportamento e a interface do celular.
- **Remaster**: tela larga em 1080p, interface nova, movimentos novos (esquiva, corrida, contra-ataque) e modo difícil.

> **O Lamina Rubra não traz o jogo.** Nenhum gráfico, som, texto ou mapa do jogo vem junto. Para jogar, você precisa do arquivo
> `.jar` original do jogo (MIDlet versão 1.4.8). O motor lê esse arquivo na hora de jogar e não o envia para lugar nenhum.

## Baixar

Na página de [releases](../../releases/latest):

| arquivo | para | precisa |
|---|---|---|
| `lamina-rubra-1.0.0.zip` | PC (Linux e Windows) | Java 21 ([adoptium.net](https://adoptium.net/)) |
| `lamina-rubra-1.0.0-linux-x64.tar.gz` | Linux | nada (Java embutido) |
| `lamina-rubra-1.0.0.apk` | Android 7.0 ou mais novo | — |

## PC

1. Extraia o arquivo baixado.
2. Rode, informando o `.jar` do jogo:
   - Linux (zip): `bin/lamina-rubra /caminho/do/gow.jar`
   - Linux (tar.gz com Java embutido): `lamina-rubra/bin/lamina-rubra /caminho/do/gow.jar`
   - Windows: `bin\lamina-rubra.bat C:\caminho\do\gow.jar`
3. Para não digitar o caminho toda vez, crie `~/.config/gow-motor/gow-motor.properties` (no Windows,
   `C:\Users\<você>\.config\gow-motor\gow-motor.properties`) com a linha `jar=/caminho/do/gow.jar`. O arquivo
   `gow-motor.properties.exemplo` do pacote mostra as outras opções.

O save e a configuração ficam em `~/.config/gow-motor/`.

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

1. Instale o `.apk` (permita instalar de fontes desconhecidas, se o aparelho pedir).
2. Na primeira abertura, toque em **Escolher o arquivo .jar** e escolha o `.jar` do jogo. Ele é copiado para a pasta privada do app; das
   próximas vezes o jogo abre direto. Para trocar de `.jar`, limpe os dados do app nas configurações do Android.
3. Controles de toque: direcional à esquerda; **PULAR**, **ATACAR**, **AGIR** e **ARMA** à direita; **BLOQ.** e **ESQUIVA** acima deles;
   **EVOL.** e **PAUSA** no alto. O botão voltar do Android pausa e volta nos menus.

Limitações desta versão no Android: a música MIDI do original não toca (o Android não tem sintetizador MIDI) e o APK ainda não foi
testado num aparelho de verdade. Relatos de problema são bem-vindos nas [issues](../../issues).

## Aviso legal

Lamina Rubra é um projeto de fãs, sem fins lucrativos e sem nenhuma ligação com a Sony Interactive Entertainment, o Santa Monica Studio
ou a Glu Mobile. *God of War* é marca dos seus donos; o nome aparece aqui só para dizer com qual jogo o motor é compatível. O motor foi
escrito do zero e não contém código, gráficos, sons, textos nem mapas do jogo. Use somente uma cópia do jogo que você tenha obtido
legalmente.
