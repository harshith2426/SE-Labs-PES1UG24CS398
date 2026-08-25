# Use-Case Flow: UC-01 Submit Lost-Baggage Claim

## Use Case ID

UC-01

## Use Case Name

Submit Lost-Baggage Claim

## Primary Actor

Passenger

## Preconditions

- The Passenger can access the Airport Lost Luggage Claim & Tracking Portal.
- The Passenger has the bag tag, flight details, and contact information required for the claim.

## Postconditions

- A valid lost-baggage claim is recorded with a unique claim reference number.
- The claim is cross-referenced against available luggage scan logs.

## Main Success Scenario

1. The Passenger selects the **Submit Lost-Baggage Claim** option.
2. The system displays a form for bag tag, flight details, and contact information.
3. The Passenger enters the required claim details and submits the form.
4. The system validates the required information and bag-tag format.
5. The system creates the lost-baggage claim and assigns a unique claim reference number.
6. The system performs UC-02, **Cross-Reference Scan Logs**, using the submitted bag tag.
7. The system displays the claim reference number and current claim status to the Passenger.
8. The use case ends successfully.

## Alternate Flow

**4a. Invalid or incomplete claim details**

1. The system detects that a required field is missing or that the bag-tag format is invalid.
2. The system displays an error message identifying the field that must be corrected.
3. The Passenger corrects the details and resubmits the form.
4. The flow resumes at Step 4 of the Main Success Scenario.
