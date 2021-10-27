# flutterMark

Flutter通过你的widgets创建Wdiget树
Flutter will go through your widgets and create the Widget tree.

通过Widget树创建Element树，Elemgnt是通过Widget的createElement创建的。
Corresponding to the Widget tree, Flutter creates the Element tree in which each Element object is created by calling createElement() on the widget.

而render object是在Element调用createRenderObject()的时候创建的
Each render object will be created when Element calls createRenderObject().
