#Usage
```php
require("RDStationAPI.class.php");
$rdAPI = new RDStationAPI("RD_PRIVATE_TOKEN", "RD_TOKEN");

//SEND NEW LEAD TO RD STATION
$return1 = $rdAPI->sendNewLead("customer@customer.com", array(
	"name" => "Julio",
	"job_title" => "Cofounder",
	"company"=> "Agendor",
	"identificador" => "contact-form",
	"subscribe_newsletter" => true //custom data is accepted
));

// UPDATE ANY LEAD INFO
$return2 = $rdAPI->updateLead("customer@customer.com", array(
    "lead" => array(
      "name" => "New Name",
      "company"=> "Agendor",
      "opportunity" => true,
      "lifecycle_stage" => 1,
      "Any Custom Field" => "Custom Field Value",
    )
));

//UPDATE LEAD STATUS TO 'won'
$return3 = $rdAPI->updateLeadStatus("customer@customer.com", 'won', 999.99);

//UPDATE LEAD STATUS TO 'lost'
$return4 = $rdAPI->updateLeadStatus("customer@customer.com", 'lost', 999.99, 'Lost reason');

//UPDATE LEAD FUNNEL STAGE AND OPPORTUNITY FLAG
$return5 = $rdAPI->updateLeadStageAndOpportunity("customer@customer.com", 1, true);
```
