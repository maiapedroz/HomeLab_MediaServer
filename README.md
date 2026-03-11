# HomeLab_MediaServer




https://www.youtube.com/watch?v=AEyhpuWeiTk

### Conceito
Usar o Jellyfin como servidor de mídia, usar o Sonarr, Radarr e Prowlarr para requisições de conteúdo e Caddy e DuckDNS para roteamento.

Passo a Passo
- Baixar o Caddy com os mods de cloudflare, duckdns e security.
- Como a Vivo atrapalha bastante, a porta 443 está bloqueada, porém a porta 8443 substitui ela e é abrível, porém não garante um certificado automaticamente.
- O DuckDNS cria uma URL e gera um certificado HTTPS, o Caddy comprova e libera o proxy.
- É necessário ainda usar o DNS resolver da Cloudflare, pois o da Vivo não funciona.
- Utiliza os Windows Service Control para automatizar a inicialização no boot.
  [Configuração do Caddy](Caddy)
