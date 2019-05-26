# JqContextMenu
Custom context menu builder Jquery plugin

## Creating an Menu

```javascript
$('#content').jqContextMenu({
    contextMenu: [{
            icon: 'lnr lnr-pencil',
            text: 'Edit',
            dataKey: 'edit'
        },
        {
            icon: 'lnr lnr-file-empty',
            text: 'Copy',
            dataKey: 'copy'
        },
        {
            icon: 'lnr lnr-bookmark',
            text: 'Add to Bookmarks',
            dataKey: 'bookmark'
        },
        {
            icon: 'lnr lnr-pie-chart',
            text: 'Stats',
            dataKey: 'stats',
        },
        {
            icon: 'lnr lnr-trash',
            text: 'Delete',
            dataKey: 'bookmark'
        }
    ]
});
```

## Handling clicks

```javascript
$(document).on('mousedown', '#content #jqcontext-menu li', function () {
    var dataKey = $(this).attr('data-key');

    if (dataKey == 'edit'){
        alert('you clicked "edit" button');
    } else {
        alert('you clicked ' + dataKey+ ' button');
    }
});
```