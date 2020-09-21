# three-rubiks-cube
> ## a extension THREE.CSS3DObject for making rubik's cube(only 333)

![grab-landing-page](https://github.com/lab89/three-rubiks-cube/blob/master/images/main.gif?raw=true)

> ## execute example
```
clone repository
cd example
npm i
npm run start
done!
```


> ## properties
```
import RubiksCube from 'three-rubiks-cube'
const cube = new RubiksCube({...})
console.log(cube.options)
===================================================================
{
    blockColor : "black", // cube block color
    size : 200, // cube size
    stickerColorSet : {
        "f": "rgba(42, 249, 107, 1)", // front face sticker color
        "b": "rgba(5, 34, 174, 1)", // back face sticker color
        "l": "rgba(225, 10, 28, 1)", // left face sticker color
        "r": "rgba(252, 77, 30, 1)", // right face sticker color
        "u": "rgba(230, 245, 252, 1)", // up face sticker color
        "d": "rgba(235, 253, 57, 1)", // down face sticker color
    },
    fitment : "fitted", // sticker size (fully_fitted, fitted)
    mirror : true,  // mirror sticker
    hoverEnabled : true, // cube block mouseover event enable
    clickEnabled : true, // cube click event enable
    hoverColor : "red", // mouseover block color
    clickColor : "cyan", // click block color
    animateDuration : 1000 // animation time
}
====================================================================
```

> ## methods
```
import RubiksCube from 'three-rubiks-cube'
const cube = new RubiksCube({...})
    
cube.cuberefreshCube() : refresh cube (block + sticker)
cube.refreshStickers() : refresh sticker
cube.refreshBlockColor() : refresh block
cube.toggleMirror() : on/off mirror sticker
cube.children : blocks array
cube.animate("RURU") : animation "RURU" operation every 1000ms(cube.options.animationDuration)
cubme.immediateOperate("RURU") : apply operation RURU without animation
```
   
> ## usage
```
import RubiksCube from 'three-rubiks-cube'
cube = new RubiksCube(
    {
        blockColor : "black", // cube block color
        size : 200, // cube size
        stickerColorSet : {
            "f": "rgba(42, 249, 107, 1)", // front face sticker color
            "b": "rgba(5, 34, 174, 1)", // back face sticker color
            "l": "rgba(225, 10, 28, 1)", // left face sticker color
            "r": "rgba(252, 77, 30, 1)", // right face sticker color
            "u": "rgba(230, 245, 252, 1)", // up face sticker color
            "d": "rgba(235, 253, 57, 1)", // down face sticker color
        },
        fitment : "fitted", // sticker size (fully_fitted, fitted)
        mirror : true,  // mirror sticker
        hoverEnabled : true, // cube block mouseover event enable
        clickEnabled : true, // cube click event enable
        hoverColor : "red", // mouseover block color
        clickColor : "cyan", // click block color
        animateDuration : 1000 // animation time
    });

    //change block color
    cube.option.blockColor = "~~"
    cube.refreshBlockColor();

    //refresh sticker
    cube.option.stickerColorSet["f] = "~~"
    cube.refreshSticker();

    //refresh cube
    cube.cuberefreshCube()
```