# react-nanodegree-life-cycle-events-summary-exercise

#Lesson Challenge
Read these 4 articles: Understanding the React Component Lifecycle, React component’s lifecycle, Understanding React — Component life-cycle, and React JS: what is a PureComponent? and answer the following questions in the #explain-it channel:

Describe what the in the workspace below will render on the screen and explain why.

Describe a React anti-pattern that's used in the code.

The render function of a component should be a pure function of the state and props. That is, for the given state and props, it should return the same value.

(new Date().getSeconds().toString())

Hence, for the same state and props, it will return a different value every time.

Another anti-pattern can be that the props is being copied in the state-

state = { update: this.props.toggle, };

Hence, if the props changes, the state won’t be updated. We will have to write code to handle this or it can cause bugs

How do we need to modify the Normal3 Component in order to keep it from re-rendering if the App Component's state remains the same?
we can use React.memo() to make sure it updates only when the props have changed
This exercise is based on this sandbox: https://codesandbox.io/s/3vpp84yp5
