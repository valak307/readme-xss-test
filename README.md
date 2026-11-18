# readme-xss-test

Authorized bug bounty test component for the ESP Component Registry README rendering (L5). Own namespace: valak307. This README intentionally contains HTML/JavaScript test payloads to check whether the registry sanitizes README rendering. Payloads are harmless alert(1) proofs only.

## Payload 1 - img onerror

<img src=x onerror=alert(1)>

## Payload 2 - script tag

<script>alert(1)</script>

## Expected

If sanitized, both payloads should appear as escaped text or be stripped, and no alert dialog should appear.
