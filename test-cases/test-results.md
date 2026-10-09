# Home Credit LAP Voice Agent — Test Results

## Overview
The voice agent was built using Retell AI to conduct preliminary Loan Against Property (LAP) eligibility checks.

## Test Scenarios

### 1. Eligible Customer
- Property: Residential house
- Ownership: Jointly owned with wife
- Original documents: Available
- Requested loan amount: ₹50 lakh
- Occupation: Salaried
- Income mode: Direct bank deposit
- Estimated property value: ₹1 crore
- Requested tenure: 10 years
- **Expected result:** Preliminary eligibility message after all required values are confirmed.
- **Observed result:** The agent gave a preliminary eligibility message and stated that final approval depends on verification.
- **Status:** Passed

### 2. Agricultural Property
- **Input:** Customer offers agricultural land as security.
- **Expected result:** Immediate polite disqualification.
- **Observed result:** The agent stated that agricultural property was not eligible and ended the qualification flow.
- **Status:** Passed

### 3. Existing Loan / EMI Reduction
- **Input:** Customer already has a loan against the property and wants a lower EMI or balance transfer.
- **Expected result:** Stop fresh-loan qualification and route the customer through the configured specialist workflow.
- **Observed result:** The agent gave the specialist-routing message. Actual transfer execution must be verified separately.
- **Status:** Conversation passed; integration unverified

### 4. Requested Amount Above ₹75 Lakh
- **Input:** Customer requests ₹90 lakh and declines the ₹75 lakh alternative.
- **Expected result:** Explain the offer limit and end the qualification flow after refusal.
- **Observed result:** The agent explained the maximum amount and ended the conversation after the customer declined.
- **Status:** Passed

### 5. Multiple Disqualification Conditions
- **Input:** Customer states that original documents are unavailable and requests a one-year tenure.
- **Expected result:** Explain confirmed ineligibility reasons and end the call.
- **Observed result:** The agent identified both disqualifying conditions.
- **Status:** Passed

## Limitations
- Speech recognition can misinterpret unclear customer audio, so ambiguous answers require clarification.
- Preliminary eligibility does not guarantee final loan approval.
- Specialist transfer and callback execution must be verified through the actual configured workflow.
