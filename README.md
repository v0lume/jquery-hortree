# jquery-hortree
This jQuery plugin will render an horizontal hierarchical tree starting from a JSON schema

## Demo

[See a demo here](https://alesmit.github.io/demo/jquery-hortree/)

## Usage

1. Include jQuery
2. Include [jquery.line.js](https://github.com/tbem/jquery.line) plugin (credits to [tbem](https://github.com/tbem))
3. Include __jquery.hortree.js__ and __jquery.hortree.css__

```
$('#your-div').hortree({
    data: [
        {
            description: 'root',
            children: []
        }
    ]
});
```

## Options

You can provide a configuration object as first parameter to manage content and graphic stuff.

|      property     | required | data type | default  |        notes        |
|:-----------------:|:--------:|:---------:|:--------:|---------------------|
| `data`            | __Yes__  |  Array    | []       | Each object in this array should have the properties `description` and `children`, where `children` is an array containing objects with the same structure. This is the basic schema, you can modify the source code adding properties and managing it in your template according to your data structure. |
| `lineStrokeWidth` |   No     |   int     | 2        |                     |
| `lineZindex`      |   No     |   int     | 8        |                     |
| `lineColor`       |   No     |  string   | #4b86b7  |                     |
| `onComplete`      |   No     | function  | -        | This function is called when the tree is rendered |

`description` content is rendered in a `<div>` element with the class `.hortree-label`. Modify it as your need to get the best look and feel.

