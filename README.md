# Ractive Component Bootstrap Modal

Modal component for Ractive that uses Twitter Bootstrap's CSS.

## Requirements

* Use ```bootstrap```'s stylesheets.
* Add this to your stylesheets:

```css
.modal-backdrop {
	opacity: 0.5;
}
```

## Usage

```shell
npm install skyrpex/ractive-components-bootstrap-modal --save-dev
```

### app.js

```js
export default Ractive.extend({
  template: require('./app.hbs'),
  components: {
    Modal: require('ractive-components-bootstrap-modal')
  },
  data() {
    return {
      // Will use this to show/hide the modal
      showModal: false
    }
  }
});
```

### app.hbs

```mustache
<div class="container">

  <h1>Ractive Bootstrap Modal</h1>

  <button type="button" class="btn btn-primary" on-click="toggle('showModal')">Show modal</button>

  <!-- Modal component -->
  <Modal show="{{showModal}}">
    <div class="modal-dialog">
      <div class="modal-content">
        <div class="modal-header">
          <button type="button" class="close" on-click="toggle('showModal')" aria-label="Close"><span aria-hidden="true">&times;</span></button>
          <h4 class="modal-title">Modal title</h4>
        </div>
        <div class="modal-body">
          <p>One fine body&hellip;</p>
        </div>
        <div class="modal-footer">
          <button type="button" class="btn btn-default" on-click="toggle('showModal')">Close</button>
          <button type="button" class="btn btn-primary">Save changes</button>
        </div>
      </div>
    </div>
  </Modal>

</div>

```

## Demo

Try the demo [here](https://cdn.rawgit.com/skyrpex/ractive-components-bootstrap-modal/master/demo/index.html).
