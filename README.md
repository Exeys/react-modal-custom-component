# React Modal Custom Component

A customizable React modal component

## Prerequisites

- npm
- react >=18.2.0
- styled-components >=5.3.6

## Installation

````
    npm install react-modal-custom-component
````


## Example

In this example, a button call the toggle modal function onClick that display the modal to the user.

````jsx
import React from 'react';
import { Modal, useModal } from "react-modal-custom-component";


function App() {

  const { isShowing: showModal, toggle: toggleModal } = useModal();

  return (
    <div className="App">
      <button type="button" onClick={toggleModal}>Open the modal</button>
      <Modal
                isShowing={showModal}
                hide={toggleModal}
                text="Employee Created!"
                title="HRnet - Create Employee" />
    </div>
  );
}

ReactDOM.render(<App />, appElement);
````


## Custom

##### Props

| Prop name | Description                      | Example values |
| --------- | -------------------------------- | -------------- |
| isShowing | Define if the modal is shown or not                           | Boolean: ```true```     |
| hide      |  Define the function that is called to turn on/off the modal                            | Function: ```toggleModal```
| title     | Content of the title             | String: ```This is the title```
| text      | Content of the body              | String: ```This is the body text```
| primary   | Setup the main color for the component (header & button background)  | String: ```white``` / ```rgb(125,12,89)``` / ```#FF0000```

