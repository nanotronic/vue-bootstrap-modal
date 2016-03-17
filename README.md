# vue-bootstrap-modal

Bootstrap style modal component for vue.

doc writing...

<img src="https://github.com/Coffcer/vue-bootstrap-modal/blob/master/modal.gif">

# Usage

import Bootstrap.css
```
<link href="bootstrap.css"></link>
```

simple options:
``` html
<!--text content-->
<modal title="Modal Title" @ok="ok" @cancel="cancel" :show.sync="show">
    Modal Text
</modal>

<!--custom content-->
<modal title="Modal Title" @ok="ok" @cancel="cancel" :show.sync="show">
    <p>Modal Body1</p>
    <div>Modal Body2</div>
    
    <p slot="header">Modal Header</p>
    <p slot="title">Modal Title</p>
    <p slot="footer">Modal Footer</p>
</modal>

```

#Props
``` javascript
props: {
    show: {
        type: Boolean,
        twoWay: true,
        default: false
    },
    title: {
        type: String,
        default: 'Modal'
    },
    // Bootstrap small style modal
    small: {
        type: Boolean,
        default: false
    },
    // Bootstrap large style modal
    large: {
        type: Boolean,
        default: false
    },
    // Bootstrap full style modal    
    full: {
        type: Boolean,
        default: false
    },
    // if it set false, click background will close modal 
    force: {
        type: Boolean,
        default: false
    },
    // vue transition name
    transition: {
        type: String,
        default: 'modal'
    },
    // [OK button] text
    okText: {
        type: String,
        default: 'OK'
    },
    // [Cancel button] text
    cancelText: {
        type: String,
        default: 'Cancel'
    },
    // [OK button] className
    okClass: {
        type: String,
        default: 'btn blue'
    },
    // [Cancel button] className
    cancelClass: {
        type: String,
        default: 'btn red btn-outline'
    },
    // automatically close when click [OK button]
    closeWhenOK: {
        type: Boolean,
        default: false
    }
}
```

# License
MIT