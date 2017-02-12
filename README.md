## Bid statistics and details

Information on bids submitted as part of a contracting process is important for many forms of analysis, including:

* Market analysis for understanding the competitiveness of a given marketplace;
* Red flag analysis for understanding potential corruption risks; and
* Value for money analysis;

Regulatory regimes vary on the extent to which they allow information on bidding to be proactively published, and at what point in the procurement process. In some systems and processes, a list of invited bidders will be published at the start of tendering, and full details and documents on the bids recieved may be disclosed when evaluation is complete. In other systems, only summary statistics on the number of bids received may be made public.

The OCDS bid extension introduces a new, flexible, top-level section to each contracting process to capture bidding information. Implementers will need to assess which fields are applicable to their local regulatory regime, and to local use-cases.

### Bid Statistics

The ```bids/bidStatistics``` array can block can be used to represent key statistical information about the number of bids and bidders. Each entry in the array is a ```BidStatistic``` object containing at least:

* An identifier
* A measure, from the bidStatistics codelist
* A value for that measure

| Category | Code                | Title                                     | Description                                                                                                                                | Min                                                                                                     | Max | Required by |    | 
|----------|---------------------|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|-----|-------------|----| 
| bids     | requests            | Requests to Participate                   | The total number of unique requests to participate received                                                                                |                                                                                                         |     | EU          |    | 
| bids     | bids                | Bids                                      | The total number of unique bids received (prior to any being discounted for not meeting essential criteria).                               |                                                                                                         |     | EU          |    | 
| bids     | validBids           | Valid Bids                                | "The total number of unique bids received that were considered valid against relevant criteria (either of the bidder                       |  or the bid submission itself). All valid bids should be consider during the tender evaluation stage. " |     |             |    | 
| bidders  | bidders             | Bidders                                   | The total number of unique organiastions or consortia submitting bids  (prior to any being discounted for not meeting essential criteria). |                                                                                                         |     |             |    | 
| bidders  | qualifiedBidders    | Qualified Bidders                         | The total number of unique organiastions or consortia passing the qualification stage of the evaluation process.                           |                                                                                                         |     |             |    | 
| bidders  | disqualifiedBidders | Disqualified Bidders                      | The total number of unique organiastions or consortia that did not pass the qualification stage of the evaluation process.                 |                                                                                                         |     |             |    | 
| EU       | electronicBids      | Electronic Bids                           | The number of bids received by electronic means.                                                                                           |                                                                                                         |     | EU          |    | 
| EU       | smeBids             | Bids from SMEs                            | The number of bids received from Small and Medium Sized Enterprises                                                                        |                                                                                                         |     | EU          |    | 
| EU       | foreignBids         | Bids from Foreign Firms                   | The number of bids received from bidders from outside the country where the tender is issued.                                              |                                                                                                         |     | EU          |    | 
| EU       | foreignBidsFromEU   | Bids from firms in other EU Member States | "The number of bids received from bidders from outside the country where the tender is issued                                              |  but based within an EU Member State."                                                                  |     |             | EU | 


### Bid Detail

The ```bids/details``` array is used to provide one or more ```Bid``` objects, each representing a unique bid received. 

### ToDo

* [ ] Demonstrate mapping between ```bid/details``` and statistics;
* [ ] Distinguish between bids for qualification, and bids at a later round of the process;
* [ ] Ensure all EU-required bidding parameters have been captured

### Schema 

```eval_rst
.. extensiontable::
   :extension: bids
```

