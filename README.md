React 

Function --- simple function
mainly uses UI 
Stateless 



Class -
more feature rich
maintain their own private data
complex UI logic
provide lifecycle hooks



HOOKS
is new feature proposal that you use state and other react feature without writing class




JSX =
Javascript XML extension 
                
const Hello = () =>{
return (
<div>
  <h1>Hiii</h1>
</div>
)
}

export default Hello





props - function
class - this.props



Destructing props and state


import React {Components } from react 

class Welcome extends Component {
    constructor (){
        super (){
            this.State ={
                count = 0
            }
        }
    }

    increament (){
        this.setState ({
            count = this.State.count +1;
            },()=>{console.log('count',this.State.count)})
    }
    render (){
        return (
            <div> Hi </div>
            <button onClick = { ()=>{this.increament()}}>  </button>
            
        )
    }
}




destructing props

const Greet = props =>{
return (
<div>
  <h1>
    Hi {props.name} a.k.a {props.heroName}    // declared name in app.js
  </h1>
 </div>
)
}

const Greet = props =>{
 const {names,heronames} = props 
 return (
    <div>
      <h1>
         Hi {name} a.ka. {props}
      </h1>
    </div>
 )
}



for class component 
class Welcome extends Component {

    const {name ,heroName} = this.props
      render (){
          return (
              <div>
                  <h1>My name is {name} a.k.a {heroName}</h1>
              </div>
          )
      }
    
}




/// EVENT HANDLING


without () we can call this as event handler
EVENT HANDLING IN FUNCTION COMPONENT
function FunctionClick(){
function ClickHandler (){
   console.log("hi")    
}
    return (
        <div>Hi</div>
        <button onClick ={ clickHandler}>Click</button>  // dont call function use them as event
    )
}




class ClassClick extends Component {
    const ClickHandler (){
        console.log("test console click handler")
    }
    render (){
        return (
            <div>Hi</div>
            <button onClick = {this.ClickHandler}></button>
        )
    }
}


Bind - keyword
to change the state = this.setState  
this.setState = {
"this" keyword in argument handle is undefined
suppose if i click on button then it is not displaying its state then we can use bind keyword

class Eventbind extends Component {
    constructor (){
        super ()
        this.state = {
            message : 'hi'
        }
    }
    clickHandler () {
        this.setState ({
            message ="Goodbye"
        })
    }
    render (){
        return (
            <h1>Hi hello this is us</h1>
            <button onClick = {this.clickHandler.bind(this)}>Click</button>
        )
    }
}
    


ANOTHE APPROACH 

class EvenBind extends Component {
    constructor ()
    {
        super ()
        this.state = {
            message :'Hi'
        }
    }
    ClickHandler = () =>{
        this.setState ({
            message :"goodbye"
        })
    }
    render ()
    {
        return (
            <div>this.state.message</div>
            <button onClick ={this.ClickHandler}>Click</button>
        )
    }
}






    
    


