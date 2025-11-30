Simulando um Ataque de Brute Force de Senhas com Medusa e Kali Linux.


Neste desafio foi realizado a configuração do ambiente em duas VMs, sendo uma com o Kali Linux e outra com o Metasploitable. Ao iniciar as duas máquinas virtuais, foi feito uma identificação de IP no metasploitable em seguida criado as Wordlists que contém: usuários e senhas, utilizados no brute force.
Principais comandos utilizados: enum4linux, no qual identifica os usuários da máquina de destino, neste caso o Metasploitable. O resultado da enumeração foi salvo no arquivo "enum4.txt". Com os usuários prontos, foi criado uma Wordlist, com os usuários “smb_user.txt” em seguida, criado outra Wordlist com senhas fracas “senha.txt”. O objetivo de criar senhas fracas é para realizar um spray, onde é feito o brute force com a mesma senha em vários usuários.
Com as Wordlistas criadas, foi utilizado a medusa para realizar o ataque. medusa -h 192.168.192.128 -U smb_user.txt -P senha.txt -M smbnt -t 2 -T 50
Onde identificou-se um usuário e senha correto.

