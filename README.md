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
