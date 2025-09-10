# teste4p0
Apenas um teste temporário e passageiro sobre teorias aleatórias, mas com alguma documentação norteadora...


IP:porta/rota do midleware na aws
http://52.1.197.112:3000/queue/items

- get: retorna todos os pedidos na fila
- post: envia um pedido para a fila

---
Mais informações no swagger do midleware em: http://52.1.197.112:3000/docs
---

Formato simplificado do payload de envio (order tem o objeto com as configurações da caixa para produção)
```
{
  "payload": {
    "orderId": "ABC-123",
    "sku": "KIT-01",
    "order":{"caixa": "exemplo"}
  },
  "callbackUrl": "http://localhost:3333/callback"
}
```
exemplo de id de pedido retornado:
```
{
  "id": "68b730ef21c2f2c7fb07ef58"
}
```

Pode usar esse id para acompanhar o status do pedido:
---
http://52.1.197.112:3000/queue/items/{id}

---


Exemplo de form de post no ar: https://teste4p0.vercel.app/


## Exemplo do payload completo com um pedido de caixa real:
```
{
            "payload": {
                "orderId": "ABC-123",
                "order": {
                    "codigoProduto": 1,
                    "bloco1": {
                        "lamina1": 1,
                        "lamina2": 1,
                        "lamina3": 1,
                        "padrao1": "1",
                        "padrao2": "1",
                        "padrao3": "1"
                    },
                    "bloco2": {
                        "lamina1": 1,
                        "lamina2": 1,
                        "lamina3": 1,
                        "padrao1": "1",
                        "padrao2": "1",
                        "padrao3": "1"
                    },
                    "bloco3": {
                        "lamina1": 1,
                        "lamina2": 1,
                        "lamina3": 1,
                        "padrao1": "1",
                        "padrao2": "1",
                        "padrao3": "1"
                    }
                },
                "sku": "KIT-01"
            },
            "callbackUrl": "http://localhost:3333/callback"
        }
```



[>> Notion que pode ser útil para isso aqui <<](https://rafaellindemann.notion.site/Post-de-pedido-e-cores-exemplo-246d393ff68e80289b22fae8c19b4025
)
