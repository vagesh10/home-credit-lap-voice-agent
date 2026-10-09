# Home Credit LAP Voice Agent

An AI-powered voice agent built using Retell AI to conduct preliminary Loan Against Property (LAP) eligibility checks through natural conversations.

## Overview

The agent verifies customer availability, explains the LAP offer, collects eligibility information, handles disqualification scenarios, and provides preliminary qualification outcomes.

## Key Features

- Natural conversational qualification flow
- Supports residential, commercial, and industrial property types
- Checks ownership and original property document availability
- Validates requested loan amount against the ₹75 lakh offer limit
- Checks occupation and bank-based income receipt
- Collects estimated property value and repayment tenure
- Handles agricultural-property disqualification
- Detects existing property loans and EMI-reduction requests
- Uses a final eligibility gate before qualifying a customer
- Avoids promising final loan approval

## Eligibility Rules

- Maximum loan amount under the offer: ₹75 lakh
- Eligible property types: residential, commercial, and industrial
- Original property documents must be available
- Eligible occupation: salaried or self-employed
- Income must be received through a bank account
- Eligible repayment tenure: 3–15 years, inclusive
- Joint ownership is permitted under the configured preliminary rules

## Repository Structure

- [`prompts/system-prompt.md`](prompts/system-prompt.md) — System prompt for the voice agent
- [`test-cases/eligible-customer-transcript.txt`](test-cases/eligible-customer-transcript.txt) — Eligible-customer call transcript
- [`test-cases/recordings-and-transcripts.md`](test-cases/recordings-and-transcripts.md) — Recording and transcript documentation
- [`test-cases/test-results.md`](test-cases/test-results.md) — Test scenarios, observed outcomes, and limitations
- [`test-cases/`](test-cases/) — Audio recording and other test artifacts

## Testing

The agent was tested with eligible-customer, agricultural-property, existing-loan, excessive-loan-amount, and multiple-disqualification scenarios.

See [`test-cases/test-results.md`](test-cases/test-results.md) for the recorded test outcomes and limitations.

## Important Notes

This agent performs preliminary qualification only. It does not approve or guarantee loans. Final approval is subject to verification.

Actual specialist transfers and callbacks depend on the configured Retell functions or connected workflows.

## Technology

- Retell AI
- Large language model (LLM)
- Prompt-based conversational logic
- Voice interaction and call transcription

## Author

Vagesh Kumar Surla
