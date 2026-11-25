# ColdBox Telesign Module

A ColdBox module that provides integration with the Telesign API for phone verification, messaging, and identity services.

## Installation

Add this module to your ColdBox application by including it in your `box.json` dependencies or manually installing it in your `modules` directory.

## Configuration

Configure the module in your `ModuleConfig.cfc`:

```cfml
this.telesign = {
    customerID = "your_customer_id",
    apiKey = "your_api_key"
};
```

## Usage

Inject the API service into your handlers or services:

```cfml
property name="telesignAPI" inject="telesign:models.API";

// Phone ID lookup
var result = telesignAPI.phoneID("1234567890");

// Get phone number info
var phoneInfo = telesignAPI.getPhoneNumber("1234567890");
```

## Features

- Phone ID lookups
- Phone number validation
- Telesign API integration
- Support for local development

## Module Properties

- **Name:** telesign
- **Version:** 2.0.0
- **Entry Point:** /telesign
- **Model Namespace:** telesign

## Requirements

- ColdBox Framework

## Author

**DealStream**

## License

Copyright (c) 2026 DealStream. All rights reserved.

## Documentation

For more information, visit the [Telesign API Documentation](https://developer.telesign.com/).
