# 前言
> 最近在群里发现有人问类似于高斯模糊的效果怎么实现，正好前段时间作者开源的RN项目[OneM](https://github.com/guangqiang-liu/OneM)中使用到了这一技术，所以在这作者单独的一个实现高斯模糊效果的Demo示例给到大家，供大家学习参考。[想查看作者的完整RN项目OneM请点击](https://github.com/guangqiang-liu/OneM)

# 预览效果图
![gif](http://upload-images.jianshu.io/upload_images/6342050-69ebfd8f81598cb2.jpg?imageMogr2/auto-orient/strip)

# 如何使用
* `npm install react-native-blur --save`
* `react-native link react-native-blur`
* `import {BlurView, VibrancyView} from 'react-native-blur'`

```
<BlurView
  style={styles.absolute}
  viewRef={this.state.viewRef}
  blurType="light"
  blurAmount={10}
/>
```

# 更多用法请查看官方文档
[https://github.com/react-native-community/react-native-blur](https://github.com/react-native-community/react-native-blur)

# 核心代码

```
render() {
    return (
      <View style={styles.container}>
        <Image
          ref={(img) => { this.backgroundImage = img}}
          source={{uri}}
          style={styles.absolute}
          onLoadEnd={this.imageLoaded.bind(this)}
        />
        <BlurView
          style={styles.absolute}
          viewRef={this.state.viewRef}
          blurType="light"
          blurAmount={10}
        />
        <Text>Hi, I am some unblurred text</Text>
      </View>
    )
  }
 
```

# 作者简书地址
**[http://www.jianshu.com/u/023338566ca5](http://www.jianshu.com/u/023338566ca5)**
 
# 总结
*react-native-blur* 组件的使用还是很简单的，同学们可以直接下载Demo示例查看使用方法即可，或者直接在官方文档中查看详细的使用教程。同学觉得文章对你有帮助，请 给个 **`star`** 给个 **`关注`** 谢谢。