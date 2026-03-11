# Descrição da configuração e do funcionamento do Caddy


## Passo a Passo
- Baixar o Caddy com os mods de Cloudflare, Duckdns e Security.
- Como a Vivo atrapalha bastante, a porta 443 está bloqueada, porém a porta 8443 substitui ela e é abrível, porém não garante um certificado automaticamente.
- O DuckDNS cria uma URL e gera um certificado HTTPS, o Caddy comprova e libera o proxy.
- É necessário ainda usar o DNS resolver da Cloudflare, pois o da Vivo não funciona.
- Utiliza os Windows Service Control para automatizar a inicialização no boot.
- Parâmetros: .\caddy.exe run
- Caso o Caddyfile esteja em outro diretório complemente: --config [caminho]
