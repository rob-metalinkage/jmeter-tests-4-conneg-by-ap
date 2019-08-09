# jmeter-tests-4-conneg-by-ap
An Apache JMeter test for the behaviour of resources implementing "Content negotiation by profile" (https://www.w3.org/TR/dx-prof-conneg/)

## status
This will track the emerging draft recommendation.

It is fairly crude - contributions to make it easier to configure and improve reporting are welcome.

## usage
Open cneg.jmx in Apache Jmeter and update the user variables to point to a file that lists the resources you wish to check. Select "view results" and run suite. By default it will show all results.

## features
* Checks for both HHTP and Query string argument forms for negotiation
* in QSA mode it reads "alternates" view to determine all the combinations to test
* in HTTP mode it uses HTTP Link headers accessed via HTTP HEAD requests to determine all combinations
* responses are checked for correct Mime type

## possible future improvements (help welcomed)
* resolve profile URIs and get profile descriptions and validation resources - and check not just conneg function but also conformance of resources
* resolve profile URIs and check more request for more general profiles return specific profiles.
* check HTTP and QSA are equivalent
* check QSA overrides HTTP
* look in 303-redirected content for profile identification (needs a canonical encoding)
