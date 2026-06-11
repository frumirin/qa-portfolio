Bug Report: Phone Number Validation Rejects Valid Numbers Containing Consecutive Zeros

Severity: High

Priority: High

Environment:
Website: Calm es simple (calmessimple.com.ar)

Feature: Checkout — contact/payment information form

Location: Argentina

Summary:
The phone number validation incorrectly rejects valid Argentine phone numbers that contain four or more consecutive zeros, preventing users from completing checkout.

Steps to Reproduce:
Navigate to checkout on calmessimple.com.ar
Enter a valid Argentine phone number containing four consecutive zeros
Attempt to proceed

Expected Result:
The form accepts any valid phone number regardless of digit patterns.

Actual Result:
Form displays "Invalid phone number" and blocks the user from proceeding.

Root Cause (hypothesis):
Validation logic likely uses a regex or heuristic rule that flags repeated zeros as indicative of a fake or test number, rather than validating against real Argentine phone number formats.

Impact:
Users with legitimate phone numbers containing consecutive zeros are completely blocked from completing a purchase and must use an alternative number — directly impacting conversion rate.