# TP curl - comprendre les requêtes et les réponses HTTP

Pour les questions suivantes, vous devez utiliser l'url suivante : https://webhook.site/37f00faa-5d4f-4572-97a8-2db3c5b785c5

Pour tous les appels vous devez ajouter un header pour identifier votre appel parmis ceux des autres étudiants : x-student : VOTRE_NOM

## Faire un appel curl : copier la commande exécutée et indiquer la requête et la réponse
curl -v https://webhook.site/37f00faa-5d4f-4572-97a8-2db3c5b785c5 -H "x-student:Bennai Meziane Rayan"
requete: GET /37f00faa-5d4f-4572-97a8-2db3c5b785c5 
reponse: HTTP/1.1 200 OK
## Quel est la version du protocole utilisé par le serveur ?
version du protocole utilisé:  HTTP/1.1

## Quels sont les headers que l'on envoie dans la requête ? Quels sont leur sens ?

> GET /37f00faa-5d4f-4572-97a8-2db3c5b785c5 HTTP/1.1 :
> Host: webhook.site : Host indique le nom de domaine du server
> User-Agent: curl/7.74.0 : user agent indique de quelle client http a été envoyé la requete
> Accept: */*  : indique le type de contenu



## Quelles informations pouvez-vous trouver à propos du certificat SSL ?

SSL connection using TLSv1.3 / TLS_AES_256_GCM_SHA384
* ALPN, server did not agree to a protocol
* Server certificate:
*  subject: CN=webhook.site
*  start date: Jul 31 23:09:19 2022 GMT
*  expire date: Oct 29 23:09:18 2022 GMT
*  subjectAltName: host "webhook.site" matched cert's "webhook.site"
*  issuer: C=US; O=Let's Encrypt; CN=R3
*  SSL certificate verify ok.

## Quel est le code de la réponse ? Que signifie-t-il ?

le code de la reponse est 200 et ça signifie que la requete est bien passé
## Quels headers recevez vous dans la response ? Quels sont leur sens ?

< Server: nginx : indique le nom du serveur
< Content-Type: text/plain; charset=UTF-8 : type de fichier reçu
< Transfer-Encoding: chunked : type d'encoding utilisé pour atteindre le client
< Vary: Accept-Encoding : 
< X-Request-Id: a131ab8d-6445-4117-bec4-39099a8c2c3a : 
< X-Token-Id: 37f00faa-5d4f-4572-97a8-2db3c5b785c5
< Cache-Control: no-cache, private : dis a tout les du client et du server si ils peuvent garder l'objet dans le cache ou pas
< Date: Thu, 06 Oct 2022 14:01:40 GMT : le temps et la date quand le message a été envoyé


## Faire un appel curl en envoyant du texte brut : copier la commande exécutée et indiquer la requête et la réponse

curl  -v --data "hi karim pinchon" https://webhook.site/37f00faa-5d4f-4572-97a8-2db3c5b785c5
requete:> POST /37f00faa-5d4f-4572-97a8-2db3c5b785c5 HTTP/1.1


reponse: HTTP/1.1 200 OK


## Faire un appel curl en envoyant du JSON (avec les bons headers) : copier la commande exécutée et indiquer la requête et la réponse
curl -v --header "Content-Type: application/json"  --request POST  --data '{"nom":"pinchon","prenom":"Rayan"}' https://webhook.site/37f00faa-5d4f-4572-97a8-2db3c5b785c5 -H "x-student:Bennai Meziane Rayan"
requete:> POST /37f00faa-5d4f-4572-97a8-2db3c5b785c5 HTTP/1.1
reponse:< HTTP/1.1 200 OK


## Faire une appel curl en envoyant une basic authentication en utilisant 2 méthodes différentes : copier les commandes exécutées et indiquer la requête et la réponse à chaque fois 
 curl --user "rayan" https://webhook.site/37f00faa-5d4f-4572-97a8-2db3c5b785c5

## Exécuter la commande suivante avec la méthode GET puis indiquer la réponse : curl https://demo.api-platform.com/books/07dd4786-aaa7-4d08-a467-076b76f1d1b6
reponse : 404 not found


## Exécuter la commande suivante avec la méthode PATCH  puis indiquer la réponse : curl https://demo.api-platform.com/top_books/1
reponse : 405 method not allowed

## Quel est le code HTTP reçu ? Quel est sa signification ?


## Exécuter la commande suivante puis indiquer la réponse : curl https://demo.api-platform.com/top_books/1
reponse: 
HTTP/2 200

## Exécuter la commande suivante puis indiquer la réponse : curl https://demo.api-platform.com/top_books/9999
reponse: 
HTTP/2 404 

## Quel est le code HTTP ? Que signifie-t-il ?
code: 404 la page n'as pas ete trouvé
## Exécuter la requête suivante et copier la réponse : curl https://google.fr


## Quel est le code HTTP reçu ? Pouvez-vous expliquer cette réponse?
code 301 : permanently moved
la ressource https://google.fr a ete remplacé par https://www.google.com



## Comment éviter cette réponse ? Trouvez 2 solutions différentes et détaillez les.
