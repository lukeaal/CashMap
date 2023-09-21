# CashMap
Geographical based iOS app to increase your spending awareness

## Contact Information
- Zach Watson: watsonz@iu.edu
- Luke Atkins: lukeatki@iu.edu

## App Functionality
Upon launching the app, users will be prompted to grant location access. Once permission is granted, the app opens to a map view centered on the user's current location. Here's what you can do within the app:

### Map View
- **View Callout Bubble:** Tap on a pin on the map to view a callout bubble with additional information (more relevant for transaction pins).
- **Add Transaction:** Click the 'plus' button in the bottom right to access the 'Add Transaction' form.
- **View Transactions:** Navigate to the transactions list by tapping the 'transactions' back button in the top right.
![Alt Text](Image URL)

### Add Transaction
- Clicking the 'Add Transaction' button opens a form where users can:
  - Enter the transaction amount.
  - Select a category that best describes the transaction.
  - Provide a brief name to identify the transaction.
- After adding the transaction, the form clears, and users can return to the map view by swiping down to dismiss the form.

### Transaction Table
- When users tap the 'transactions' back button on the map, they are directed to a segmented table displaying all their transactions.
- The table is segmented by category, with each row showing the transaction name and amount.
- Interaction options on the table include:
  - Tapping the arrow indicator in the top right to return to the map view.
  - Using the clear button in the top left to remove all previous transactions.
  - Tapping on a table row to return to the map view, focused on the respective transaction.
  - Swiping left on a table row to reveal a delete button, allowing users to remove a specific transaction.

### Widget
- Users can add a transactions widget to their home screen, displaying the total spent in each category.
- Tapping the widget takes users back to the app.

**Note:** The app does not pull live data. Data sharing between widgets and the main app requires an Apple developer license due to bundle identifier conflicts and entitlement issues.

## Xcode Environment
- Xcode Version: 14.2 (14C18)
- Compatible with iOS versions 14 and above
- Best experienced on iPhone 14 Plus (Please note: Category scroll bar may not appear on the form view for iPhone 14 Pro or Max due to constraint issues)

## Features, Functionalities, Implementations

### MapKit
- Implemented by the MapViewController
- Location services are used in MapViewController and EntryViewController

### Widgets
- Implemented by the new CashMapWidget target and build source

### Notifications
- Implemented by the NotificationsHelper, used in the MapViewController and AppDelegate

### CoreData
- Implemented by the Transactions and TransactionsModel files

## Navigation Controller
- Implemented through a split view controller containing the MapViewController and TableViewController

## Data Entry
- Implemented through EntryViewController

