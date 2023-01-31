## Class Component and State 2

## Concepts in Focus
* setState() Object Syntax
* Sending Function as Callback
* Input Element
* Searchable Users List Application

# search user list

* Add input Elements
* Filter user list based on input values
* Dispay filterd user list

# Deleting User

* maintain user list in the state 
* Add delete button
* Add delete function functionality
------------------------------------------------------------------------

#  setState() Object Syntax:

The setState() object syntax can be used while updating the state to the value that is independent of the previous state.

# Syntax:
this.setState(
  {propertyName1: propertyValue1},
  {propertyName2: propertyValue2}
  // and many more...
);
------------------------------------------------------------------------
#  Callback vs Object

# Callback:

this.setState(prevState => {
  return { count: prevState.count + 1 };
});


It is used while updating the state to a value, which is computed based on the previous state.
-----------

# Object:

this.setState({ quantity: 2 });

It is used while updating the state to a static value.

------------------------------------------------------------------------

##  Sending Function as Callback

* We can pass functions as props to child components.

# Syntax:

<ComponentName functionName={this.functionName} />

------------------------------------------------------------------------

##  Input Element:

In React, the Input Element value can be handled in two ways:

Controlled Input
Uncontrolled Input

# Controlled Input

If the Input Element value is handled by a React State then it is called Controlled Input. Controlled Inputs are the React Suggested way to handle Input Element value.

# Example:

import {Component} from 'react'

class App extends Component {
  state = {
    searchInput: '',
  }

  onChangeSearchInput = event => {
    this.setState({
      searchInput: event.target.value,
    })
  }

  render() {
    const {searchInput} = this.state
    return (
      <input
        type="text"
        onChange={this.onChangeSearchInput}
        value={searchInput}
      />
    )
  }
}

export default App
------------------------------------------------------------------------

## Uncontrolled Input

If the Input Element value is handled by the browser itself then it is called Uncontrolled Input.

Uncontrolled inputs are like traditional HTML form inputs. Its value can only be set by a user, but not programmatically. However, in controlled input value is programmatically handled using React State.

# Example:

<input type="text" />
------------------------------------------------------------------------

## Publish 

# https://userprofilesai.ccbp.tech

