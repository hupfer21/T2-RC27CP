# Trabalho 2: Integração de habilidades - 2022/1
**Disciplina: Redes de Computadores**

**Curso: Engenharia de Computação / Elétrica**

**Nome/RA: Gustavo Hupfer Martins / 2157365**


## Tarefa 1:  Sub-Redes
| Sub- Rede |             IPv6 - Sub-Rede            |  IPv4 - Sub-Rede  |  IPv4 - Máscara   | IPv4 - Broadcast  |    
|:---------:|:--------------------------------------:|:-----------------:|:-----------------:|:-----------------:|
| Matriz    | 2001:DB8:ACAD:4100::/64 | 200.200.65.0   | 255.255.255.192 | 200.200.65.63  |
| Filial 1  | 2001:DB8:ACAD:4101::/64 | 200.200.65.64  | 255.255.255.224 | 200.200.65.95  |
| Filial 2  | 2001:DB8:ACAD:4102::/64 | 200.200.65.96  | 255.255.255.224 | 200.200.65.127 |
| Filial 3  | 2001:DB8:ACAD:4103::/64 | 200.200.65.128 | 255.255.255.224 | 200.200.65.159 |
| Filial 4  | 2001:DB8:ACAD:4104::/64 | 200.200.65.160 | 255.255.255.224 | 200.200.65.192 |
| Filial 5  | 2001:DB8:ACAD:4105::/64 | 200.200.65.192 | 255.255.255.224 | 200.200.65.223 |
| pb-vit    | 2001:DB8:ACAD:41FF::0:0/112 | 200.200.65.224 | 255.255.255.252 | 200.200.65.227 |
| vit-fb    | 2001:DB8:ACAD:41FF::1:0/112 | 200.200.65.228 | 255.255.255.252 | 200.200.65.231 |
| fb-ita    | 2001:DB8:ACAD:41FF::2:0/112 | 200.200.65.232 | 255.255.255.252 | 200.200.65.235 |
| ita-pb    | 2001:DB8:ACAD:41FF::3:0/112 | 200.200.65.236 | 255.255.255.252 | 200.200.65.239 |
| cv-ita    | 2001:DB8:ACAD:41FF::4:0/112  | 200.200.65.240 | 255.255.255.252 | 200.200.65.243 |


