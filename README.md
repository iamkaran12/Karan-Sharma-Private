# **Query Document RoomDB**

## **1. Error Response Requirements**

To ensure comprehensive and accurate API documentation, detailed error response specifications are required for all endpoints across the Distributor API.

Currently, several endpoints define only successful **(`200`)** and generic server **(`500`)** responses. For complete developer guidance and production-grade documentation, additional error handling details are necessary.

### **Required Information**

For each endpoint, please provide:

1. **All possible HTTP status codes**, including but not limited to:

   * **`400 Bad Request`**

   * **`401 Unauthorized`**

   * **`403 Forbidden`**

   * **`404 Not Found`**

   * **`409 Conflict`**

   * **`422 Unprocessable Entity`**

   * **`429 Too Many Requests`**

   * Any other custom or business-specific codes

2. **Exact JSON error response structure**, including:

   * Field names

   * Data types

   * Required vs optional fields

   * Sample values

3. **Field-level descriptions**, such as:

   * **`status`**

   * **`message`**

   * **`errorCode`**

   * **`traceId`**

   * **`executionTime`**

   * Any additional metadata fields

4. **Business-level validation errors**, including:

   * Invalid distributor credentials

   * Expired token

   * Booking not found

   * Insufficient availability

   * Invalid cancellation window

   * Rate plan mismatch

   * Duplicate reservation

   * Any domain-specific validation scenario

5. **Real-world example error responses** for:

   * Authentication failures

   * Booking validation errors

   * Pricing conflicts

   * Availability mismatches

   * Cancellation restrictions

## **2. Clarification Required: Endpoint-to-Module Mapping**

While organizing the API documentation into logical modules (Authentication, Hotels, Rooms, Products, Availability, Pricing, Booking / Reservation, Cancellation, Policies, Webhooks, Reporting, Admin), I have created a Google Sheet to track:

* Which endpoints we need to document

* Which endpoints should be excluded (e.g., deprecated or out of scope)

* Which endpoints belong under each module

However, I am facing a challenge.

The current API specification is structured using technical tags and endpoint paths. In contrast, the documentation is being organized based on business modules (such as Hotels, Rooms, Products, etc.).

For example:

* We have a module called **Hotels**

* But there is no explicit “Hotels” grouping in the API specification

* Property search, filters, logos, and related endpoints may logically fall under Hotels

* However, there is no clear mapping that confirms this

Because of this, it is difficult to confidently assign endpoints to the correct business module.

I have attached the Google Sheet structured according to the agreed slices:

* Authentication

* Hotels

* Rooms

* Products

* Availability

* Pricing

* Booking / Reservation

* Cancellation

* Policies

* Webhooks

* Reporting

* Admin

The goal of this sheet is to clearly define the documentation scope and ensure everything is aligned correctly.

Could you please review the sheet and:

1. Add or confirm the endpoints under each module

2. Indicate which endpoints should be excluded

3. Confirm if any additional endpoints need to be included

This clarification will help ensure that we document only the relevant APIs and structure them correctly according to the intended business modules.

**Here is the Google Sheet Link:** [https://docs.google.com/spreadsheets/d/1QkLIta8cExyik1l8i1zbYBkZqlKjMOJmZl0YLzIMAWc/edit?usp=sharing](https://docs.google.com/spreadsheets/d/1QkLIta8cExyik1l8i1zbYBkZqlKjMOJmZl0YLzIMAWc/edit?usp=sharing) 
