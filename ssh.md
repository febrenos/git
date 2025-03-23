### Para que serve?
- ter multiplos usuarios no github localmente

### Gerar e salvar a chave ssh
- criar uma pasta **.ssh** (ela ficará oculta e para vizualizar no finder aperte ```cmd+shif+.``` ou no cmd ```ls -la ~/.ssh```)
- ssh-keygen -t ed25519 -C "email_2@example.com" -f ~/.ssh/febrenos
- ssh-keygen -t ed25519 -C "email_2@example.com" -f ~/.ssh/fbaltran_meli
- Crie essa arquitetura fbaltran_meli, fbaltran_meli.pub, febrenos, febrenos.pub são gerados automaticamente pelo ssh 

```
.shh
├── config (gerenciamento dos git)
├── fbaltran_meli
├── fbaltran_meli.pub (arquivo com ssh para githuh)
├── febrenos
├── febrenos.pub (arquivo com ssh para githuh)
└── known_hosts
```

### Salvar a chave ssh no git hub
- Acessar o github desejado e ir em ```settings/SSH and GPG keys```
- clicar em **New SSH key**
- adicionar o conteúdo de **febrenos.pub** gerado pela ssh
- Realizar essas mesmas etapas para as proximas contas que for adicionar

### arquivo Config

```
Host github.com
Hostname ssh.github.com
Port 443
IdentityFile ~/.ssh/fbaltran_meli

Host p.github.com
Hostname ssh.github.com
Port 443
IdentityFile ~/.ssh/febrenos
```


### Como usar o git clone
- acessar o SSH para clonar ao invez do HTTPS
