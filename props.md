### Remember

Answer these on your own, then compare answers as a group

1.  What are props?
  properties that we can use to pass data between components
  *props is an object available to the component*
  *props are data being passed into a component*
2.  How do you pass props from a parent to a child?
  *We pass props into the child using the child's component tag*
  *We set up the props on the child's component tag by saying <whatever property nam>=<hardcoded data OR a reference to existing data using curly braces
  
3.  How do you access props from a class based child component?
  *From within JSX, we would say {this.props.<prop name>} and outside of JSX we would simply say this.props.<prop name>*

4.  How do you access props from a functional component?
  props.<prop name>
5.  How do you bind a function to a parent component so that it can be passed to a child?
  *From within the constructor outside of our this.state, we would say this.<function name> = this.<function name>.bind(this)*
  *We can use lexical binding by not having to use the bind method AND by making our function an arrow function*

### Understand

Discuss this question in pairs if you have a 4-person group

6.  What's happening in this component?

```jsx
import React, { Component } from "react";

class Queue extends Component {
  constructor(props) {
    super(props);

    this.state = {
      questions: []
    };

    this.askQuestion = this.askQuestion.bind(this);
    this.answerQuestion = this.answerQuestion.bind(this);
  }
  askQuestion(newQuestion) {
    const questions = [...this.state.questions, newQuestion];
    this.setState({ questions });
  }
  answerQuestion(index) {
    const questions = [...this.state.questions];
    questions.splice(index, 1);
    this.setState({ questions });
  }
  render() {
    <div className="queue-container">
      <h1>The Queue</h1>
      <h3>{this.state.questions.length}</h3>
      <h3>questions need answers</h3>
      <Student askQuestion={this.askQuestion} />
      <Mentor answerQuestion={this.answerQuestion} />
    </div>;
  }
}
```

### Apply

Try these on your own, but work together if you start to get stuck.

7.  Using the `Queue` component above, create a `Student` component that can add a question as a string and a `Mentor` component that can remove a question from the array.

### Analyze, Evaluate, Create

Discuss these questions as a group

8.  In the Queue component above, why are we holding state in the Queue component instead of Mentor or Student?
