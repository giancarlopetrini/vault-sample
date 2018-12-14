# vault-sample
Local instance of vault server with some example interaction.

## usage
1. `git clone https://github.com/giancarlopetrini/vault-sample`
2. `cd vault-sample/docker && docker build . -t vault-server`
3. `docker run -p 8200:8200 vault-server`
4. copy these values from container's output on startup.
```
(sample outout)
Unseal Key: VxoPKlqrTzYM6nMAXUL6mf6uI7zqbjTUJqSvJjg9LaA=
Root Token: s.8DvHThWbRAvEclTBeRvjgnVI
```
5. in `client/auth.yaml` paste token and unseal key in corresponding places
6. in another terminal, `cd client && go run main.go`
