Project: Develop a FIX client (https://en.wikipedia.org/wiki/Financial_Information_eXchange) that can send random orders to a FIX server and calculate certain statistics related to the order flow.

FIX version: 4.2

1. Generate Order and save the log file: FIX_LOG_GENERATION.ipynb
   1) Handle basic FIX flows: Logon, Seq Number handling
   2) Able to send below message to server:
      - New Order (35=D): Limit Order or Market Order. You can put a random price for Limit Order.
      - Order Cancel Request (35=F)
      - Do not send another other request
   3) Able to handle below message from server:
      - Reject (35=3)
      - Execution Report (35=8)
      - Order Cancel Reject (35=9)
   4) Send 1000 random orders for MSFT, AAPL, and BAC. One side can be BUY, SELL, or SHORT. It could be a limit or a market order. Send 1000 orders within a 5 minutes period from when the application starts. And, need to randomly cancel them within 5 minutes from when you send the order.
  