## Tarefa 2: Endereçamento de Dispositivos
| Dispositivo           |Interface|      IPv4     |  IPv4 - Máscara |IPv4 - Gateway|      IPv6/Prefixo (GUA)     | IPv6 (LLA) |IPv6-Gateway|
|:-----------------------:|:---------:|---------------|-----------------|--------------|-----------------------------|------------|---------|
| PC1                   | NIC     | 200.200.65.3   | 255.255.255.192 | 200.200.65.1  | 2001:DB8:ACAD:4100::3/64    |   EUI-64   | FE80::1 |
| PC2                   | NIC     | 200.200.65.4   | 255.255.255.192 | 200.200.65.1  | 2001:DB8:ACAD:4100::4/64    |   EUI-64   | FE80::1 |
| PC3                   | NIC     | 200.200.65.67  | 255.255.255.224 | 200.200.65.65 | 2001:DB8:ACAD:4101::3/64    |   EUI-64   | FE80::1 |
| PC4                   | NIC     | 200.200.65.68  | 255.255.255.224 | 200.200.65.65 | 2001:DB8:ACAD:4101::4/64    |   EUI-64   | FE80::1 |
| PC5                   | NIC     | 200.200.65.99  | 255.255.255.224 | 200.200.65.97 | 2001:DB8:ACAD:4102::3/64    |   EUI-64   | FE80::1 |
| PC6                   | NIC     | 200.200.65.100 | 255.255.255.224 | 200.200.65.97 | 2001:DB8:ACAD:4102::4/64    |   EUI-64   | FE80::1 |
| Switch-Matriz         | SVI     | 200.200.65.2   | 255.255.255.192 | 200.200.65.1  |             -               |     -      |    -    |
| Switch-Filial1        | SVI     | 200.200.65.66  | 255.255.255.224 | 200.200.65.65 |             -               |     -      |    -    |
| Switch-Filial2        | SVI     | 200.200.65.98  | 255.255.255.224 | 200.200.65.97 |             -               |     -      |    -    |
| Roteador-Pato Branco  | Fa0/0   | 200.200.65.1   | 255.255.255.192 |      -       | 2001:DB8:ACAD:4100::1/64    |   FE80::1  |    -    |
| Roteador-Pato Branco  | Se0/0/0 | 200.200.65.225 | 255.255.255.252 |      -       | 2001:DB8:ACAD:41FF::0:1/112 |   EUI-64   |    -    |
| Roteador-Pato Branco  | Se0/0/1 | 200.200.65.238 | 255.255.255.252 |      -       | 2001:DB8:ACAD:41FF::3:2/112 |   EUI-64   |    -    |
| Roteador-Fco. Beltrão | Fa0/0   | 200.200.65.65  | 255.255.255.224 |      -       | 2001:DB8:ACAD:4101::1/64    |   FE80::1  |    -    |
| Roteador-Fco. Beltrão | Se0/0/0 | 200.200.65.233 | 255.255.255.252 |      -       | 2001:DB8:ACAD:41FF::2:1/112 |   EUI-64   |    -    |
| Roteador-Fco. Beltrão | Se0/0/1 | 200.200.65.230 | 255.255.255.252 |      -       | 2001:DB8:ACAD:41FF::1:2/112 |   EUI-64   |    -    | 
| Roteador-Vitorino     | Se0/0/0 | 200.200.65.229 | 255.255.255.252 |      -       | 2001:DB8:ACAD:41FF::1:1/112 |   EUI-64   |    -    | 
| Roteador-Vitorino     | Se0/0/1 | 200.200.65.226 | 255.255.255.252 |      -       | 2001:DB8:ACAD:41FF::0:2/112 |   EUI-64   |    -    | 
| Roteador-Itapejara    | Se0/0/0 | 200.200.65.237 | 255.255.255.252 |      -       | 2001:DB8:ACAD:41FF::3:1/112 |   EUI-64   |    -    | 
| Roteador-Itapejara    | Se0/0/1 | 200.200.65.234 | 255.255.255.252 |      -       | 2001:DB8:ACAD:41FF::2:2/112 |   EUI-64   |    -    | 
| Roteador-Itapejara    | Fa0/1   | 200.200.65.241 | 255.255.255.252 |      -       | 2001:DB8:ACAD:41FF::4:1/112 |   EUI-64   |    -    | 
| Roteador-Coronel      | Fa0/0   | 200.200.65.97  | 255.255.255.224 |      -       | 2001:DB8:ACAD:4102::1/64    |   FE80::1  |    -    |
| Roteador-Coronel      | Fa0/1   | 200.200.65.242 | 255.255.255.252 |      -       | 2001:DB8:ACAD:41FF::4:2/112 |   EUI-64   |    -    | 

## Tarefa 3: Tabela de Roteamento
#### IPv4

### Roteador Pato Branco
| Rede de Destino | Máscara | Next Hop | Interface de Saída |
|-----------------|---------|----------|--------------------|
| 200.200.65.64  | 255.255.255.224 | 200.200.65.226 | Se0/0/0 | 
| 200.200.65.228 | 255.255.255.252 | 200.200.65.226 | Se0/0/0 | 
| 200.200.65.232 | 255.255.255.252 | 200.200.65.226 | Se0/0/0 | 
| 200.200.65.240 | 255.255.255.252 | 200.200.65.226 | Se0/0/0 | 
| 200.200.65.96  | 255.255.255.224 | 200.200.65.226 | Se0/0/0 |

#### Roteador Francisco Beltrão
| Rede de Destino | Máscara | Next Hop | Interface de Saída |
|-----------------|---------|----------|--------------------|
| 200.200.65.0   | 255.255.255.192 | 200.200.65.234 | Se0/0/0 | 
| 200.200.65.224 | 255.255.255.252 | 200.200.65.234 | Se0/0/0 | 
| 200.200.65.236 | 255.255.255.252 | 200.200.65.234 | Se0/0/0 | 
| 200.200.65.240 | 255.255.255.252 | 200.200.65.234 | Se0/0/0 | 
| 200.200.65.96  | 255.255.255.224 | 200.200.65.234 | Se0/0/0 |

