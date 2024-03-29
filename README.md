# JP-MORGANONLINE-INTERNSHIP

Based on my last knowledge update in January 2022, I don't have any specific information about a program called "JP-MORGANONLINE-INTERNSHIP." It's possible that this program has been introduced after my last update, or it could be a term or reference that is not widely known.

To obtain accurate and up-to-date information about the "JP-MORGANONLINE-INTERNSHIP," I suggest visiting the official website of JPMorgan Chase, the company behind the JP Morgan brand. Companies often provide comprehensive details about their internship programs, including application procedures, eligibility requirements, and program specifics on their official websites.

If this is a specific program within JPMorgan Chase, you may also consider reaching out to their human resources or recruitment department for further information. They can offer insights into the structure, objectives, and application process of the internship.

Remember to always rely on official and trustworthy sources when gathering information about internships or any programs, especially when it involves personal or sensitive information.

* Task 1 (Interface with a stock price data feed)

  - Car Class:
  
    Constructor: The __init__ method initializes a Car object with a default speed of 0. It also sets attributes for speed, odometer, and time.
    Accelerate: The accelerate method increases the car's speed by 5 units.
    Brake: The brake method decreases the car's speed by 5 units.
    Step: The step method updates the car's odometer based on its current speed and increments the time.
    Average Speed: The average_speed method calculates and returns the average speed of the car.
    
  - Main Section:

    In the main section, a new instance of the Car class called my_car is created. Then, a loop is initiated where the user is asked to input an action. They can choose to accelerate (A), brake (B), show the odometer (O), or show the average speed (S). Depending on the user's input, the script executes the corresponding action on the car and gives feedback. This loop will keep running until it is manually stopped.

* Task 2 (Use JPMorgan Chase & Co. frameworks and tools)

   - App.tsx Changes:
      Added a new state variable called showGraph with an initial value of false.
      Modified the renderGraph method to only render the Graph component if the showGraph state is true.
      Updated the getDataFromServer method to fetch new data from the server and update the state. It also sets the showGraph state to true. The data fetching is done repeatedly using setInterval until it reaches a limit of 1000 iterations.
  
   - Graph.tsx Changes:
      Added a console.log('rendering') statement in the componentDidMount method for debugging purposes.
      Removed an unnecessary check for the existence of a worker in the window.perspective object in the componentDidMount method.
      Updated the Perspective configurations:
        Set the view to 'y_line'.
        Defined column-pivots, row-pivots, columns, and aggregates attributes for the <perspective-viewer> element.
  
   - General Info:
      The changes made in App.tsx indicate that the graph's display is now conditional based on the showGraph state.
      The changes in Graph.tsx involve the initialization and configuration of the Perspective library, specifying how the data is visualized in the graph.
  
   - Notes:
      The console.log statements, especially the one in Graph.tsx, are likely used for debugging purposes and can be removed or adjusted based on the developer's needs.
      The clearInterval statement in the getDataFromServer method may stop the data fetching after 1000 iterations to prevent an infinite loop.

* Task 3 (Display data visually for traders.patch)

  - DataManipulator.ts Changes:
    Row Interface Modification:
    The Row interface has been updated to include new properties such as price_abc, price_def, ratio, upper_bound, lower_bound, and trigger_alert. These changes allow for a more comprehensive representation of the data.
  
  - generateRow Method Modification:
    The generateRow method has been modified to generate a single Row instead of an array of Rows. This updated Row now includes the calculated values for the newly added properties. This change improves the efficiency and accuracy of the data manipulation process.
  
  - Graph.tsx Changes:
    Schema Modification:
    The schema definition in Graph.tsx has been adjusted to incorporate the new properties: price_abc, price_def, ratio, upper_bound, lower_bound, and trigger_alert. This modification ensures that the schema accurately reflects the updated structure of the Row.
  
  - Update in componentDidUpdate:
    The componentDidUpdate method has been updated to pass an array containing the generated row to this.table.update. This change ensures that the latest data is properly updated and displayed in the graph component.
  
  - General Information:
    The changes made in DataManipulator.ts indicate a refactoring of the generateRow method to better represent the data structure and handle additional properties. These modifications may have been implemented in response to changes in the expected data format.
    
    In Graph.tsx, the adjustments to the schema and the componentDidUpdate method are made to accommodate the modified structure of the Row. These changes ensure that the graph component can accurately display and visualize the updated data.
  
  - Considerations:
    The introduction of the properties upper_bound, lower_bound, and trigger_alert suggests that these changes are aimed at handling alert triggers based on certain conditions. These new properties provide the necessary information for implementing dynamic alerts.
    
    Overall, these changes indicate a need for a more detailed and dynamic representation of the data, as evidenced by the addition of new properties in both DataManipulator and Graph. These modifications enhance the functionality and flexibility of the data manipulation and visualization processes.
