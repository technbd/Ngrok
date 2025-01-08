## Ngrok:

Ngrok is a powerful tool that provides secure tunnels to your local machine or server. It allows developers to expose a local web server to the internet without deploying it to a public host. This can be particularly useful for testing and development purposes.


#### Key Features of Ngrok:

- Local to Public Tunneling: Exposes your local development environment to a public URL that can be shared.
- HTTPS Support: Automatically provides HTTPS for your exposed endpoints.
- Custom Subdomains and Domains: With a paid plan, you can use custom subdomains or your own domains.
- Introspection: Provides a web interface to inspect HTTP traffic in real time.
- Authentication: Supports securing tunnels with basic authentication.
- Webhooks: Simplifies testing and debugging webhooks by exposing a URL accessible from the internet.
- Session Persistence: Allows persistent tunnels, so you can keep the same public URL across sessions with the right plan.
- Multi-Protocol Support: Supports HTTP, HTTPS, TCP, and even custom protocols.


### Install Ngrok:

```
wget https://bin.equinox.io/c/bNyj1mQVY4c/ngrok-v3-stable-linux-amd64.tgz
```



```
tar -zxvf ngrok-v3-stable-linux-amd64.tgz
```


```
./ngrok -v

ngrok version 3.19.0
```


```
./ngrok -h


NAME:
  ngrok - tunnel local ports to public URLs and inspect traffic

USAGE:
  ngrok [command] [flags]

DESCRIPTION:
  ngrok exposes local networked services behinds NATs and firewalls to the
  public internet over a secure tunnel. Share local websites, build/test
  webhook consumers and self-host personal services.
  Detailed help for each command is available by adding '--help' to any command or with
  the 'ngrok help' command.
  Open https://dashboard.ngrok.com/obs/traffic-inspector to inspect traffic.


TERMS OF SERVICE: https://ngrok.com/tos

EXAMPLES:
  ngrok http 80                           # secure public URL for port 80 web server
  ngrok http --url baz.ngrok.dev 8080     # port 8080 available at baz.ngrok.dev
  ngrok http foo.dev:80                   # tunnel to host:port instead of localhost
  ngrok http https://localhost            # expose a local https server
  ngrok tcp 22                            # tunnel arbitrary TCP traffic to port 22
  ngrok tls --url=foo.com 443             # TLS traffic for foo.com to port 443
  ngrok start foo bar baz                 # start tunnels from the configuration file

COMMANDS:
  api                            use ngrok agent as an api client
  completion                     generates shell completion code for bash or zsh
  config                         update or migrate ngrok's configuration file
  credits                        prints author and licensing information
  diagnose                       diagnose connection issues
  help                           Help about any command
  http                           start an HTTP tunnel
  service                        run and control an ngrok service on a target operating system
  start                          start endpoints or tunnels by name from the configuration file
  tcp                            start a TCP tunnel
  tls                            start a TLS tunnel
  tunnel                         start a tunnel for use with a tunnel-group backend
  update                         update ngrok to the latest version
  version                        print the version string

OPTIONS:
      --config strings    path to config files; they are merged if multiple
  -h, --help              help for ngrok
      --metadata string   opaque user-defined metadata for the tunnel session
  -v, --version           version for ngrok

```



#### Add the token to your setup:

```
ngrok config add-authtoken <toke_here>


Authtoken saved to configuration file: /root/.config/ngrok/ngrok.yml
```



#### Start a Tunnel:

- Expose a local server on port 80. 


```
./ngrok http 80


### Output:

🐛 Found a bug? Let us know: https://github.com/ngrok/ngrok

Session Status                online
Account                       Technbd (Plan: Free)
Version                       3.19.0
Region                        India (in)
Latency                       76ms
Web Interface                 http://127.0.0.1:4040
Forwarding                    https://8530-113-11-21-65.ngrok-free.app -> http://localhost:80

Connections                   ttl     opn     rt1     rt5     p50     p90
                              0       0       0.00    0.00    0.00    0.00
```




```
echo "Hello ngrok" > /var/www/html/index.html
```



#### Web console:
Visit the web interface: `http://127.0.0.1:4040` or `https://8530-113-11-21-65.ngrok-free.app`






### Links:
- [Download ngrok](https://download.ngrok.com/linux?tab=download)
- [Sign up on ngrok](https://dashboard.ngrok.com/signup)
- [Install Ngrok | video](https://www.youtube.com/watch?v=JA2maK8AeXQ)