#### Roteador Vitorino
| Rede de Destino | Máscara | Next Hop | Interface de Saída |
|-----------------|---------|----------|--------------------|
| 200.200.65.0   | 255.255.255.192 | 200.200.65.230 | Se0/0/0 | 
| 200.200.65.64  | 255.255.255.224 | 200.200.65.230 | Se0/0/0 | 
| 200.200.65.232 | 255.255.255.252 | 200.200.65.230 | Se0/0/0 | 
| 200.200.65.236 | 255.255.255.252 | 200.200.65.230 | Se0/0/0 | 
| 200.200.65.96  | 255.255.255.224 | 200.200.65.230 | Se0/0/0 | 
| 200.200.65.240 | 255.255.255.252 | 200.200.65.230 | Se0/0/0 |

#### Roteador Itapejara D'Oeste
| Rede de Destino | Máscara | Next Hop | Interface de Saída |
|-----------------|---------|----------|--------------------|
| 200.200.65.0   | 255.255.255.192 | 200.200.65.238 | Se0/0/0 | 
| 200.200.65.64  | 255.255.255.224 | 200.200.65.238 | Se0/0/0 | 
| 200.200.65.224 | 255.255.255.252 | 200.200.65.238 | Se0/0/0 | 
| 200.200.65.228 | 255.255.255.252 | 200.200.65.238 | Se0/0/0 | 
| 200.200.65.96  | 255.255.255.224 | 200.200.65.242 | Fa0/1 | 

#### Roteador Coronel Vivida
| Rede de Destino | Máscara | Next Hop | Interface de Saída |
|-----------------|---------|----------|--------------------|
| 200.200.65.0   | 255.255.255.192 | 200.200.65.241 |  Fa0/1  | 
| 200.200.65.64  | 255.255.255.224 | 200.200.65.241 |  Fa0/1  | 
| 200.200.65.224 | 255.255.255.252 | 200.200.65.241 |  Fa0/1  | 
| 200.200.65.228 | 255.255.255.252 | 200.200.65.241 |  Fa0/1  | 
| 200.200.65.232 | 255.255.255.252 | 200.200.65.241 |  Fa0/1  | 
| 200.200.65.236 | 255.255.255.252 | 200.200.65.241 |  Fa0/1  | 


### IPv6
#### Roteador Pato Branco
| Rede de Destino/Prefixo      | Next Hop      | Interface de Saída |
|------------------------------|---------------|--------------------|
| 2001:0DB8:ACAD:4101::/64     | 2001:0DB8:ACAD:41FF::0:2 | Se0/0/0 |
| 2001:0DB8:ACAD:4102::/64     | 2001:0DB8:ACAD:41FF::0:2 | Se0/0/0 |
| 2001:0DB8:ACAD:41FF::1:0/112 | 2001:0DB8:ACAD:41FF::0:2 | Se0/0/0 |
| 2001:0DB8:ACAD:41FF::2:0/112 | 2001:0DB8:ACAD:41FF::0:2 | Se0/0/0 |
| 2001:0DB8:ACAD:41FF::4:0/112 | 2001:0DB8:ACAD:41FF::0:2 | Se0/0/0 |
      
#### Roteador Francisco Beltrão
| Rede de Destino/Prefixo      | Next Hop      | Interface de Saída |
|------------------------------|---------------|--------------------|   
| 2001:0DB8:ACAD:4100::/64     | 2001:0DB8:ACAD:41FF::2:2 | Se0/0/0 |
| 2001:0DB8:ACAD:4102::/64     | 2001:0DB8:ACAD:41FF::2:2 | Se0/0/0 |
| 2001:0DB8:ACAD:41FF::0:0/112 | 2001:0DB8:ACAD:41FF::2:2 | Se0/0/0 |
| 2001:0DB8:ACAD:41FF::3:0/112 | 2001:0DB8:ACAD:41FF::2:2 | Se0/0/0 |
| 2001:0DB8:ACAD:41FF::4:0/112 | 2001:0DB8:ACAD:41FF::2:2 | Se0/0/0 |
      
