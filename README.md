# Styled_widget
<a href="https://pub.dev/packages/styled_widget"><img src="https://img.shields.io/pub/v/styled_widget"></a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="https://www.buymeacoffee.com/tOTWBs7"><img src="https://camo.githubusercontent.com/be06971baed9105260e0ed5c03746108c30b527f/68747470733a2f2f63646e2e6275796d6561636f666665652e636f6d2f627574746f6e732f64656661756c742d6f72616e67652e706e67" alt="Buy Me A Coffee" data-canonical-src="https://cdn.buymeacoffee.com/buttons/default-orange.png" width="150px" /></a><br /><br />
<img src="https://github.com/ReinBentdal/styled_widget/blob/master/example/assets/styled_widget.jpg?raw=true" />


>Simplifying your widget tree structure by defining widget using methods.

If you like the package, consider giving the package a :star: on [GitHub](https://github.com/ReinBentdal/styled_widget) or a :thumbsup: on [pub](https://pub.dev/packages/styled_widget)!

### To read about how this package works and how to use it, visit the [wiki](https://github.com/ReinBentdal/styled_widget/wiki)

## Examples
#### Showcase app
| [App designer](https://dribbble.com/shots/6459693-Creative-layout-design),  [Code](https://github.com/ReinBentdal/styled_widget/blob/master/example/homepage_example.dart) |
|-|
|<img src="https://raw.githubusercontent.com/ReinBentdal/styled_widget/master/example/assets/demo_app.gif" width="250">|

#### Text
```dart
Text('some text')
  .bold()
  .fontSize(24)
  .padding(all: 10)
  .backgroundColor(Colors.amber)
  .alignment(Alignment.center);
```
"Native" flutter eqivalent
```dart
Align(
  alignment: Alignment.center,
  child: DecoratedBox(
    decoration: BoxDecoration(
      color: Colors.amber,
    ),
    child: Padding(
      padding: EdgeInsets.all(10),
      child: Text(
        'some text', 
        style: TextStyle(
          fontSize: 24,
          fontWeight: FontWeight.bold,
        ),
      ),
    ),
  ),
);
```

#### Animations
```dart
YourWidget
  ...
  .backgroundColor(onTapState ? Colors.black : Colors.amber, animate: true)
  ...
  .animate(duration: Duration(milliseconds: 1000), curve: Curves.easeOut)
  .gestures(onTapChange: (state) => setState(() => onTapState = state));
```
