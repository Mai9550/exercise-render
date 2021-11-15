#### Lesson Challenge

Read these 4 articles: [Understanding the React Component Lifecycle](http://busypeoples.github.io/post/react-component-lifecycle/), [React component’s lifecycle](https://medium.com/react-ecosystem/react-components-lifecycle-ce09239010df), [Understanding React — Component life-cycle](https://medium.com/@baphemot/understanding-reactjs-component-life-cycle-823a640b3e8d), and [React JS: what is a PureComponent?](http://lucybain.com/blog/2018/react-js-pure-component/) and answer the following questions in the #explain-it channel:

1.  Describe what the in the workspace below will render on the screen and explain why.

2.  Describe a React anti-pattern that's used in the code.

The render function of a component should be a pure function of the state and props. That is, for the given state and props, it should return the same value.

(new Date().getSeconds().toString())

Hence, for the same state and props, it will return a different value every time.

Another anti-pattern can be that the props is being copied in the state-

state = {
  update: this.props.toggle,
};

Hence, if the props changes, the state won’t be updated.
We will have to write code to handle this or it can cause bugs

3.  How do we need to modify the `Normal3` Component in order to keep it from re-rendering if the `App` Component's state remains the same?
4.  we can use React.memo() to make sure it updates only when the props have changed

This exercise is based on this sandbox: https://codesandbox.io/s/3vpp84yp5.
