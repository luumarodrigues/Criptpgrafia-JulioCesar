## Sobre a Criptografia de Júlio César

Essa criptografia se baseia na substituição da letra do alfabeto avançado um determinado número de casas. Por exemplo, considerando o número de casas = 3:

Normal: a ligeira raposa marrom saltou sobre o cachorro cansado

Cifrado: d oljhlud udsrvd pduurp vdowrx vreuh r fdfkruur fdqvdgr

Regras
As mensagens serão convertidas para minúsculas tanto para a criptografia quanto para descriptografia.
No nosso caso os números e pontos serão mantidos, ou seja:

Normal: 1a.a

Cifrado: 1d.d

## DESAFIO 

Escrever programa, em qualquer linguagem de programação, que faça uma requisição HTTP para a url abaixo:

`https://api.codenation.dev/v1/challenge/dev-ps/generate-data?token=SEU_TOKEN`

O resultado da requisição vai ser um JSON conforme o exemplo:

```
{
	"numero_casas": 10,
	"token":"token_do_usuario",
	"cifrado": "texto criptografado",
	"decifrado": "aqui vai o texto decifrado",
	"resumo_criptografico": "aqui vai o resumo"
}
```
O primeiro passo é você salvar o conteúdo do JSON em um arquivo com o nome answer.json, que irá usar no restante do desafio.

Você deve usar o número de casas para decifrar o texto e atualizar o arquivo JSON, no campo decifrado. O próximo passo é gerar um resumo criptográfico do texto decifrado usando o algoritmo sha1 e atualizar novamente o arquivo JSON.

Seu programa deve submeter o arquivo atualizado para correção via POST para a API:

`https://api.codenation.dev/v1/challenge/dev-ps/submit-solution?token=SEU_TOKEN`

OBS: a API espera um arquivo sendo enviado como multipart/form-data, como se fosse enviado por um formulário HTML, com um campo do tipo file com o nome answer. Considere isso ao enviar o arquivo.


## Configurações iniciais

| Variável                       | Padrão         | Commentário       |
| :---                           | :---            | :---             |
| `API_TOKEN` | 'TOKEN'| Para encontrar o seu token , acesse seu perfil na plataforma Codenation.  |
| `API_URL` | 'https://api.codenation.dev/v1/challenge/dev-ps/generate-data?token=TOKEN' | Url dada para fazer requisição HTTP | 
| `arquivo` | 'C:\\Users\\luma.de.f.rodrigues\\python\\answer.json'| Caminho para criar o arquivo json no seu computador|
| `url` | 'https://api.codenation.dev/v1/challenge/dev-ps/submit-solution?token=TOKEN' | Url para fazer requisição post | 
