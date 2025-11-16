# CloudmersiveFrauddetectionApiClient::AdvancedFraudDetectionResult

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**successful** | **BOOLEAN** | True if successful, false otherwise | [optional] 
**clean_result** | **BOOLEAN** | True if the document is clean, false if fraud threats were found | [optional] 
**fraud_risk_level** | **Float** | Overall fraud risk level between 0.0 and 1.0 | [optional] 
**contains_financial_liability** | **BOOLEAN** | True if the document contains financial liability | [optional] 
**contains_sensitive_information_collection** | **BOOLEAN** | True if the document contains sensitive data collection from the recipient | [optional] 
**contains_asset_transfer** | **BOOLEAN** | True if the document contains an asset transfer | [optional] 
**contains_purchase_agreement** | **BOOLEAN** | True if the document contains a purchase agreement | [optional] 
**contains_employment_agreement** | **BOOLEAN** | True if the document contains an employment agreement | [optional] 
**analysis_rationale** | **String** | Rationale on why the document was classified as such | [optional] 


