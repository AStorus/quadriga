Getting Started
===============

Here is an example showing how the **quadriga** client can be initialized and
used:

.. code-block:: python

    from quadriga import QuadrigaClient

    # Initialize the QuadrigaCX client
    client = QuadrigaClient(
        api_key='api_key',
        api_secret='api_secret',
        client_id='client_id',
        default_book='btc_usd'
    )

    # Get the latest trading summary
    client.get_ticker()

    # Get all public open orders
    client.get_public_orders()

    # Get recently completed public trades
    client.get_public_trades()

    # Get the user's open orders
    client.get_user_orders()

    # Get the user's completed trades
    client.get_user_trades()

    # Get the user's account balance
    client.get_account_balance()

    # Buy 10 bitcoins at the market price
    client.buy_market_order(10)

    # Buy 10 bitcoins at limit price of $1000 USD
    client.buy_limit_order(10, 1000)

    # Sell 20 bitcoins at the market price
    client.sell_market_order(20)

    # Sell 20 bitcoins at limit price of $1300 USD
    client.sell_limit_order(20, 1300)

    # Look up an order by its ID
    client.lookup_order('order_id')

    # Cancel an open order by its ID
    client.cancel_order('order_id')

    # Return the deposit address used for funding bitcoin
    client.get_deposit_address('bitcoin')

    # Return the deposit address used for funding ether
    client.get_deposit_address('ether')

    # Return the deposit address used for funding litecoin
    client.get_deposit_address('litecoin')

    # Withdraw 15 bitcoins from QuadrigaCX to the given address
    client.withdraw('bitcoin', 15, 'my_bitcoin_withdrawal_address')

    # Withdraw 20 ethers from QuadrigaCX to the given address
    client.withdraw('ether', 20, 'my_ether_withdrawal_address')

    # Withdraw 50 litecoins from QuadrigaCX to the given address
    client.withdraw('litecoin', 50, 'my_litecoin_withdrawal_address')

Refer to the :ref:`API` for more details.
