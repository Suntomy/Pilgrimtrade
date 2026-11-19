# GLOBAL PILGRIM BANK PLC — VAULT ADMIN UPGRADE

Owner / Proprietor: Olawale Abdul-Ganiyu Adeshina
Prepared for: Adegan Global Enterprise

## 1. Business identity supplied by project owner

Registered name: Global Pilgrim Bank
Registration reference supplied:
BN-99-88-27364-GP

Incorporation date supplied:
24 October 2023

Trademark asset reference supplied:
GPB-TM-0X9030277275

Trademark status supplied:
WIP_SYNCED — pending independent verification

Copyright / sovereign brand:
Owner-supplied intellectual property claims.
Do not represent as registered or officially verified without evidence.

## 2. Tax and compliance

Tax details must be stored only in a protected server-side
secret store or authorised compliance system.

Never place tax IDs, verification PINs, passwords or API
secrets in frontend HTML, JavaScript, logs or Git.

Compliance status must be obtained from an authorised
verification source. Do not assume "100% cleared".

## 3. Nigerian bank withdrawal dashboard

Required administrator fields:

- Send to
- Bank name
- Account number
- Verified account name
- Amount
- Currency
- Transaction reference
- Transaction ID
- Live transaction date
- Live transaction time
- Payment status
- Receipt
- Administrator approval
- Audit history

Bank list:
Retrieve dynamically from the approved payment provider,
using the existing /api/ng/banks endpoint.

Beneficiary:
Use the provider's official account-resolution endpoint.
Do not accept an unverified account name as proof.

Withdrawal:
Keep disabled until authentication, authorisation,
provider approval, idempotency, verified balance,
webhook verification and reconciliation are implemented.

Never store card PIN, CVV or full card credentials.

## 4. Global Pilgrim Bank Vault

Required controls:

- Authenticated administrator access
- Role-based permissions
- Master payout switch
- Per-payment-method switches
- Per-transaction and daily limits
- Two-person approval for high-value transfers
- Emergency stop
- Immutable transaction audit records
- Secure receipt storage
- Encrypted backups
- Login and configuration-change history

## 5. Floating international market terminal

Display live provider-sourced data with:

- Market name and symbol
- Bid and ask where available
- Last price
- Price timestamp
- Data provider
- Connection status
- RSI and other advisory indicators
- Market-data error and stale-data warnings

Do not fabricate prices, fills, profits or balances.
Do not execute orders without a verified broker connection.

## 6. Network and international settlement

NIBSS/NIP, SWIFT GPI, UETR, ISO 20022,
AES-256-GCM and settlement references are
configuration targets until independently verified.

A reference string alone does not establish a live connection.

## 7. Deployment and integrity

- Keep private credentials outside public folders.
- Protect administrator routes with server-side authentication.
- Log configuration changes.
- Back up before every upgrade.
- Verify file hashes after installation.
- Keep order execution and withdrawals disabled until
  the relevant providers and security controls pass testing.
