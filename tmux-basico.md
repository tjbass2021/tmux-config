# Comandos básicos do Tmux

> O Tmux é um multiplexador, permite que se manipule várias sessões e várias janelas no shell. Cada sessão pode conter múltiplas janelas separadas por abas ou organizadas lado a lado.

Para acionar o modo de comando do Tmux, utiliza-se a o comando mestre ^b (ctrl+b).

## Lista de comandos

### listar sessões
Para este comando, basta digitar no shell `tmux ls` que serão listadas todas as sessões em andamento.

### abrir nova janela
`^b - c`

**para navegar entre as janelas**
`^b - n` para ir para a próxima janela
`^b - p` para voltar à janela anterior

Na barra de status é possível identificar o índice das janelas (a partir do número 0), onde a janela atual está marcada com o asterisco (quando utilizado o tema padrão do tmux). Observado isso, outra maneira de alternar entre as janelas é utilizando o atalho `^b - [i]`, onde o `[i]` é o índice da janela qual você deseja acessar. 

### split de janelas

`^b - "` para dividir a janela horizontalmente
`^b - %` para dividir a janela verticalmente

### Dettached e Attached da sessão

Para sair de uma sessão do Tmux sem encerrá-la, fazemos o dettached com o atalho `^b - d`

Para retormar a sessão, utiliza-se o comando `tmux a -t [i]` - lembrando que `[i]` é o índice da sessão.

### renomeando a sessão e janela

`^b - $` para renomear a sessão
`^b - ,` para renomear a janela

> Note que após digitar o atalho, vai estar disponível na barra de status a edição dos respectivos nomes de acordo com os respectivos atalhos acionados

### Focando e retornando do foco em uma janela dividida

Quando utilizando o modo split de janelas, às vezes, por mais comodidade é preciso focara em uma janela, logo, para isso basta utilizar `^b - z`. E para retornar ao modo anterior de janelas divididas, basta repetir o atalho.

### Criando uma nova sessão

`tmux new -s [nome_sessao]`

#### listando sessões

`^b - w` lista as sessões, podendo escolher entre elas

#### listando janelas

`^b - s` lista as janelas, podendo escolher entre elas

#### criando uma nova sessão, mas sem entrar nela

`tmux new -s [nome_sessao] -d`

### finalizando uma sessão específica

`tmux kill-session -t [nome_sessao]`

### finalizando uma ou mais sessões de uma vez

`tmux kill-server`

### exibindo a hora

`^b - t`
