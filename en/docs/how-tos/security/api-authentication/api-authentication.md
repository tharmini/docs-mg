# API Authentication

WSO2 Microgateway provides the ability to secure APIs in API level and resource levels. The following section would concisely guide you through the available security options in the WSO2 Microgateway. API security can be divided to two main categories; namely, Application-level security and Transport level security.

By default, APIs are secured with application security. However, if you want to disable all security for API, you can achieve it by following the document on [Disabling Security](https://docs.wso2.com/display/MG310/Disabling+Security) .

### Application Security

Application security can be provided in the API and resource levels. The following are the API authentication types granted by WSO2 Microgateway.

-   [JWT authentication]({{base_path}}/how-tos/security/api-authentication/secure-apis-using-oauth2.0-access-tokens/secure-apis-using-jwt-self-contained-jwt/)
-   [Opaque token authentication]({{base_path}}/how-tos/security/api-authentication/secure-apis-using-oauth2.0-access-tokens/secure-apis-using-opaque-tokens/)
-   [Basic authentication]({{base_path}}/how-tos/security/api-authentication/basic-authentication/)
-   [API Key authentication]({{base_path}}/how-tos/security/api-authentication/api-key-authentication/)

If you provide two or more security types for a resource or API, API invocation would be successful if one of the given authentications passed for the API request. i.e. Application security types have OR relationship with one another.

### Transport Security

Mutual SSL support is provided in the gateway level and API Level in WSO2 Microgateway. Mutual SSL authentication is supported at the API level.

-   [Mutual SSL authentication]({{base_path}}/how-tos/security/api-authentication/mutual-ssl-authentication/)

### Combine Application and transport Security for API Authentication

By default, Application security is mandatory for API authentication. However, if you enable transport security for API authentication (i.e. if you enabled mutual SSL authentication for the API), you can make application security to be optional so that application security is not necessarily be added to the API/resource. Follow the documentation on [make application security optional]({{base_path}}/how-tos/security/api-authentication/making-application-security-optional/) for more details.

By default Application security and transport security is in AND relationship. i.e. if mutual SSL authentication is enabled, a successful API invocation requires passing the mutual SSL handshake as well as passing one of the provided application security. To override this behavior, i.e. to combine Application security and transport security authentication schemes with OR combination, make application security optional. For more details, follow the documentation on [make application security optional]({{base_path}}/how-tos/security/api-authentication/making-application-security-optional/

