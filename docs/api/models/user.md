# User

The user model is used to represent a user in the database.

| Field Name      | Type       | Description                                |
| --------------- | ---------- | ------------------------------------------ |
| `id`            | `number`   | The ID of the user                         |
| `username`      | `string`   | The username of the user                   |
| `avatar`        | `string`   | A base64 encoded image of the users avatar |
| `token`         | `string`   | The users auth token                       |
| `administrator` | `boolean`  | If the user is an administrator            |
| `superAdmin`    | `boolean`  | If the user is a super administrator       |
| `systemTheme`   | `string`   | The system theme of the user               |
| `embedTitle`    | `string`   | The embed title of the user                |
| `embedColor`    | `string`   | The embed color of the user                |
| `embedSiteName` | `string`   | The embed site name of the user            |
| `ratelimit`     | `date`     | The ratelimit of the user, if any          |
| `totpSecret`    | `string`   | The TOTP secret of the user                |
| `domains`       | `string[]` | A list of domains                          |
| `oauth`         | `array`    | [A list of oauth providers](#oauth)        |

## OAuth

| Field Name | Type     | Description                                 |
| ---------- | -------- | ------------------------------------------- |
| `id`       | `number` | Autogenerated ID (useless field honestly)   |
| `provider` | `string` | The provider of the oauth                   |
| `userId`   | `number` | The ID of the user                          |
| `username` | `string` | The username of the oauth user, NOT zipline |
| `token`    | `string` | The access_token                            |
| `refresh`  | `string` | The refresh_token                           |

## Oauth Providers

- `DISCORD`
- `GITHUB`
- `GOOGLE`
