# DynamicCanvasComponents 🎨

**DynamicCanvasComponents** is a library offering reusable components for Canvas Apps and Model-driven app Custom Pages.

## DynamicTable Component 📊

The **DynamicTable** component is designed to simplify data display by allowing you to create a customizable table that can be reused across different screens and projects. It helps avoid the repetitive task of recreating tables for each data source and project, ensuring a consistent and efficient user experience.

### Installation and Setup 🚀

1. **Download the Unmanaged Solution** 📥
   - Download the latest unmanaged solution from the [Releases](#) section.

2. **Install the Solution** ⚙️
   - Import the unmanaged solution into your Power Apps environment using the standard import process.

3. **Add the Component to Your Canvas App** 🖼️
   - Open your Canvas App, go to **Insert > Custom Components**, and add the **DynamicTable** component.

4. **Start Using the Component** 🛠️
   - Configure the **DynamicTable** component with your data and adjust settings as needed.

### Configuration ⚙️

Once the **DynamicTable** component is added to your app, you can configure it by setting the following input properties:

1. **`Data`** (type: text) 📊  
   - This property accepts a JSON array that represents the data to be displayed in the table. The component dynamically renders the table based on this input.

2. **`Columns`** (type: table) 📝  
   - Define the structure of the table columns using this property. This includes column names, data types, and whether they are visible or hidden.

3. **`selectorHoverFill`** (type: color) 🎨  
   - Sets the color that appears when hovering over a row in the table. This enhances user experience by providing visual feedback when interacting with rows.

4. **`selectorPressedFill`** (type: color) 🎨  
   - The color that is applied when a row is pressed or clicked. This helps users identify their selection.

5. **`selectorFill`** (type: color) 🎨 
   - Defines the default background color of the selector column (the first column that contains the checkboxes or selection markers).

6. **`headerFill`** (type: color) 🎨 
   - Specifies the background color for the table header row, allowing you to customize the visual appearance of the table’s header.

7. **`CalculatedWidth`** (output: number) 📏  
   - This is an output property that provides the calculated width of the entire table. It automatically adjusts based on the visibility and width of individual columns.

8. **`selectedRow`** (output: text) 🔍  
   - An output property that returns the currently selected row as a JSON string. You can use this property to capture and interact with user selections.
