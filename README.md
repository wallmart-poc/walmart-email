# walmart-email · Email Service

Order confirmation email gRPC service. Sends post-purchase notification emails to customers after a successful checkout.

## Stack
- **Language:** Python 3.11
- **Framework:** gRPC (`grpcio`)
- **Templating:** Jinja2 (`templates/confirmation.html`)

## API
Implements `EmailService` from `demo.proto`:
- `SendOrderConfirmation(SendOrderConfirmationRequest) → Empty`

In the demo environment emails are logged rather than delivered — no real SMTP connection is made.

## Running locally
```bash
pip install -r requirements.txt
python email_server.py
```
Service listens on port `8080` by default (`EMAIL_SERVICE_PORT`).

## Dependencies
None — standalone service, no outbound calls to other internal services.
