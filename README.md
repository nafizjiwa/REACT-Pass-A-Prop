# REACT-Pass-A-Prop

### Passing a variable to a functional child component in React.<br/>
You can do it in a similar way to how you pass props to class components. Here’s how you can do it:<br/>
Define the variable in the parent component: Create the variable within the parent component.<br/>
Pass the variable as a prop: Include the variable as a prop in the `child component's JSX tag`.<br/>
Access the variable in the child component: Retrieve the variable in the child component via props.<br/>
Here’s an example to illustrate:

##### ParentComponent.js:

        import React from 'react';
        import ChildComponent from './ChildComponent';

        const ParentComponent = () => {
          const message = 'Hello from the Parent Component!';
        
          return (
            <div>
              <h1>Parent Component</h1>
              <ChildComponent message={message} />
            </div>
          );
        };

        export default ParentComponent;
##### ChildComponent.js:

        import React from 'react';
        
        const ChildComponent = ({ message }) => {
          return (
            <div>
              <h2>Child Component</h2>
              <p>{message}</p>
            </div>
          );
        };
        
        export default ChildComponent;


###### In this example:<br/>
A variable message is defined in the ParentComponent.<br/>
This variable is passed to the ChildComponent as a prop named message.<br/>
The ChildComponent accesses the variable via message prop and displays it in a paragraph.<br/>
😊 Happy coding<br/>


### Passing a function to a functional child component in React:

Define the function in the parent component: Create the function within the parent component.<br/>
Pass the function as a prop: Include the function as a prop in the `child component's JSX tag`.<br/>
Access the function in the child component: Retrieve the function in the child component via props.<br/>
Here’s an example to illustrate:<br/>

##### ParentComponent.js:

      import React from 'react';
      import ChildComponent from './ChildComponent';
      
      const ParentComponent = () => {
        const handleButtonClick = () => {
          alert('Button clicked!');
        };
      
        return (
          <div>
            <h1>Parent Component</h1>
            <ChildComponent onButtonClick={handleButtonClick} />
          </div>
        );
      };
      
      export default ParentComponent;
##### ChildComponent.js:

      import React from 'react';
      
      const ChildComponent = ({ onButtonClick }) => {
        return (
          <div>
            <h2>Child Component</h2>
            <button onClick={onButtonClick}>Click Me</button>
          </div>
        );
      };
      
      export default ChildComponent;

In this example:
The handleButtonClick function is defined in the ParentComponent.<br/>
This function is passed to the ChildComponent as a prop named onButtonClick.<br/>
The ChildComponent accesses the function via the onButtonClick prop and uses it as the click handler for the button.<br/>
😊 Happy coding! 🎨 <br/>


