# HyperText Transfer Protocol (HTTP) Basics

- HTTP é um protocolo de nível de aplicativo usado para acessar recursos na World Wide Web. O termo hipertexto significa texto contendo links para outros recursos e textos que podem ser facilmente interpretados pelos leitores.

A comunicação HTTP consiste em um cliente e um servidor, onde o cliente solicita um recurso ao servidor. O servidor processa as solicitações e retorna o recurso solicitado. A porta padrão para comunicação HTTP é 80; no entanto, isso pode ser alterado.

Os recursos por HTTP são acessados por meio de um Localizador Uniforme de Recursos (URL). Vejamos a estrutura de um URL.

![Estrutura de um URL](./assets/url_structure.png)

- Aqui está o que cada componente representa:

| Component      | Description                                                                                                                                                                                                                                                                                                                                      |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `scheme`       | Isso é usado para identificar o protocolo que está sendo acessado pelo cliente. Geralmente é _http_ ou _https_.                                                                                                                                                                                                                                  |
| `User info`    | Este é um componente opcional que contém credenciais no formato _usuário:senha_, que é usado para autenticação no host.                                                                                                                                                                                                                          |
| `Host`         | O host significa a localização do recurso. Pode ser um nome de host ou um endereço IP. Dois pontos separam um **host** e uma **porta**.                                                                                                                                                                                                          |
| `Port`         | URLs sem uma porta especificada apontam para a porta 80 padrão. Se a porta do servidor HTTP não estiver sendo executada na porta 80, ela pode ser especificada na URL.                                                                                                                                                                           |
| `Path`         | PAth aponta para o recurso que está sendo acessado, que pode ser um arquivo ou uma pasta. Se nenhum caminho for especificado, o servidor retorna o documento de índice padrão hospedado por ele **(por exemplo, index.html)**.                                                                                                                   |
| `Query String` | A string de consulta é precedida por um ponto de interrogação (?). Este é outro componente opcional que é usado para passar informações para o recurso. Uma string de consulta consiste em um parâmetro e um valor. No exemplo acima, o parâmetro é _login_ e seu valor é _true_. Pode haver vários parâmetros separados por um E comercial (&). |
| `Fragment`     | Isso é processado por navegadores no lado do cliente para localizar seções dentro do recurso primário.                                                                                                                                                                                                                                           |

---

## HTTP Flow

![Estrutura de um fluxo HTTP](./assets/HTTP_Flow.png)

The diagram above presents the anatomy of an HTTP request at a very high level. The first time a user enters a URL (inlanefreight.com) into the browser, it requests a DNS (Domain Name Resolution) server to resolve the domain. The DNS server looks up the IP address for inlanefreight.com and returns it. All domain names need to be resolved this way, as a server can't communicate without an IP address.

Next, the browser sends a GET request to the default HTTP port, i.e., 80, asking for the root / folder. Here GET is the request method. The type of request can vary, as we'll see later. The web server receives the request and processes it. By default, servers are configured to return an index file when a request for / is received. In this case, the contents of index.html are read and returned by the webserver as an HTTP response. The response also contains information such as the status code 200 OK, meaning the request processed successfully.

The index.html contents are then rendered by the web browser and presented to the user. HTML (HyperText Markup Language) is a client-side language that is understood and processed by browsers. It is the standard markup language to display documents via a web browser. HTML pages are assisted by Cascading Style Sheets (CSS), which allow flexibility for applying presentation elements such as layout, colors, and fonts to one or multiple web pages as well as scripting languages such as JavaScript which enable interactive web pages.
