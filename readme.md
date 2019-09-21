Mule OAuth 2.0 Provider (MOAP)
===============================

It can be used in conjunction with OAuth 2.0 Access Token Enforcement (OAuth2 ATE).

Endpoints:
* /validate
* /authorize
* /access_token

OAuth 2.0 Provider Module: https://anypoint.mulesoft.com/exchange/com.mulesoft.modules/mule-oauth2-provider-module/

## Getting Started

1. Open Studio and create a Mule project
2. Search in Exchange for "OAuth Provider Module"


## OAuth Policy Enforcement

Query parameter: ?access_token=123
Authorization header: Authentication: Bearer 123

Security scheme required for API console.

Security schemes: https://github.com/raml-org/raml-spec/blob/master/versions/raml-10/raml-10.md#security-schemes


## Flow

1. Client contacts Mule OAuth Provider (MOAP) to retrieve the token (/authorize, /access_token)
2. Client calls the resource
3. Proxy intercepts the call and validate the token (/validate)
4. Validated token is cached
5. Resource is available to the client

## OAuth 2.0 Grant Types

Implicit, Client credentials, Password, Authorization Code

Common: Authorization Code

Implicit: issuer skips the step of generating an intermediate access code


## Client 

OAuth client module: https://docs.mulesoft.com/connectors/oauth/oauth-documentation

## Reference

RFC 6749: The OAuth 2.0 Authorization Framework
https://tools.ietf.org/html/rfc6749


## Examples

Example 2: External OAuth 2.0 server for Anypoint Platform
https://anypoint.mulesoft.com/exchange/org.mule.templates/api-gateway-external-oauth2-provider/
Doc:https://github.com/mulesoft/template-gw-external-oauth2-provider/blob/master/ExternalAESTutorial.pdf

Example 3: accelerator (Authentication Server)
https://anypoint.mulesoft.com/exchange/org.mule.templates/template-banking-auth-server/

Example 4: 2-factor auth
https://anypoint.mulesoft.com/exchange/68ef9520-24e9-4cf2-b2f5-620025690913/two-factor-auth-policy/



(Client implementation)
Example OAuth using Box.com
https://anypoint.mulesoft.com/exchange/org.mule.examples/oauth2-authorization-code-using-the-HTTP-connector/

