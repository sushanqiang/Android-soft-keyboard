# Android-soft-keyboard

在开发中使用安卓软件盘时，会遇到很多问题，比如：当点击编辑edittext时，软键盘出来，要么会把布局往上顶，或者覆盖等等，


在这里，我们要先了解软键盘输入的一些特点

【A】stateUnspecified：软键盘的状态并没有指定，系统将选择一个合适的状态或依赖于主题的设置
【B】stateUnchanged：当这个activity出现时，软键盘将一直保持在上一个activity里的状态，无论是隐藏还是显示
【C】stateHidden：用户选择activity时，软键盘总是被隐藏
【D】stateAlwaysHidden：当该Activity主窗口获取焦点时，软键盘也总是被隐藏的
【E】stateVisible：软键盘通常是可见的
【F】stateAlwaysVisible：用户选择activity时，软键盘总是显示的状态
【G】adjustUnspecified：默认设置，通常由系统自行决定是隐藏还是显示
【H】adjustResize：该Activity总是调整屏幕的大小以便留出软键盘的空间
【I】adjustPan：当前窗口的内容将自动移动以便当前焦点从不被键盘覆盖和用户能总是看到输入内容的部分



我在开发中使用时跟布局使用RelativeLayout，然后布局里面的editext放在layout_alignParentBottom，这时，打开的话就是把这个编辑器覆盖了，所以应该在manifest中使用 android:windowSoftInputMode="adjustResize|adjustPan"
