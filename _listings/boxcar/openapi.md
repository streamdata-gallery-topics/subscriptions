swagger: "2.0"
x-collection-name: Boxcar
x-complete: 1
info:
  title: Box Car
  description: add-boxcar-services-to-your-app-so-users-can-get-messages-and-update-all-their-favorite-social-services-
  version: 1.0.0
host: boxcar.io
basePath: /devices/providers/%7Bprovider_key%7D/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /notifications/subscribe:
    post:
      summary: Subscribe to Provider
      description: This sends the user with the matching e-mail address a push notification
        which requests that they add your service. This will ease integration with
        your website, as you will have already registered them on your system and
        can identify whom they are based on their Boxcar e-mail address. Please note,
        this API call is an exception and will return an HTTP status code of 404 if
        we are unable to find the registered user by e-mail in our system. If the
        email address is not found in our system, we'll send an email to it letting
        the user know where they can download Boxcar. If the user has already added
        your service, we'll return an HTTP status code of 401.
      operationId: Create_subscribeToProvider_
      x-api-path-slug: notificationssubscribe-post
      parameters:
      - in: query
        name: email
        description: The users e-mail address
      - in: query
        name: provider_key
        description: The API key
      responses:
        1:
          description: Photoset not found - The photoset id passed was not the id
            of avalid photoset owned by the calling user
        2:
          description: Photo not found - The photo id passed was not the id of a valid
            photo owned by the calling user
        95:
          description: SSL is required - SSL is required to access the Flickr API
        96:
          description: Invalid signature - The passed signature was invalid
        97:
          description: Missing signature - The call required signing but no signature
            was sent
        98:
          description: Login failed / Invalid auth token - The login details or auth
            token passed were invalid
        99:
          description: User not logged in / Insufficient permissions - The method
            requires user authentication but the user was not logged in, or the authenticated
            method call did not have the required permissions
        100:
          description: Invalid API Key - The API key passed was not valid or has expired
        105:
          description: Service currently unavailable - The requested service is temporarily
            unavailable
        106:
          description: Write operation failed - The requested operation failed due
            to a temporary issue
        111:
          description: Format "xxx" not found - The requested response format was
            not found
        112:
          description: Method "xxx" not found - The requested method was not found
        114:
          description: Invalid SOAP envelope - The SOAP envelope send in the request
            could not be parsed
        115:
          description: Invalid XML-RPC Method Call - The XML-RPC request document
            could not be parsed
        116:
          description: Bad URL found - One or more arguments contained a URL that
            has been used for abuse on Flickr
        "":
          description: ""
        400:
          description: Bad input parameter
        401:
          description: Bad or expired token
        403:
          description: Bad OAuth request (wrong consumer key, bad nonce, expired timestamp
        404:
          description: File or folder not found at the specified path
        405:
          description: Request method not expected (generally should be GET or POST)
        429:
          description: Your app is making too many requests and is being rate limited
        503:
          description: If the response includes the Retry-After header, this means
            your OAuth 1
        507:
          description: User is over Dropbox storage quota
        5xx:
          description: Server error
        200:
          description: OK
      tags:
      - Notifications
      - Subscriptions