# 💸 Funding

* Funding is paid continuously and is automatically added to the user's `Unsettled Pnl`
* To see past funding earned, visit the Account page in the UI.

Funding is computed continuously as a daily difference in the index price and the current book price (current mid). The `UpdateFunding` instruction is called by the Keeper roughly every 5 seconds and so funding is paid out roughly every 5 seconds. The calculation is as follows:

```
book_price = (bid + ask) / 2
diff = clamp(book_price / index_price - 1, -0.05, 0.05)
time_factor = (now - last_updated) / TIME_IN_DAY
funding = diff * time_factor * contract_size * index_price
```
