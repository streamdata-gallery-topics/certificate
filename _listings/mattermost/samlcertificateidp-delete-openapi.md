---
swagger: "2.0"
x-collection-name: Mattermost
x-complete: 0
info:
  title: Mattermost API Remove IDP certificate
  description: |-
    Delete the current IDP certificate being used with your SAML configuration. This will also disable SAML on your system as this certificate is required for SAML.
    ##### Permissions
    Must have `manage_system` permission.
  termsOfService: https://about.mattermost.com/default-terms/
  version: 4.0.0
host: your-mattermost-url.com
basePath: /api/v4
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /saml/certificate/idp:
    post:
      summary: Upload IDP certificate
      description: |-
        Upload the IDP certificate to be used with your SAML configuration. This will also set the filename for the IdpCertificateFile setting in your `config.json`.
        ##### Permissions
        Must have `manage_system` permission.
      operationId: upload-the-idp-certificate-to-be-used-with-your-saml-configuration-this-will-also-set-the-filename-f
      x-api-path-slug: samlcertificateidp-post
      parameters:
      - in: formData
        name: certificate
        description: The IDP certificate file
      responses:
        200:
          description: OK
      tags:
      - Upload
      - IDP
      - Certificate
    delete:
      summary: Remove IDP certificate
      description: |-
        Delete the current IDP certificate being used with your SAML configuration. This will also disable SAML on your system as this certificate is required for SAML.
        ##### Permissions
        Must have `manage_system` permission.
      operationId: delete-the-current-idp-certificate-being-used-with-your-saml-configuration-this-will-also-disable-sa
      x-api-path-slug: samlcertificateidp-delete
      responses:
        200:
          description: OK
      tags:
      - Remove
      - IDP
      - Certificate
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---