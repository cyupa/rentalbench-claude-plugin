# Recovery

- For an expired or revoked connection, reconnect in Claude.
- For `insufficient_scope`, reconnect with write permission before requesting a change.
- For access or membership errors, check the selected location and the connected
  staff role. Ask the workspace administrator for access when needed.
- For `billing_required` or plan limits, use the authenticated RentalBench
  billing overview to see the current subscription and available actions.
- For `validation_failed`, identify the returned fields and ask for the missing
  information. Get consent, addresses and signatures from their proper sources.
- For `invalid_transition`, read the current order and item states. Cancel
  eligible orders before checkout. Use returns for checked-out rentals.
- For `return_requires_rentalbench`, use the returned order link to complete the
  return and online refund in RentalBench.
- For a timeout or provider error, read the affected record before retrying a
  write. Report the last confirmed state.

Use the appropriate lifecycle, custom field and comment tools to update
orders. Customer records can be managed individually.
