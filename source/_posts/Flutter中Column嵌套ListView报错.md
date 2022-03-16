---
title: Flutter中Column嵌套ListView报错
date: 2022-03-16 16:33:03
categories:
- [技术, Flutter]
tags: 
- Flutter
---

```dart
Column(
  children: <Widget>[
    ListView.builder(
      itemCount: 10,
      itemBuilder: (context, index){
      return Text('$index');
    })
  ],
),
```

报错。

解决办法：使用Expand包裹ListView即可

```dart
Column(
  children: <Widget>[
    Expanded(child: ListView.builder(
        itemCount: 10,
        itemBuilder: (context, index){
          return Text('$index');
        }))
  ],
),
```

