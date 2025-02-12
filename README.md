# Plano de Teste: Teste de Performance - JSONPlaceholder

## Thread Groups (Grupos de Usuários Simulados)

### Carga - 500 Usuários
- **Número de Usuários**: 500
- **Tempo de Ramp-up**: 60 segundos
- **Duração**: Indefinida

### Stress - Até Falha
- **Número de Usuários**: 1000
- **Tempo de Ramp-up**: 30 segundos
- **Duração**: Indefinida

### Segurança - DDoS & SQL Injection
- **Número de Usuários**: 200
- **Tempo de Ramp-up**: 10 segundos
- **Duração**: Indefinida

## Requisições HTTP Configuradas

### Requisição GET - Carga
- **Host**: jsonplaceholder.typicode.com
- **Caminho**: /users
- **Método**: GET

### Requisição GET - Stress
- **Host**: jsonplaceholder.typicode.com
- **Caminho**: /users
- **Método**: GET

### Ataque DDoS
- **Host**: jsonplaceholder.typicode.com
- **Caminho**: /users
- **Método**: GET

### SQL Injection
- **Host**: jsonplaceholder.typicode.com
- **Caminho**: /users?id=' OR 1=1 --
- **Método**: GET

## O que esses testes fazem?

- **Carga (500 usuários)**: Simula um número considerável de acessos simultâneos para verificar a estabilidade do sistema.
- **Stress (1000 usuários até falha)**: Testa os limites do servidor para entender até que ponto ele aguenta.
- **Segurança (DDoS e SQL Injection)**: Verifica se o sistema está vulnerável a ataques de negação de serviço (DDoS) e injeções SQL.

