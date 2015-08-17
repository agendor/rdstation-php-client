#Usage
```php
require("RDStationAPI.class.php");
$rdAPI = new RDStation("RD_PRIVATE_TOKEN", "RD_TOKEN");

//SEND NEW LEAD TO RD STATION
$return1 = $rdAPI->sendNewLead("customer@customer.com", array(
	"nome" => "Julio",
	"cargo" => "Cofounder",
	"empresa"=> "Agendor",
	"identificador" => "contact-form",
	"subscribe_newsletter" => true //custom data is accepted
));

//UPDATE LEAD STATUS TO 'won'
$return2 = $rdAPI->updateLeadStatus("customer@customer.com", 'won', 999.99);

//UPDATE LEAD STATUS TO 'lost'
$return3 = $rdAPI->updateLeadStatus("customer@customer.com", 'lost', 999.99, 'Lost reason');

//UPDATE LEAD FUNNEL STAGE AND OPPORTUNITY FLAG
$return4 = $rdAPI->updateLeadStageAndOpportunity("customer@customer.com", 1, true);
```