#### Roteador Vitorino
| Rede de Destino/Prefixo      | Next Hop      | Interface de Saída |
|------------------------------|---------------|--------------------|
| 2001:0DB8:ACAD:4100::/64     | 2001:0DB8:ACAD:41FF::1:2 | Se0/0/0 |
| 2001:0DB8:ACAD:4101::/64     | 2001:0DB8:ACAD:41FF::1:2 | Se0/0/0 |
| 2001:0DB8:ACAD:4102::/64     | 2001:0DB8:ACAD:41FF::1:2 | Se0/0/0 |
| 2001:0DB8:ACAD:41FF::2:0/112 | 2001:0DB8:ACAD:41FF::1:2 | Se0/0/0 |
| 2001:0DB8:ACAD:41FF::3:0/112 | 2001:0DB8:ACAD:41FF::1:2 | Se0/0/0 |
| 2001:0DB8:ACAD:41FF::4:0/112 | 2001:0DB8:ACAD:41FF::1:2 | Se0/0/0 |
      
#### Roteador Itapejara D'Oeste
| Rede de Destino/Prefixo      | Next Hop      | Interface de Saída |
|------------------------------|---------------|--------------------|
| 2001:0DB8:ACAD4100::/64     | 2001:0DB8:ACAD:41FF::3:2 | Se0/0/0 |
| 2001:0DB8:ACAD:4101::/64     | 2001:0DB8:ACAD:41FF::3:2 | Se0/0/0 |
| 2001:0DB8:ACAD:4102::/64     | 2001:0DB8:ACAD:41FF::4:2 | Fa0/1   |
| 2001:0DB8:ACAD:41FF::0:0/112 | 2001:0DB8:ACAD:41FF::3:2 | Se0/0/0 |
| 2001:0DB8:ACAD:41FF::1:0/112 | 2001:0DB8:ACAD:41FF::3:2 | Se0/0/0 |
      
#### Roteador Coronel Vivida
| Rede de Destino/Prefixo      | Next Hop      | Interface de Saída |
|------------------------------|---------------|--------------------|
| 2001:0DB8:ACAD:4100::/64     | 2001:0DB8:ACAD:41FF::4:1 | Fa0/1   |
| 2001:0DB8:ACAD:4101::/64     | 2001:0DB8:ACAD:41FF::4:1 | Fa0/1   |
| 2001:0DB8:ACAD:41FF::0:0/112 | 2001:0DB8:ACAD:41FF::4:1 | Fa0/1   |
| 2001:0DB8:ACAD:41FF::1:0/112 | 2001:0DB8:ACAD:41FF::4:1 | Fa0/1   |
| 2001:0DB8:ACAD:41FF::2:0/112 | 2001:0DB8:ACAD:41FF::4:1 | Fa0/1   |
| 2001:0DB8:ACAD:41FF::3:0/112 | 2001:0DB8:ACAD:41FF::4:1 | Fa0/1   |

## Topologia - Packet Tracer
- [ ] ![Trabalho2-Topologia-NomeAluno](trabalho2-topologia-gustavohupfer.pkt)


## Arquivos de Configuração dos Dispositivos Intermediários (roteadores e switches)
- [ ] ![Roteador Pato Branco](r-pb-gh.txt)
- [ ] ![Roteador Francisco Beltrão](r-fb-gh.txt)
- [ ] ![Roteador Vitorino](r-vit-gh.txt)
- [ ] ![Roteador Itapejara D'Oeste](r-ita-gh.txt)
- [ ] ![Roteador Coronel Vivida](r-cv-gh.txt)
- [ ] ![Switch Pato Branco](sw-matriz-gh.txt)
- [ ] ![Switch Francisco Beltrão](sw-filial1-gh.txt)
- [ ] ![Switch Coronel Vivida](sw-filial2-gh.txt)
