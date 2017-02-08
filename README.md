# AutoSuggest Text Input
AutoSuggest Text input using Array of object as list of searchable content. And return selected of object with term object must have this key {text, value}.

## Installation
* `npm install {link of this git download} --save`

___

## Example:
```js
import AutoSuggest from 'react-native-autosuggest';

const suggestions = [
      {text: 'Banana', value: '1'},
      {text: 'Apple', value: '2'}
    ]

<AutoSuggest
      rowTextStyles={{backgroundColor: 'darkblue', color: 'white'}}
      terms={suggestions}
      placeholder="select a fruit."
      textInputStyles={{backgroundColor: 'black', color: 'white'}}
      onChangeText={(el) => console.log('changing text!', el.text)}
      onItemPress={(el) => console.log('changing text!', el.text)}
      clearBtnVisibility={false}
      maxRow = {10}
    />
```

## Props:
Refer to React's [TextInput](https://facebook.github.io/react-native/docs/textinput.html) documentation for more information on `placeholder` and `onChangeText`.
Refer to the source code for more information about the rest.

* `onChangeText` (__function__, fired when the input changes.)
* `onChangeTextDebounce` (__integer__, the minimum break *in milliseconds* that the onChangeText callback needs to take before firing again. **default is 0.**)
* `onItemPress` (__function__ fired when an item in the menu is pressed with that item's string value as the argument. You probably don't need this, and should just use onChangeText)
* `clearBtn` (__Array__ e.g. [[<MyCustomClearButtonComponent />]  -- only if you want a custom btn component, **default is undefined**.)
* `terms` (__Array__  e.g. ['Chicago', 'New York', 'San Francisco'])
* `placeholder` (__String__ e.g. "Please enter a City.")
* `maxRow` (__Number__ e.g. 10, Default number is 5)

### Styles:
* `clearBtnStyles` (__Object__ e.g. {backgroundColor: "white", flex: 2})
* `textInputStyles` (__Object__ e.g. {width: 400, backgroundColor: "black"})
* `containerStyles` (__Object__ e.g. {flex: 2})
* `rowWrapperStyles`

## Todo:
* ~~pass a custom component for the "clear" button~~
