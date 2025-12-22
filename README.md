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
