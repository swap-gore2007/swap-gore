# swap-gore
These workflows help to integrate Philips Hue light with Cisco SecureX platform. Philips Hue light can be managed (switch on or change color) in a critical event. 
This can be act as visual alert mechanism to concern team like SOC or higher executive to indicate critical situation in the network. 

Philips Hue light requires Hue bridge and a supported light. Kindly refer https://www.philips-hue.com/en-in for more information.

Philips Hue API works on OAuth2.0 authentication framework. It provides access token to access API resources. Access token is valid only for 7 days.
Hence it needs to be refreshed before it's expiry. 

Access token and userid are required to access Philips Hue API resources. Complete process is explained at https://developers.meethue.com/develop/hue-api/remote-authentication-oauth/

1. "Philips Hue - Access Token & Referesh Token and Username Creation" workflow generates access token and refresh token. It also creates Username in Philips Hue system. This userid will require to manage lights.

2. "Philips Hue - Refershing Access Token & Refresh Token" workflow refreshes access token within seven days. This helps to keep access token valid.

3. "Philips Hue - Light Control" workflow switch on light and change it's color to RED. This workflow requires access token and 
userid created in above workflows. This can be used as alert mechanism in any other workflows.

If you need any help, kindly contact me at swap.gore2007@gmail.com
