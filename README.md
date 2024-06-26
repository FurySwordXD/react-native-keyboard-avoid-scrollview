# React Native - Keyboard Avoid Scrollview
React Native Keyboard Avoid Scrollview is a simple and easy to use cross platform component that augments react-native's SafeAreaView and ScrollView to create a single component that works out of the box to handle all the jank involved in keyboard avoidance in React Native.

## Getting Started
- Install the library to your project
```
yarn add react-native-keyboard-avoid-scrollview
```
```
npm install react-native-keyboard-avoid-scrollview
```
- Start using KeyboardAvoidScrollView

You have access to all ScrollView props and can be passed to the KeyboardAvoidScrollView.
In addition, you have an additional spacing prop to which you can pass in a number that adds offset to your scrolling when a keyboard shows up.

Note: All values passed to the style prop is applied to the SafeAreaView that wraps the ScrollView

```
import KeyboardAvoidScrollView from 'react-native-keyboard-avoid-scrollview';

function App()
{
    return (
        <KeyboardAvoidScrollView>
            <View style={{ flex: 1 }}/>
            <TextInput />
        </KeyboardAvoidScrollView>
    )
}
```

### Examples
![Alt text](./example1.gif?raw=true "Example1")
```
    <View style={{ flex: 1, padding: 20  }}>
        <KeyboardAvoidScrollView style={{ flex: 1 }}>
            <View style={{ height: 500, justifyContent: 'center', alignItems: 'center', borderRadius: 20, backgroundColor: Colors.light }}>
                <Text style={{ fontSize: 20 }}>This is some large content...</Text>
            </View>
            <View style={{ gap: 20, paddingVertical: 20 }}>
                <Input label='First Name' placeholder='Enter first name...'/>
                <Input label='Last Name' placeholder='Enter last name...'/>
                <Button title='Submit' />
            </View>
        </KeyboardAvoidScrollView>
    </View>
```

Now let's add some spacing so that the KeyboardAvoidScollView scrolls to the input with some additional offset.
![Alt text](./example2.gif?raw=true "Example2")
```
    <View style={{ flex: 1, padding: 20  }}>
        <KeyboardAvoidScrollView style={{ flex: 1 }} spacing={100}>
            <View style={{ height: 500, justifyContent: 'center', alignItems: 'center', borderRadius: 20, backgroundColor: Colors.light }}>
                <Text style={{ fontSize: 20 }}>This is some large content...</Text>
            </View>
            <View style={{ gap: 20, paddingVertical: 20 }}>
                <Input label='First Name' placeholder='Enter first name...'/>
                <Input label='Last Name' placeholder='Enter last name...'/>
                <Button title='Submit' />
            </View>
        </KeyboardAvoidScrollView>
    </View>
```

### Authors
Sainath Ganesh - @furyswordxd

### License
This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.