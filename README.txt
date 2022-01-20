Este playbook realiza a instação de todos os itens descritos na documentação de OnBoarding, disponível em: https://zenvia.atlassian.net/wiki/spaces/SRECPAAS/pages/2434072644/Onboarding

Com exceção dos seguintes componentes:
- KAF
- Govc
- Docker
- Docker-Compose
- kubectl

* Este playbook também não realizar importação de certificados, configuração de clusters e exportação de variavies.

Para sua utilizaçação siga os passos abaixo: 

Instalação do Ansible
$ sudo apt update
$ sudo apt install software-properties-common
$ sudo add-apt-repository --yes --update ppa:ansible/ansible
$ sudo apt install ansible


Modifique o ip do arquivo hosts
ip addr | grep eth0 <<< Para descobrir seu IP

Mofique o conteudo do arquivo "ansible_cfg.txt" localizado em /etc/ansible/ utilizando as informações do arquivo "ansible_cfg.txt.tmp. 

Dentro da pasta que contem o playbook rode o comando abaixo para realizar as instalações:

ansible-playbook -i hosts playbook-yml