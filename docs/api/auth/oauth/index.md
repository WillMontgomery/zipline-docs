import APIBadge from '../../../../src/components/APIBadge';

# /api/auth/oauth

:::info
Requires [authentication](/docs/api#authentication)
:::

## <APIBadge type="GET" /> Get OAuth providers

### <APIBadge type="200" /> Ok (JSON)

Array of OAuth Objects:

| Field Name | Type     | Description                                         |
| ---------- | -------- | --------------------------------------------------- |
| `id`       | `string` | An autogenerated ID of the provider                 |
| `provider` | `string` | The name of the provider, discord, github or google |
| `token`    | `string` | The OAuth access_token of the user                  |
| `refresh`  | `string` | The OAuth refresh_token of the user                 |
| `username` | `string` | The username of the O                               |

```json
[
  {
    "id": 2,
    "provider": "DISCORD",
    "userId": 18,
    "username": "dicedtomato",
    "token": "x",
    "refresh": "x"
  },
  {
    "id": 3,
    "provider": "GITHUB",
    "userId": 18,
    "username": "diced",
    "token": "gho_x",
    "refresh": null
  }
]
```
