# Responses
The response in case of a HTTP Status Code 200 will be a single JSON object containing the information of a vessel and its stays of the last 2 months or upcoming ones in the Port of Antwerp. The structure of this is specified in the swagger file of this API. Only non-null fields will be returned.

## Vessel properties
| ------------- |-------------| -----| ---- |
| vesselName | String | | The name of the seagoing vessel  |
| imoNumber  | Number | | The IMO number  |
| vesselType  | String | Apics coded  | Apics vessel type  |
| flag | String | ISO 3166  | ISO code of the flag  |
| countryEn | String | | Full name of the country (flag) in English |
| loa | Number | | Length over all |

## Stay properties

| ------------- |-------------| -----| ---- |
| stayNumber | String  |  | Stay number |
| agentCode | String | Apics coded | Apics code of the shipping agent |
| agentName | String | | Full name of the shipping agent |
| eta | Date | yyyy-MM-ddTHH:mm:ssZ (UTC) | Estimated time of arrival |
| ata | Date | yyyy-MM-ddTHH:mm:ssZ (UTC) | Actual time of arrival |
| etd | Date | yyyy-MM-ddTHH:mm:ssZ (UTC) | Estimated time of departure |
| berthDeparture | String | Apics berth code | Berth of departure in the Port of Antwerp |
| originFull | String | | Full name of the previous port |
| destinationFull | String | | Full name of the next port |