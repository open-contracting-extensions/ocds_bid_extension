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

EMBED BID STATISTICS CODELIST HERE

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

