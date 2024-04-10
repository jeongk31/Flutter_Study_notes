# Flutter Development Notes

## Basic Syntax and Concepts

### Functions
- `add(a, b)`: positional parameter
- `add({a, b})`: named parameter, call using `add(b:5, a:10)`
- `add(a, [b = 5])`: optional positional parameter where `b` defaults to 5
- Named parameters are optional and can be made mandatory using the `required` keyword.

### Variables
- `var`
- `[type]? name;`:   unassigned variable
- `final`:           unchanged variable
- `const`:           constant variable

### Constants
- `const` is used for runtime performance optimization.

### Arrow Function
- `() => 'x'`: shorthand for `() { return 'x'; }`.

### Anonymous Functions
- `() { code }`: defines a function in place.

## Classes and Widgets

### General Structure
- Class can be defined in a separate file, e.g., `gradient_container.dart` and includes:
  - Fields (variables)
  - Methods (functions)
  - Constructor

### Widget Types
- `widget -> class`
- Stateless widget: no internal state (does not change).
- Stateful widget: contains state (changes are possible), and triggers `build` method on state changes.

### Lifecycle Methods
- `initState()`: Called when a stateful widget is initialized.
- `build()`: Called to build the widget. Rebuilt on calling `setState()`.
- `dispose()`: Called when the widget is about to be removed from the tree permanently.

## Layout Widgets

### Column & Row
- Used to place multiple child widgets.
- Takes use of all available space.
  - `mainAxisSize`: for the main axis (selected column/row).
  - `crossAxisAlignment`: for the perpendicular axis.
  - `mainAxisSize: MainAxisSize.min`: Centers the column.

### ListView and Cards
- `ListView()`: Scrollable list. Use `ListView.builder()` for enhanced performance as it only loads visible items.
- `Card()`: Puts content into a card with aesthetic shadow.
- `Spacer()`: An empty widget that takes up maximum space available.

## Asset Management

### Adding Assets
- Create a folder for assets.
- Include assets in `pubspec.yaml`.

## Code Styling and Tools in VS Code

### Refactoring and Formatting
- Refactor: Easy to add widgets.
- Format: Use `,` after each parenthesis to format documents (`>format`).

### Debugging Tools
- Use 'Debug Console' and click the link to navigate directly to error lines.
- Run -> Start Debugging: Runs app in debug mode, allows breakpoints, and step over commands.
- `>flutter devtools`: Opens various analysis tools in a webpage.
- Profile mode for performance analysis.

## Advanced Concepts

### Enumerations and Spread Operator
- `enum`: A set of predefined values.
- `...`: Spread operator, to add multiple widgets in a list or to flatten lists.

### State Management
- `State<DiceRoller> createState()`: Replaces `build` for stateful widgets, initializes state.
- `setState()`: Re-executes the `build` method within the State class.
- Access stateful widget properties with `widget.propertyName`.

### Layout Enhancements
- `mainAxisAlignment: MainAxisAlignment.center`: Use all vertical space.
- `crossAxisAlignment: CrossAxisAlignment.stretch`: Use all horizontal space.
- `Expanded`: Takes all available space, avoids overflow.
- `SingleChildScrollView`: Makes a single child scrollable.

## Fonts and Packages

### Using Fonts and External Packages
- Install package.
- Import package.
- Use as per the package documentation. Refer to package docs for more details.

## Variable Visibility
- `varName`: Public by default.
- `_varName`: Private, commonly used for class names.

## Device Management in Flutter
- Change running device using `>Flutter: Select Device`.

## Settings for VS Code
- Use settings to enhance coding efficiency:
  - Refactor widgets easily.
  - Automatically format documents.
