ClaimsAuthenticationModule
==========================

When using federated authentication the identity provider decides solely what 
claims to use to populate the incoming identity. If using multiple identity
providers there is very high probability that they will present the same
information in somewhat different ways. That's where the 
`ClaimsAuthenticationManager` fits in. It works as a translation filter,
that can modify or replace the incoming identity as soon as it has been
constructed from the incoming authentication response.

Implement a `ClaimsAuthenticationManager` by creating a class derived from the
[`System.Security.Claims.ClaimsAuthenticationManager`](http://msdn.microsoft.com/en-us/library/system.security.claims.claimsauthenticationmanager.aspx)
class.

Then register it with a 
[`<claimsAuthenticationManager>`](Configuration.md#claimsauthenticationmanager-element) 
element in the configuration.