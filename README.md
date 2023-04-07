# Hello-world
Just another repository
route('/buy', methods=['POST'])
def buy_currency():
    data = request.get_json()
    currency = data['currency']
    amount = data['amount']
    payment_currency = data['payment_currency']
    update_wallet_balance(wallet_address, currency, new_balance)
    update_wallet_balance(wallet_address, payment_currency, payment_currency_balance - payment_amount)
    
    return jsonify({'success': True})

import requests
import json

api_url = "https://api.coinbase.com/v2"
api_key = "<your api key>"
api_secret = "<your api secret>"
headers = {"CB-ACCESS-KEY": api_key, "CB-ACCESS-SIGN": api_secret}

def convert_btc_to_eth(amount):
    # Convert BTC to ETH using Coinbase API
    url = api_url + "/accounts/<BTC account id>/buys"
    data = {"amount": amount, "currency": "BTC", "payment_method": "<payment method id>"}
    response = requests.post(url, data=json.dumps(data), headers=headers)
    if response.status_code == 200:
        buy_id = response.json()["data"]["id"]
        url = api_url + "/accounts/<ETH
