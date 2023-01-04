# dex-guide

[Dex](https://github.com/dexidp/dex) 基于 [OpenID Connect](https://openid.net/connect/) 提供了统一的身份认证服务。
支持包括：LDAP、OAuth 等认证服务的对接。

在 DevOps 这种需要连接很多系统、工具的场景下，Dex 可以作为非常好的一种身份统一连接器。

`/.well-known/openid-configuration`

返回

```json
{
    "issuer": "http://localhost:3000/",
    "authorization_endpoint": "http://localhost:3000/login/oauth/authorize",
    "token_endpoint": "http://localhost:3000/login/oauth/access_token",
    "jwks_uri": "http://localhost:3000/login/oauth/keys",
    "userinfo_endpoint": "http://localhost:3000/login/oauth/userinfo",
    "introspection_endpoint": "http://localhost:3000/login/oauth/introspect",
    "response_types_supported": [
        "code",
        "id_token"
    ],
    "id_token_signing_alg_values_supported": [
        "RS256"
    ],
    "subject_types_supported": [
        "public"
    ],
    "scopes_supported": [
        "openid",
        "profile",
        "email",
        "groups"
    ],
    "claims_supported": [
        "aud",
        "exp",
        "iat",
        "iss",
        "sub",
        "name",
        "preferred_username",
        "profile",
        "picture",
        "website",
        "locale",
        "updated_at",
        "email",
        "email_verified",
        "groups"
    ],
    "code_challenge_methods_supported": [
        "plain",
        "S256"
    ],
    "grant_types_supported": [
        "authorization_code",
        "refresh_token"
    ]
}
```
