Here are the answers to your questions:

Test Case Titles:
1. Registration with email confirmation and verification
2. Deposit funds with bank details completion
3. Open, modify, and cancel buy/sell order
4. Check transaction history after order opening/closing


BE + FE Testing:
1.  Order Opening: Verify UI displays successful order placement, expect a 200 POST request with response data (order ID, time). Confirm the new entity exists in the database.
2.  Order Modification: UI allows modifications with successful notifications, expect a 200 PUT request. Verify response body and changes in the database.
3.  Get All Orders: UI correctly displays data, expect a 200 GET request. Confirm all entries in the database.
4.  Order Deletion: UI displays notifications, on confirmation, expect a 204 DELETE request. The deleted order should no longer be visible in the UI or database.


Mobile FE + BE Testing:
1. Real-Time Price Monitoring: I would verify that the mobile app updates prices in real-time, with visual indicators for price fluctuations, like green for an increase and red for a decrease. I would ensure no delay in receiving these updates and cross-check with backend data for accuracy. API requests can be tracked via WebSocket or GET requests for real-time data delivery.

2. Viewing Transaction History: This test would check whether the transaction history displays correctly, including purchase dates, amounts, and statuses. The backend should properly store transaction data and provide accurate records. Using API requests, I would verify that the history is fetched correctly and matches the user’s activities.

3. Stock Chart Rendering: I would ensure that stock charts are rendered smoothly and display accurate historical data for various timeframes (1D, 1W, 1M). On the backend, I would validate that the data provided is accurate and aligns with actual market conditions. API requests for chart data must be monitored to ensure they are timely and correct.
