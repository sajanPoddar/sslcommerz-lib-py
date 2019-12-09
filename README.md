# SSLCOMMERZ PAYMENT GATEWAY

**Note**: If you're using this wrapper with our sandbox environment `issandbox` is true and live `issandbox` is false. (Details: [Test Or Sandbox Account](https://developer.sslcommerz.com/)).
settings = { 'store_id': 'testbox', 'store_pass': 'qwerty', 'issandbox': True }
sslcommerz = SSLCOMMERZ(settings)

## Installation

`pip install sslcommerz-lib`

## Authentication Keys

You can find your store_id and store_pass at the API Documentation Page.
Create an account on SSLCOMMERZ, log in and visit this link:
https://developer.sslcommerz.com/registration/

## Usage

### Create a Initial Payment Request Session 

    from sslcommerz-lib import SSLCOMMERZ 
    settings = { 'store_id': 'testbox', 'store_pass': 'qwerty', 'issandbox': True }
    sslcommez = SSLCOMMERZ(settings)
    post_body = {}
    post_body['total_amount'] = 100.26
    post_body['currency'] = "BDT"
    post_body['tran_id'] = "12345"
    post_body['success_url'] = "your success url"
    post_body['fail_url'] = "your fail url"
    post_body['cancel_url'] = "your cancel url"
    post_body['emi_option'] = 0
    post_body['cus_name'] = "test"
    post_body['cus_email'] = "test@test.com"
    post_body['cus_phone'] = "01700000000"
    post_body['cus_add1'] = "customer address"
    post_body['cus_city'] = "Dhaka"
    post_body['cus_country'] = "Bangladesh"
    post_body['shipping_method'] = "NO"
    post_body['multi_card_name'] = ""
    post_body['num_of_item'] = 1
    post_body['product_name'] = "Test"
    post_body['product_category'] = "Test Category"
    post_body['product_profile'] = "general"


    response = sslcommez.createSession(post_body)
    print(response)


