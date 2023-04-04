
# [Cannot update a component while rendering a different component warning](https://stackoverflow.com/questions/62336340/cannot-update-a-component-while-rendering-a-different-component-warning)

const getRefForFilters = (ref) => {

    //get ref from FilterCriterion.jsx

    useEffect(() => {

      setFiltersToBeDisplayedRef(ref);

    }, []);

  };

When you have a state in app that you try to update => you try to update the app component.
The thing is that you cannot update the component while you instantly change a state that is in the app from a child component, so a solution would be to use useEffect hook to update it only after the app has rendered => the child component is also rendered.
