---
swagger: "2.0"
x-collection-name: CloudFlare
x-complete: 1
info:
  title: CloudFlare
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /user/billing/subscriptions/apps:
    get:
      summary: List all of your app subscriptions
      description: List all of your app subscriptions
      operationId: cloudflare-app-subscription-api
      x-api-path-slug: userbillingsubscriptionsapps-get
      parameters:
      - in: query
        name: activated_on
        description: When the subscription was activated2014-03-01T12:20:00Z
      - in: query
        name: cancelled_on
        description: When the subscription was cancelled2014-04-01T12:20:00Z
      - in: query
        name: direction
        description: Direction to order subscriptionsdesc
      - in: query
        name: expired_on
        description: When the subscription expired2014-04-02T12:20:00Z
      - in: query
        name: expires_on
        description: When the subscription will expire2014-03-31T12:20:00Z
      - in: query
        name: match
        description: Whether to match all search requirements or at least one (any)all
      - in: query
        name: order
        description: Field to order subscriptions bystatus
      - in: query
        name: page
        description: Page number of paginated results1
      - in: query
        name: per_page
        description: Number of items per page20
      - in: query
        name: price
        description: The price of the subscription that will be billed, in US dollars20
      - in: query
        name: renewed_on
        description: When the subscription was renewed2014-05-11T12:20:00Z
      - in: query
        name: status
        description: The state of the subscriptionactive
      - in: header
        name: X-AUTH-EMAIL
        description: Email address associated with your account
      - in: header
        name: X-AUTH-KEY
        description: API key generated on the My Account page
      responses:
        200:
          description: OK
      tags:
      - Subscriptions
  /user/billing/subscriptions/apps/:identifier:
    get:
      summary: Billing subscription details
      description: Billing subscription details
      operationId: cloudflare-app-subscription-api
      x-api-path-slug: userbillingsubscriptionsappsidentifier-get
      responses:
        200:
          description: OK
      tags:
      - Subscriptions
  /user/billing/subscriptions/zones:
    get:
      summary: List all of your zone plan subscriptions
      description: List all of your zone plan subscriptions
      operationId: cloudflare-zone-subscription-api
      x-api-path-slug: userbillingsubscriptionszones-get
      parameters:
      - in: query
        name: activated_on
        description: When the subscription was activated2014-03-01T12:20:00Z
      - in: query
        name: cancelled_on
        description: When the subscription was cancelled2014-04-01T12:20:00Z
      - in: query
        name: direction
        description: Direction to order subscriptionsdesc
      - in: query
        name: expired_on
        description: When the subscription expired2014-04-02T12:20:00Z
      - in: query
        name: expires_on
        description: When the subscription will expire2014-03-31T12:20:00Z
      - in: query
        name: match
        description: Whether to match all search requirements or at least one (any)all
      - in: query
        name: order
        description: Field to order subscriptions bystatus
      - in: query
        name: page
        description: Page number of paginated results1
      - in: query
        name: per_page
        description: Number of items per page20
      - in: query
        name: price
        description: The price of the subscription that will be billed, in US dollars20
      - in: query
        name: renewed_on
        description: When the subscription was renewed2014-05-11T12:20:00Z
      - in: query
        name: status
        description: The state of the subscriptionactive
      - in: header
        name: X-AUTH-EMAIL
        description: Email address associated with your account
      - in: header
        name: X-AUTH-KEY
        description: API key generated on the My Account page
      responses:
        200:
          description: OK
      tags:
      - Zone Subscriptions
  /user/billing/subscriptions/zones/:identifier:
    get:
      summary: Billing subscription details
      description: Billing subscription details
      operationId: cloudflare-zone-subscription-api
      x-api-path-slug: userbillingsubscriptionszonesidentifier-get
      responses:
        200:
          description: OK
      tags:
      - Zone Subscriptions
---