# xjsx

A jsx shorthand middleware library.  
`q` and `if` props are added to make coding easy.  
It is compatible to Fresh projects.

## setup

In deno.json, add the following configurations.
```json
  "imports": {
    ... (other imports),
    "xjsx/jsx-runtime": "https://deno.land/x/xjsx@<version>/jsx-runtime.ts",
  },
  "compilerOptions": {
    "jsx": "react-jsx",
    "jsxImportSource": "xjsx"
  },
```

## q props

You can use q props as an alternative to class props
```tsx
  <div q="foo" />
```
is equivalent to
```tsx
  <div class="foo" />
```

## multiple class names

Props `q` accepts an array of class values
```tsx
  <div q={["foo", "bar", "buzz"]} />
```

## q props for function component
```tsx
  const Foo = () => <div>hoge<div>
  <Foo q="foo">
```

Any function components accept `q` props, then the specified class name is applied to the root dom element of the component.


## if props
There is `if` props added for conditional rendering. It is similar to `ngIf` in angular or `v-if` in vue.
```tsx
  <div if={someCondition}>hello</div>
```
it results equivalent to
```tsx
  {someCondition && <div>hello</div> }
```

Happy Coding!!

## License
MIT


