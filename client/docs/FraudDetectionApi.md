# CloudmersiveFrauddetectionApiClient::FraudDetectionApi

All URIs are relative to *https://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**document_detect_fraud**](FraudDetectionApi.md#document_detect_fraud) | **POST** /fraud-ai/detection/document | AI Fraud Detection for Documents
[**document_detect_fraud_advanced**](FraudDetectionApi.md#document_detect_fraud_advanced) | **POST** /fraud-ai/detection/document/advanced | Advanced AI Fraud Detection for Documents


# **document_detect_fraud**
> FraudDetectionResult document_detect_fraud(opts)

AI Fraud Detection for Documents

Perform fraud detection and classification on input document and user context.  Input document formats supported include DOCX, PDF, PNG and JPG.

### Example
```ruby
# load the gem
require 'cloudmersive-frauddetection-api-client'
# setup authorization
CloudmersiveFrauddetectionApiClient.configure do |config|
  # Configure API key authorization: Apikey
  config.api_key['Apikey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['Apikey'] = 'Bearer'
end

api_instance = CloudmersiveFrauddetectionApiClient::FraudDetectionApi.new

opts = { 
  input_file: File.new('/path/to/file.txt') # File | Input document, or photos of a document, to perform fraud detection on
}

begin
  #AI Fraud Detection for Documents
  result = api_instance.document_detect_fraud(opts)
  p result
rescue CloudmersiveFrauddetectionApiClient::ApiError => e
  puts "Exception when calling FraudDetectionApi->document_detect_fraud: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **input_file** | **File**| Input document, or photos of a document, to perform fraud detection on | [optional] 

### Return type

[**FraudDetectionResult**](FraudDetectionResult.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json



# **document_detect_fraud_advanced**
> AdvancedFraudDetectionResult document_detect_fraud_advanced(opts)

Advanced AI Fraud Detection for Documents

Perform advanced fraud detection and classification on input document and user context.  Input document formats supported include DOCX, PDF, PNG and JPG.

### Example
```ruby
# load the gem
require 'cloudmersive-frauddetection-api-client'
# setup authorization
CloudmersiveFrauddetectionApiClient.configure do |config|
  # Configure API key authorization: Apikey
  config.api_key['Apikey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['Apikey'] = 'Bearer'
end

api_instance = CloudmersiveFrauddetectionApiClient::FraudDetectionApi.new

opts = { 
  user_email_address: 'user_email_address_example', # String | User email address for context (optional)
  user_email_address_verified: true, # BOOLEAN | True if the user's email address was verified (optional)
  input_file: File.new('/path/to/file.txt') # File | Input document, or photos of a document, to perform fraud detection on
}

begin
  #Advanced AI Fraud Detection for Documents
  result = api_instance.document_detect_fraud_advanced(opts)
  p result
rescue CloudmersiveFrauddetectionApiClient::ApiError => e
  puts "Exception when calling FraudDetectionApi->document_detect_fraud_advanced: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_email_address** | **String**| User email address for context (optional) | [optional] 
 **user_email_address_verified** | **BOOLEAN**| True if the user&#39;s email address was verified (optional) | [optional] 
 **input_file** | **File**| Input document, or photos of a document, to perform fraud detection on | [optional] 

### Return type

[**AdvancedFraudDetectionResult**](AdvancedFraudDetectionResult.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json



