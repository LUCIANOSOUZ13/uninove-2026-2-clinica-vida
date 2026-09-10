## O caminho de uma requisição

```mermaid
sequenceDiagram
    participant N as Navegador do paciente
    participant D as Servidor DNS
    participant S as Servidor da Clínica Vida+
    N->>D: clinicavidamais.com.br?
    D-->>N: 203.0.113.42
    N->>S: conexão TCP e TLS na porta 443
    N->>S: GET /consultas/agendar
    S-->>N: 200 OK, HTML da agenda
```

## Evidência do DNS

```text
C:\Users\leonida>nslookup github.com
Servidor:  one.one.one.one
Address:  1.1.1.1

Nome:    github.com
Address:  4.228.31.150

C:\Users\leonida>ping github.com
Disparando github.com com 32 bytes de dados:
Resposta de 4.228.31.150: bytes=32 tempo=12ms TTL=113
```
