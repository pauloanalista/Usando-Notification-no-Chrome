# Usando-Notification-no-Chrome

#### Veja como utilizar a classe Notification do Chrome
```sh


<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
</head>

<body>
    <h1>Notificações</h1>
    <input type="button" value="Notificar!" onclick="minhaNotificao()">
    <script>
        //Verifica e solicita se o usuario tem permissao para utilizar as notificações do Chrome
        document.addEventListener('DOMContentLoaded', function () {
            if (!Notification) {
                alert('Desktop notifications not available in your browser. Try Chromium.');
                return;
            }

            if (Notification.permission !== "granted")
                Notification.requestPermission();
        });

        function minhaNotificao() {
            if (Notification.permission !== "granted") {
                Notification.requestPermission();
            }
            else {
                var notificacao = new Notification("I love code", {
                    icon: 'http://cdn.sstatic.net/stackexchange/img/logos/so/so-icon.png',
                    body: 'Se inscreva e curta nossas redes sociais'
                });

                notificacao.onclick = function () {
                    window.open('http://ilovecode.com.br');
                };
            }
        }

        minhaNotificao();
    </script>
</body>

</html>
```

# VEJA TAMBÉM
## Grupo de Estudo no Telegram
- [Participe gratuitamente do grupo de estudo](https://t.me/blogilovecode)

## Cursos baratos!
- [Meus cursos](https://olha.la/udemy)

## Fique ligado, acesse!
- [Blog ILoveCode](https://ilovecode.com.br)

## Novidades, cupons de descontos e cursos gratuitos
https://olha.la/ilovecode-receber-cupons-novidades
