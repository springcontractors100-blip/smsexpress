# Payment security
- [x] Remove simulated top-ups; lock browser access to credits and settlement.
- [x] Remove the old payment provider's code and callback; no provider secrets or hosted functions existed.
- [x] Pesapal v3 production checkout and verified IPN settlement.
- [x] Reset current balance to 6.
- [x] Production Pesapal credentials saved; real checkout renders MTN and Airtel, with no payment approved and balance still 6.
- [ ] End-to-end completed payment/IPN test — requires publishing the new callback and a user-approved Mobile Money payment.