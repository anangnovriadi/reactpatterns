# Destructuring rest/spread operator

The `...` rest operator gathers the rest of the items in the props object argument and puts them in the variable rest.

The `...` rest in the JSX is actually JSX syntax for spreading the props in the the rest object into individual props.

Without using rest/spread:

```
function Modal(props) {
  var onClick = props.onClick;
  var show = props.show;
  var backdrop = props.backdrop;

  return (
    <Modal show={show} backdrop={backdrop}>
      <Button onClick={onClick}>Next</Button>
    </Modal>
  );
}
```

Here is an example destructuring rest/spread operator:

```
function Modal({ onClick, ...rest }) {
  return (
    <Modal {...rest}>
      <Button onClick={onClick}>Next</Button>
    </Modal>
  );
}
```