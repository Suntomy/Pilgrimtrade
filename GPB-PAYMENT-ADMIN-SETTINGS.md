# GLOBAL PILGRIM BANK — ADMIN PAYMENT SETTINGS

## Master controls
- Master payment switch
- Master payout switch
- Emergency stop
- Administrator-only access
- Require confirmation for every switch change
- Record administrator, date, time and reason

## Payment methods
Each method has:
- Enabled / disabled
- Provider configured
- Provider connection verified
- Transaction limit
- Daily limit
- Approval requirement
- Last provider check
- Last successful transaction
- Failure status

Methods to support when provider-approved:
- Nigerian bank transfer
- Flutterwave-supported card acceptance
- Visa / Mastercard / Verve where supported
- Approved crypto payment provider, if configured

Do not assume card acceptance means card payouts are supported.

## Bank beneficiary form
- Send to
- Bank name
- Account number
- Verified account name
- Amount
- Currency
- Transaction ID
- Live date and time
- Payment status
- Receipt
- Administrator approval

Bank list must come from the approved provider.
Account name must be resolved by the provider.

## Backend security
- Enforce settings on the server, not only in the browser.
- Require authenticated administrator role.
- Store settings in persistent database.
- Never trust a client-supplied enabled flag.
- Log every setting change in an append-only audit table.
- Require idempotency for payment requests.
- Verify provider webhook signatures.
- Reconcile provider transfers against ledger entries.
- Do not store PAN, CVV or card PIN.
- Keep secrets in server-side environment variables.

## Initial safe configuration
MASTER_PAYMENTS_ENABLED=false
MASTER_PAYOUTS_ENABLED=false
BANK_TRANSFER_ENABLED=false
CARD_ACCEPTANCE_ENABLED=false
CARD_PAYOUTS_ENABLED=false
CRYPTO_PAYMENTS_ENABLED=false
BROKER_ORDERS_ENABLED=false

A method can only become active after its own provider
connection and compliance checks pass.
