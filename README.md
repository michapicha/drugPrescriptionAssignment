# drugPrescriptionAssignment

##Assubmptions:

Each medicine is has a unique name and relates to one or multiple codes.
In the interaction section when closing the prescription - each group of codes is validated against the interaction drugs api.

For example: 

ADVIL (Oral Liquid) has 2 RXCUIS codes: https://clinicaltables.nlm.nih.gov/api/rxterms/v3/search?terms=ADVIL%20(Oral%20Liquid)&ef=RXCUIS
RXCUIS codes: "731531", "206878"

Simvastatin (Oral Liquid) has 2 RXCUIS codes as well: https://clinicaltables.nlm.nih.gov/api/rxterms/v3/search?terms=Simvastatin%20(Oral%20Liquid)&ef=RXCUIS
RXCUIS codes: "1790679", "1944264"

The close prescription route will check the product of the code lists as follows:
 "731531" with "1790679"
 "206878" with "1790679"
 "731531" with "1944264"
 "206878" with "1944264"