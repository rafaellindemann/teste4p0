http://52.1.197.112:3000/queue/items
get
post
```
{
  "payload": {
    "orderId": "ABC-123",
    "sku": "KIT-01",
    "order":{"caixa": "bonita"}
  },
  "callbackUrl": "http://localhost:3333/callback"
}
```


---
http://52.1.197.112:3000/queue/items/{id}

---