
Use effect will run every time the component is mounted only if it has a dependency array else it will only run on updates.
If the dependencie array is empty it will run only once when the component is first mounted, else if the dependencie array is not specified it will run at every update of any state, else if the dependencie array contains some states then it will run every time one of the states that are followed change. 

Use effect can also run when the component is unmounted if you return a clear effect function. The clear function will run once if the dependencie array is empty BUT it will run every time if there is a state variable that is changing, so the clear function in this case will run first and after that the content in the useEffect callback function will run.This happens because the value in the state that is displayed on DOM will get unmounted and then a new value will be mounted;

