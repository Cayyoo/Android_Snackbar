# Android_Snackbar
Snackbar使用

```java
/**
 * Android Snackbar花式使用指南：
 *
 *
 * 基本介绍：
 * 1、使用Snackbar要导入com.android.support:design库。如，compile 'com.android.support:design:25.3.1'
 * 2、Snackbar显示在所有屏幕其它元素之上(屏幕最顶层)，同一时间只能显示一个snackbar。
 * 3、Snackbar的基本使用很简单，与Toast类似。
 *   Snackbar.make(view, message_text, duration)
 *           .setAction(action_text, click_listener)
 *           .show();
 *
 *      make()方法是生成Snackbar的。
 *      Snackbar需要一个控件容器view用来容纳，官方推荐使用CoordinatorLayout来确保Snackbar和其他组件的交互，有俩个好处：
 *            1.用户可以滑动（右滑）消除掉snackbar。
 *            2.当snackbar出现的时候，布局会移动一些UI元素，比如右下角有悬浮按钮会自动上移、比如滑动取消Snackbar、Snackbar出现时FloatingActionButton上移。
 *      显示时间duration有三种类型：
 *         LENGTH_SHORT //短时间显示，然后自动取消
 *         LENGTH_LONG //长时间显示，然后自动取消
 *         LENGTH_INDEFINITE //不消失显示，除非手动取消
 * 4、snackbar显示是一个接一个的，不能同时显示很多。
 */

/**
 * SnackBars提供了一个轻量级的反馈操作。
 * 他们在屏幕的底部显示一条简短的信息，如果是较大的设备就显示在左下角。
 * SnackBar出现在屏幕中所有其他元素的上方，同一时间仅仅只有一条SnackBar。
 * 即：
 * 1、SnackBar和Toast的用途一样，都是用来提示用户操作后的结果的。
 * 2、SnackBar显示时位置一般是在屏幕底部，较大的设备就显示在左下角。
 * 3、SnackBar同一时间只有一条
 *
 * 在超时或者用户在屏幕上完成了交互的时候SnackBar会自动消失，特别是在召唤了新的表层（意思是SnackBar本来是最外层的，然后在SnackBar上又新添加了一层）或者Activity的时候。
 * SnackBar能在屏幕上侧滑。即
 * 1、SnackBar可以自动消失，也可以手动取消（在完成某个操作的时候）
 * 2、在Activity结束的时候，SnackBar会消失，这点Toast不会
 * 3、SncakBar能支持侧滑，侧滑干嘛呢？当然是删除，之后会做介绍
 *
 * SnackBar能包含一个action使用setAction方法。
 *
 * 你可以用CallBack来得知Snackbar是显示还是隐藏。
 */
```

![](https://github.com/ykmeory/Android_Snackbar/blob/master/img/base.gif "基础")<br/>
![](https://github.com/ykmeory/Android_Snackbar/blob/master/img/msg.gif "消息")<br/>
![](https://github.com/ykmeory/Android_Snackbar/blob/master/img/addIcon.gif "添加图标")<br/>
![](https://github.com/ykmeory/Android_Snackbar/blob/master/img/addMultiLayout.gif "添加多布局")<br/>
![](https://github.com/ykmeory/Android_Snackbar/blob/master/img/warningAndErrorMsg.gif "警告和错误消息")
