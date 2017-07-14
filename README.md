# React Native Content Loader  

Fork of https://github.com/virusvn/react-native-svg-animated-linear-gradient with minor modifications in order to use it outside of EXPO

## Demo
<table>
<tr><td>
<img src="https://raw.githubusercontent.com/virusvn/react-native-svg-animated-linear-gradient/master/images/demo-svg-animated-linear-gradient.gif" width="300"></td><td>
<img src="https://raw.githubusercontent.com/virusvn/react-native-svg-animated-linear-gradient/master/images/demo-svg-animated-linear-gradient-angle.gif" width="300">
</td>
</tr>
</table>

## Install

###### Install react-native-svg and d3-interpolate ######
```js
npm install react-native-svg d3-interpolate --save
```
###### Link react-native-svg ######
```js
react-native link react-native-svg
```
###### Install Content Loader ######
```js
npm install react-native-content-loader
```

**IMPORTANT: Remove “libRNSVG-tvOS.a” in xcode.**

*(How? Open .xcodeproj inside ios folder. Click on your project (root in the folder navigator on your left).
Build Phases tab -> Link Binary with Libraries -> remove “libRNSVG-tvOS.a”)*


###### Restart app running react-native run-ios ###### 

## Usage

```js
import ContentLoader from 'react-native-content-loader'
import {Circle, Rect} from 'react-native-svg'
```
### Examples

#### Instagram style
```jsx
<ContentLoader height={300} duration={1000}>
    <Circle cx="30" cy="30" r="30"/>
    <Rect x="75" y="13" rx="4" ry="4" width="100" height="13"/>
    <Rect x="75" y="37" rx="4" ry="4" width="50" height="8"/>
    <Rect x="0" y="70" rx="5" ry="5" width="400" height="200"/>
</ContentLoader>
```

#### Facebook style

```jsx
<ContentLoader primaryColor="#e8f7ff"
               secondaryColor="#4dadf7"
               duration={700}
               height={140}>
    <Rect x="0" y="0" rx="5" ry="5" width="70" height="70"/>
    <Rect x="80" y="17" rx="4" ry="4" width="300" height="13"/>
    <Rect x="80" y="40" rx="3" ry="3" width="250" height="10"/>
    <Rect x="0" y="80" rx="3" ry="3" width="350" height="10"/>
    <Rect x="0" y="100" rx="3" ry="3" width="200" height="10"/>
    <Rect x="0" y="120" rx="3" ry="3" width="360" height="10"/>
</ContentLoader>
```
#### Code style

```jsx
<ContentLoader
            primaryColor="#fff0f6"
            secondaryColor="#f783ac"
            height={80}>
    <Rect x="0" y="0" rx="3" ry="3" width="70" height="10"/>
    <Rect x="80" y="0" rx="3" ry="3" width="100" height="10"/>
    <Rect x="190" y="0" rx="3" ry="3" width="10" height="10"/>
    <Rect x="15" y="20" rx="3" ry="3" width="130" height="10"/>
    <Rect x="155" y="20" rx="3" ry="3" width="130" height="10"/>
    <Rect x="15" y="40" rx="3" ry="3" width="90" height="10"/>
    <Rect x="115" y="40" rx="3" ry="3" width="60" height="10"/>
    <Rect x="185" y="40" rx="3" ry="3" width="60" height="10"/>
    <Rect x="0" y="60" rx="3" ry="3" width="30" height="10"/>
</ContentLoader>
```
### Props

|Prop   |Type   |Default   |Description
|---|---|---|---|
|primaryColor   |String   |'#eeeeee'   |Primary color, also background color   |
|secondaryColor   |String   |'#dddddd'   |Secondary color   |
|duration   |Number   |2000   |Animation duration   |
|width   |Number   |300   |Width of SVG   |
|height   |Number   |200   |Height of SVG   |
|x1   |String   |'0'   |x of point star gradient, accept Number or Percentage   |
|y1   |String   |'0'   |y of point star gradient, accept Number or Percentage   |
|x2   |String   |'100%'   |x of point end gradient, accept Number or Percentage   |
|y2   |String   |'0'   |y of point end gradient, accept Number or Percentage   |

## TODO
- Test on Android

## License

MIT
