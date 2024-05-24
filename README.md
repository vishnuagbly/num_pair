# NumPair
<img src="https://raw.githubusercontent.com/vishnuagbly/num_pair/master/logo.png" alt="Logo" height="300">

**NumPair** is an essential Dart package that revolutionizes how you handle numerical values in Flutter! Convert any pair of numbers into a versatile `NumPair` class and perform an array of powerful matrix and vector operations effortlessly. Designed to supercharge your Flutter projects, NumPair offers seamless conversions and a robust, intuitive API that simplifies your code and boosts your productivity.

## 🚀 Features

- **Unified Number Pair Class**: Transform any numerical values into a common `NumPair` class.
- **Matrix/Vector Operations**: Execute complex operations like dot products, addition, subtraction, multiplication, division, and scalar operations with ease.
- **Utility Methods**: Access utilities for rounding, flipping, absolute values, and more.
- **Element-Wise Operations**: Perform element-wise maximum and minimum operations.
- **Seamless Conversions**: Effortlessly convert to and from standard Flutter objects like `Alignment`, `Offset`, and `Size`.
- **Simple and Intuitive API**: Easily integrate into your Flutter projects and streamline your numerical handling.

## 🏁 Getting Started

To start using NumPair, add it as a dependency in your `pubspec.yaml` file:

```yaml
dependencies:
  num_pair: ^1.0.0
```

Then run `flutter pub get` to fetch the package.

## 🌟 Usage

Here's a quick example of how to use NumPair in your Flutter project:

```dart
import 'package:num_pair/num_pair.dart';

void main() {
  var pair1 = NumPair(3, 4);
  var pair2 = NumPair(5, 6);

  var additionResult = pair1 + pair2;
  var dotProduct = pair1 * pair2;
  var scalarMultiplication = pair1 * 10;
  var roundedPair = pair1.round();
  var absolutePair = pair1.abs();
  var flippedPair = pair1.flip();
  var elementWiseMax = NumPair.elementWiseMax(pair1, pair2);

  print('Addition: $additionResult'); // Output: NumPair(8, 10)
  print('Dot Product: $dotProduct'); // Output: NumPair(15, 24)
  print('Scalar Multiplication: $scalarMultiplication'); // Output: NumPair(30, 40)
  print('Rounded Pair: $roundedPair'); // Output: NumPair(3, 4)
  print('Absolute Pair: $absolutePair'); // Output: NumPair(3, 4)
  print('Flipped Pair: $flippedPair'); // Output: NumPair(4, 3)
  print('Element-Wise Max: $elementWiseMax'); // Output: NumPair(5, 6)
}
```

### 🌈 Extensions for Seamless Conversions

NumPair makes converting standard Flutter objects a breeze! Check out these powerful extensions:

```dart
import 'package:flutter/material.dart';
import 'package:num_pair/num_pair.dart';

void main() {
  var alignment = Alignment(0.5, 0.5);
  var offset = Offset(100, 200);
  var size = Size(50, 100);
  var tuple = (10, 20);

  var npFromAlignment = alignment.np;
  var npFromOffset = offset.np;
  var npFromSize = size.np;
  var npFromTuple = tuple.np;
  var npFromNum = 5.np;

  print('NumPair from Alignment: $npFromAlignment'); // Output: NumPair(0.5, 0.5)
  print('NumPair from Offset: $npFromOffset'); // Output: NumPair(100, 200)
  print('NumPair from Size: $npFromSize'); // Output: NumPair(50, 100)
  print('NumPair from Tuple: $npFromTuple'); // Output: NumPair(10, 20)
  print('NumPair from Num: $npFromNum'); // Output: NumPair(5, 5)
}
```

## 📚 Class Details

### NumPair Class

- **Constructors**:
    - `NumPair(num x, num y)`: Creates a `NumPair` with the specified values.
    - `NumPair.fromPair((int, int) values)`: Creates a `NumPair` from a tuple of integers.

- **Operators**:
    - `*`: Multiplies `NumPair` with another `NumPair` or a scalar value.
    - `+`: Adds two `NumPair` objects.
    - `-`: Subtracts one `NumPair` from another or negates a `NumPair`.
    - `/`: Divides `NumPair` by another `NumPair` or a scalar value.
    - `[]`: Accesses elements by index.

- **Methods**:
    - `flip()`: Returns a `NumPair` with its elements swapped.
    - `round()`: Returns a `NumPair` with its elements rounded.
    - `abs()`: Returns a `NumPair` with its elements as absolute values.
    - `sum()`: Returns the sum of the elements.
    - `elementWiseMax()`: Returns the element-wise maximum of two `NumPair` objects.
    - `elementWiseMin()`: Returns the element-wise minimum of two `NumPair` objects.

## 🔍 Additional Information
For more details, visit our [documentation](https://example.com/num_pair_docs). If you encounter any issues or have feature requests, please file them on our [issue tracker](https://github.com/your_username/num_pair/issues). We welcome contributions! Check out our [contributing guide](https://github.com/your_username/num_pair/blob/main/CONTRIBUTING.md) to get started.

Follow us on [Twitter](https://twitter.com/your_handle) and [LinkedIn](https://linkedin.com/in/your_profile) for the latest updates and news.

Happy coding with NumPair! 🎉