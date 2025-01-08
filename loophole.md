## Loophole:

Loophole is an open-source tool designed to expose local web servers to the internet securely. It simplifies tasks like sharing local applications, testing APIs, or debugging webhooks by providing a public HTTPS URL for your local server.

#### Key Features of Loophole:
- End-to-End Encryption: Loophole ensures your data is secure by encrypting traffic between your machine and the client.
- Custom Subdomains: You can use custom subdomains for your URLs, making them more recognizable and user-friendly.
- Ease of Use: Its simple CLI allows you to set up a public URL in seconds.
- No Configuration Hassle: Loophole handles the complexities of port forwarding, NAT traversal, and tunneling.



#### Supported Functionalities
- Expose local HTTP server
- Expose HTTP server running on any machine in your network
- Expose local directory via HTTPS
- Expose local directory via WebDav
- Basic Auth



### Install Loophole: 

```
https://github.com/loophole/cli/releases/download/1.0.0-beta.15/loophole-cli_1.0.0-beta.15_linux_64bit.tar.gz
```


```
tar -zxvf loophole-cli_1.0.0-beta.15_linux_64bit.tar.gz
```



```
mv loophole-cli_1.0.0-beta.15_linux_64bit loophole-cli
cd loophole-cli
```



```
./loophole --version
```


```
./loophole -h


Loophole - End to end TLS encrypted TCP communication between you and your clients

Usage:
  loophole [flags]
  loophole [command]

Available Commands:
  account     Group of comands concerning loophole account
  completion  Generates bash completion scripts
  help        Help about any command
  http        Expose http server on given port to the public
  path        Expose given directory to the public
  webdav      Expose given directory to the public via WebDav

Flags:
  -h, --help      help for loophole
  -v, --verbose   verbose output
      --version   version for loophole

Use "loophole [command] --help" for more information about a command.
```




#### Create account or login:

_Loophole requires authentication. To log in or sign up, run:_

```
./loophole account login


Please open https://loophole.eu.auth0.com/activate and use RBWL-WPQS code to log in6:47AM INF Logged in successfully
```



#### Logout: (If need)

```
./loophole account logout


6:50AM INF Logged out successfully
```



#### Web console: 

Visit the web interface: `https://loophole.eu.auth0.com/activate` and follow the instructions for sign up. 





### Expose given directory to the public:


```
./loophole path /var/www

./loophole path /var/www --hostname technbd1
```


Or,


```
./loophole dir /var/www/html

./loophole dir /var/www/html --hostname technbd1 --qr


### Output:

Loophole - End to end TLS encrypted TCP communication between you and your clients

Registering your domain... Success!
Starting local file server Success!
Starting local proxy server...  Success!
Initializing secure tunnel...  Success!


Forwarding https://4a2ff03e5faca7920eb574484da802f1.loophole.site -> /var/www/html
Press CTRL + C to stop the service
Logs:
6:51AM INF Awaiting connections...
6:51AM INF Succeeded to accept connection over HTTPS
6:51AM INF Succeeded to accept connection over HTTPS
6:51AM INF Succeeded to accept connection over HTTPS
6:51AM INF Succeeded to accept connection over HTTPS
6:51AM INF Succeeded to accept connection over HTTPS
6:51AM INF TLS Certificate successfully provisioned

```



### Expose http server on given port to the public:

```
./loophole http 80

./loophole http 80 --hostname technbd2


### Output:

Loophole - End to end TLS encrypted TCP communication between you and your clients

Registering your domain... Success!
Starting local proxy server...  Success!
Initializing secure tunnel...  Success!


Forwarding https://technbd2.loophole.site -> http://127.0.0.1:80
Press CTRL + C to stop the service
Logs:
6:54AM INF Awaiting connections...
6:54AM INF Succeeded to accept connection over HTTPS
6:54AM INF Succeeded to accept connection over HTTPS
6:54AM INF Succeeded to accept connection over HTTPS
6:54AM INF Succeeded to accept connection over HTTPS
6:54AM INF Succeeded to accept connection over HTTPS
6:54AM INF Succeeded to accept connection over HTTPS
6:55AM INF TLS Certificate successfully provisioned
6:55AM INF Succeeded to accept connection over HTTPS

```






### Links:
- [Download & Setup](https://loophole.cloud/download)
- [Loophole Docs](https://loophole.cloud/docs)
- [Expose a local resource to the Internet](https://loophole.cloud/docs/guides/expose)
- [Share your files with ease](https://loophole.cloud/blog/share-your-files-with-ease)

