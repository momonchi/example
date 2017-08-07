git clone https://github.com/demoiselle/example.git --depth=1

# CEP App
Aplicação "Consulta CEP" com Demoiselle v3.0.

- **Auth**: (CRUD)
- **Cep**: Open

Verificação de segurança da api (https://schd.io/2sGy)
Verificação de segurança do demoiselle.org (https://schd.io/30wv)

# Progessive Web

https://www.demoiselle.org/cep/#!/

# Windows Store
https://www.microsoft.com/pt-br/store/p/cep/9pchwwpc3phr?rtc=1

# Docker

docker pull demoiselleframework/cep

docker run -t -i -p 8080:8080 --network="host" demoiselleframework/cep

# Api do servidor

https://cep-fwkdemoiselle.rhcloud.com/ (Servidor Wildfly API)

https://cep-fwkdemoiselle.rhcloud.com/haproxy-status/ 

# Exemplos de consulta (Restful padrão)

```bash
Lista de UF
https://cep-fwkdemoiselle.rhcloud.com/api/v1/ufs

Lista de Localidades por UF
https://cep-fwkdemoiselle.rhcloud.com/api/v1/cidades/PR

Lista de Logradouros por UF
https://cep-fwkdemoiselle.rhcloud.com/api/v1/logradouro/PR/Pioli
```

# Exemplos de consulta (Usando componente CRUD)

 ```bash
 Filtro por Logradouros do Paraná (PR)
 https://cep-fwkdemoiselle.rhcloud.com/api/v1/ceps?cep=80520170
  
 Filtro por Logradouros do Paraná (PR)
 https://cep-fwkdemoiselle.rhcloud.com/api/v1/ceps?uf=PR
 
 Filtro por Logradouros do Paraná (Curitiba)
 https://cep-fwkdemoiselle.rhcloud.com/api/v1/ceps?cidade=Curitiba
 
 Filtro por Logradouros do Paraná (Curitiba) com apenas 11 registros
 https://cep-fwkdemoiselle.rhcloud.com/api/v1/ceps?cidade=Curitiba&range=0-10
 
 Filtro por Logradouros do Paraná (Curitiba) ordenado por logradouro
 https://cep-fwkdemoiselle.rhcloud.com/api/v1/ceps?cidade=Curitiba&sort=logradouro
 
 Filtro por Logradouros do Paraná (Curitiba) ordenado por bairro
 https://cep-fwkdemoiselle.rhcloud.com/api/v1/ceps?cidade=Curitiba&sort=bairroIni
```

