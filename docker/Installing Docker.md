O Docker é instalado na máquina alvo, de onde iremos coletar os dados usando o Prometheus.
1. Um script shell é criado para automatizar a instalação do Docker na máquina e facilitar a reprodutibilidade.
2. O script é enviado para a máquina alvo

## Enviando o script para a máquina

`scp install_docker.sh user@remoteHost:/path/remote`

## Como executar o script

1. Salve o *script* em um arquivo, como: `install_docker.sh`.

2. Torne o *script* executável:

    `chmod +x install_docker.sh`

3. Execute o *script*:

    `./install_docker.sh`

## Permissões necessárias

- sudo: O *script* requer permissões de sudo para instalar pacotes e fazer alterações na configuração do sistema.

- Alterações no Grupo de Usuários: O *script* adiciona o usuário atual ao grupo docker. Esta alteração terá efeito após você sair e entrar novamente.