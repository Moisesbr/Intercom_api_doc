# Documentação API Interfone.

O Token para acesso a API é obtido na primeira pagina da console de configuração.

# Exemplo para leitura das entradas digitais:

```
curl -X POST http://192.168.0.102:9000/get_inputs -F token=af87241285fe416668ecc050c17385bf
```

Retorno Json:
```
{
    "Opto2": 1,
    "Opto1": 1
}
```

# Exemplo para leitura dos estados dos reles:

```
curl -X POST http://192.168.0.102:9000/get_relay -F token=af87241285fe416668ecc050c17385bf
```

Retorno Json:
```
{
    "Relay2": 0,
    "Relay1": 0
}
```

# Exemplo para Acionamento dos reles:

```
curl -X POST http://192.168.0.102:9000/set_relay -F token=af87241285fe416668ecc050c17385bf -F relay_number=1 -F type_action=pulse
```
Metódos suportados são:
* type_action=pulse
* type_action=on
* type_action=off

Retorno Json:
```
{  
   "200":"Rele acionado"
}
```




