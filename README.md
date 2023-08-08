# 🛠️ GymSubscription 🛠️ 

GymSubscription is an application built on DAML that offers a platform for inquiry and getting the membership of the Gym.

### I. Overview
This project was created by using the `empty-skeleton` template.
In this application member can enquiry for the gym , they can go for free trail and if they like the service then can get the subscription for the Gym.
Members can make payment for the subscription of the Gym, extend their membership , update subscription plan as per their need. Gym owner can confirm the payment made by
member and owner can terminate the membership of any member.

### II. Workflow
1. Member can enquiry for the gym through GymEnquiry template.
2. Member get the subscription through GetSubscription choice in the template GymEnquire.
3. Member can go for free trail also through FreeTrial choice in the template GymEnquire.
4. Member can submit the payment for the subscription of Gym through PayMembershipFee choice.
5. Gym Owner can confirm the payment through ConfirmPayment choice in the template MemberPayment.
6. If member wants then can extend the membership by ExtendMembership choice in the template GymSubscription.
7. Member can update their subscription plan through UpdateSubscriptionPlan choice in the template GymSubscription.
8. Gym owner can terminate any membership by TerminateMembership choice in the template GymSubscription.

### III. Challenge(s)
* The project was created by using `empty-skeleton` and the following was removed from `daml.yaml`:
```
sandbox-options:
   - --wall-clock-time
```
and the following was added:

```
init-script: Test:testGym
exposed-modules:
  - Main

```

### IV. Compiling & Testing
To compile and test, run the pre-written script in the `Test.daml` under /daml OR run:
```
$ daml start
```
Test coverage report
```
$ daml test --show-coverage

**Test Summary
**
daml/Test.daml:setupParties: ok, 0 active contracts, 0 transactions.
daml/Test.daml:testGym: ok, 0 active contracts, 12 transactions.
Modules internal to this package:
- Internal templates
  3 defined
  3 (100.0%) created
  internal templates never created: 0
- Internal template choices
  12 defined
  9 ( 75.0%) exercised
  internal template choices never exercised: 3
    Main:GymEnquire:Archive
    Main:GymSubscription:Archive
    Main:MemberPayment:Archive
- Internal interface implementations
  0 defined
    0 internal interfaces
    0 external interfaces
- Internal interface choices
  0 defined
  0 (100.0%) exercised
  internal interface choices never exercised: 0
Modules external to this package:
- External templates
  0 defined
  0 (100.0%) created in any tests
  0 (100.0%) created in internal tests
  0 (100.0%) created in external tests
  external templates never created: 0
- External template choices
  0 defined
  0 (100.0%) exercised in any tests
  0 (100.0%) exercised in internal tests
  0 (100.0%) exercised in external tests
  external template choices never exercised: 0
- External interface implementations
  0 defined
- External interface choices
  0 defined
  0 (100.0%) exercised in any tests
  0 (100.0%) exercised in internal tests
  0 (100.0%) exercised in external tests
  external interface choices never exercised: 0
