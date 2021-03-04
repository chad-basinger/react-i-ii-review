### Remember

Answer these on your own, then compare answers as a group

1.  What is React?
  -Javascript library used to package all your structure, styling, and functionality together
  *uses component based architecture and unidirectional data flow
  *has it's own Virtual DOM
2.  What is create-react-app?
  -a FB owned terminal command - works with node, that builds the very basics for a react app to work
  *Package that sets up a new React project*
  *
3.  What is Component Based Architecture?
  *The concept of encapsulating individual pieces of code to bring together into a larger project/app*

4.  What is JSX?
  *It is the syntax that React uses (looks like HTML)*
  *Eventually transpiled into regular JS function calls*

5.  What is the virtual DOM?
temporary DOM, without having us actually change the data. We can choose if/what to push from temporary DOM to the original DOM. speeds up the app using virtual DOM
*Light-weight copy of the DOM, React updates the virtual DOM when any changes to a component are made, then uses the virtual DOM*
*to decide what parts of the actual DOM to change, and ONLY updates pieces that need to be updated*

6.  What is unidirectional (one-way) data flow?
data flows down, actions flow up
*Data can only flow one way to other parts of the application(e.g. parent to child using props)*
### Understand

Discuss these questions in pairs if you have a 4-person group

7.  Summarize what happens when you run `create-react-app my-app`
  -terminal command that builds a react package, and names it my-app
8.  Explain what this code does:

```jsx
import React from "react";

const Mentor = props => (
  <div className="mentor-container">
    <h1 className={props.title === "Lead Mentor" ? "lead" : ""}>Tim Biles</h1>
    <ul>
      <li>Fort Worth, TX</li>
      <li>My email address is timbilestimbiles@gmail.com</li>
    </ul>
  </div>
);

export default Mentor;
```

9.  Explain how data is passed from a parent component to a child component.

### Apply

Try these on your own, but work together if you start to get stuck.

10.  Use `create-react-app` to create a new React application called `student-directory`

11.  Use the code from `Mentor` above to create a new functional, stateless component called `User` with a list of friends. Hard code the list of friends, do not use state or props.

### Analyze, Evaluate, Create

Discuss these questions as a group

12. What are the benefits and drawbacks of using a tool like create-react-app?

13. Compare and contrast JSX with other templating options, such as those used in Angular or Vue

14. Compare and contrast one-way data flow with two-way data binding.
