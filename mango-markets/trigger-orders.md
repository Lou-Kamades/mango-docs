# 📈 Trigger Orders

Trigger Orders allow user to place orders that execute under certain price conditions. Currently Stop Loss and Take Profit orders are supported.

### How to Place a Trigger Order
The Trigger Order UI is located on the swap page -- TODO

### How do Trigger Orders Work
Trigger orders are executed by liquidators when the specified trigger price is reached according to the oracles of tokens involed in the order. Because liquidators are responsible for triggering the orders, if there are not enough liquidators or they are not well capitalized the orders may not trigger when expected. Additionally, since liquidators may be delayed in triggering orders, the exact execution price is not guaranteed.

