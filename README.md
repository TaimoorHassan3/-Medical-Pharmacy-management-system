# -Medical-Pharmacy-management-systemPharmacy Management System
Overview
The Pharmacy Management System is a desktop application designed to manage the various operations of a pharmacy, including placing orders for medicines, viewing order history, managing medicine stock, and processing payments. This application provides a user-friendly interface to facilitate these operations efficiently.
Technologies Used
•	Java: Core language for application development.
•	Swing: Java's GUI toolkit used for building the user interface.
•	Java AWT: Used for graphical user interface components.
Features
1.	Place Order: Allows users to place an order for medicines.
2.	Order Summary: Displays a summary of the order before confirmation.
3.	Payment Processing: Enables users to enter payment details and process payments.
4.	Apply Discount: Users can apply discount codes to reduce the total cost of their orders.
5.	View Order History: Displays a list of past orders for reference.
6.	Shipping Method Selection: Users can select the shipping method and see the estimated delivery time.
Installation
1.	Clone the Repository:
bash
Copy code
git clone https://github.com/yourusername/pharmacy-management-system.git
cd pharmacy-management-system
2.	Compile the Code:
bash
Copy code
javac -d bin src/**/*.java
3.	Run the Application:
bash
Copy code
java -cp bin main.PlaceOrderGui
Instructions
1.	Launching the Application:
o	Run the PlaceOrderGui class to start the application.
2.	Placing an Order:
o	Enter the medicine name and select the quantity.
o	Optionally, choose a category to filter the search results.
o	Click Search to find the medicine.
o	Click Place Order to proceed to the order summary.
3.	Applying a Discount:
o	Enter a valid discount code in the discount code field.
o	Click Apply Discount to apply the discount to the total cost.
4.	Viewing Order Summary:
o	Review the order details in the summary dialog.
o	Click Confirm to finalize the order.
5.	Processing Payment:
o	Click Payment to open the payment dialog.
o	Enter card details and click Pay to process the payment.
6.	Viewing Order History:
o	Click View Order History to open the order history dialog.
o	Review past orders in the displayed table.
Code Changes and Additions
File: PlaceOrderGui.java
New Functionalities Added
1.	Apply Discount Code:
o	Elements Added:
java
Copy code
private JTextField discountCodeField;
private JButton applyDiscount;
private Map<String, Double> discountCodes;
o	Functionality:
	Added a text field for entering discount codes and a button to apply the discount.
	Implemented logic to validate and apply discount codes to reduce the total cost.
2.	Display Total Cost:
o	Element Added:
java
Copy code
private JLabel totalCostLabel;
o	Functionality:
	Added a label to display the total cost of the order, which updates when a discount is applied.
3.	Order Summary Display:
o	Method Added:
java
Copy code
private void displayOrderSummary() { ... }
o	Functionality:
	Added a dialog to display an order summary before confirming the order, including medicine name, quantity, total cost, shipping method, and estimated delivery time.
4.	Payment Processing:
o	Method Added:
java
Copy code
private void processPayment() { ... }
o	Functionality:
	Added a dialog to enter card details and process the payment. Includes fields for card number, expiry date, and CVV.
5.	Shipping Method and Estimated Delivery:
o	Elements Added:
java
Copy code
private JComboBox<String> shippingMethodComboBox;
private JLabel estimatedDeliveryLabel;
o	Functionality:
	Added a dropdown to select the shipping method (Standard or Express).
	Added a label to display the estimated delivery time based on the selected shipping method.
6.	View Order History:
o	Elements Added:
java
Copy code
private JButton viewOrderHistory;
private List<Order> orderHistory;
o	Functionality:
	Added a button to view past orders.
	Added a dialog to display the order history in a table format with columns for order ID, date, and total price.
Summary of Code Changes
•	Added UI elements for discount code application, total cost display, payment processing, and order summary display.
•	Implemented methods for processing payments, applying discount codes, updating estimated delivery time, and displaying order summaries.
•	Added logic for viewing order history and managing shipping methods.
Conclusion
The Pharmacy Management System provides an intuitive interface for managing pharmacy operations, from placing orders to processing payments. The added functionalities enhance user experience by offering discounts, detailed order summaries, and various shipping options. The system is built with Java and Swing, ensuring a robust and scalable application.

