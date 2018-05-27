# react-native-fontawesome-free
Easily use your FontAwesome Free icons in React-Native

# Requirements

* Install `react-native-svg`

```
npm install --save react-native-svg

or

yarn add react-native-svg
```

* Link `react-native-svg`

```
react-native link react-native-svg
```

# Installation

`npm install react-native-fontawesome-free --save`

or

`yarn add react-native-fontawesome-free`

The postinstall script will then automatically install the pro packages for you.

# Usage

In your main app.js file
```
import { configureFontAwesomeFree } from "react-native-fontawesome-free";

/* NOTE: Optional you can pass a prefixType into configureFontAwesomePro to change the default from "regular" to "solid" or "light" */

configureFontAwesomeFree();
// configureFontAwesomeFree("solid");
```

In your components
```
import Icon from "react-native-fontawesome-free";

<View style={styles.container}>
  <Icon name="chevron-right" color="red" type="regular" onPress={() => alert("do something")} />
  <Icon name="chevron-right" color="blue" type="solid" size={24}/>
  <Icon name="chevron-right" color="green" type="light" size={24} />
</View>
```

# Props
```
  prefixType = {
    regular: "far",
    solid: "fas",
    light: "fal",
    brands: "fab"
  };
```
The icon `name` prop can be found in fontawesome.com/icons
If a valid name is not provided `question-circle` will show up instead.

| Props         | type          | default  |
| ------------- |:-------------:| --------:|
| name          | string        | ""                      |
| color      | hexdecimal or string | "black"             |
| size      | number      |   20                        |
| type | prefixType as a string see definition above      |    "regular" |
| iconStyle | style object      |    {} |
| containerStyle | style object      |    {} |
| onPress | function      |    null |



