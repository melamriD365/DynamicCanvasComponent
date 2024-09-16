# DynamicCanvasComponents 

**DynamicCanvasComponents** is a library offering reusable components for Canvas Apps and Model-driven app Custom Pages.

## DynamicTable Component 📊

The **DynamicTable** component is designed to simplify data display by allowing you to create a customizable table that can be reused across different screens and projects. It helps avoid the repetitive task of recreating tables for each data source and project, ensuring a consistent and efficient user experience.

### Installation and Setup 🚀

1. **Download the Unmanaged Solution** 
   - Download the latest unmanaged solution from the [Releases](#) section.

2. **Install the Solution** 
   - Import the unmanaged solution into your Power Apps environment using the standard import process.

3. **Add the Component to Your Canvas App** 
   - Open your Canvas App, go to **Insert > Custom Components**, and add the **DynamicTable** component.

4. **Start Using the Component** 
   - Configure the **DynamicTable** component with your data and adjust settings as needed.

### Configuration ⚙️

Once the **DynamicTable** component is added to your app, you can configure it by setting the following input properties:

1. **`Data`** (type: text)  
   - This property accepts a JSON array that represents the data to be displayed in the table. The component dynamically renders the table based on this input.

2. **`Columns`** (type: table) 
   - Define the structure of the table columns using this property. This includes column names, data types, and whether they are visible or hidden.

3. **`selectorHoverFill`** (type: color) 
   - Sets the color that appears when hovering over a row in the table. This enhances user experience by providing visual feedback when interacting with rows.

4. **`selectorPressedFill`** (type: color) 
   - The color that is applied when a row is pressed or clicked. This helps users identify their selection.

5. **`selectorFill`** (type: color) 
   - Defines the default background color of the selector column (the first column that contains the checkboxes or selection markers).

6. **`headerFill`** (type: color) 
   - Specifies the background color for the table header row, allowing you to customize the visual appearance of the table’s header.

7. **`CalculatedWidth`** (output: number)  
   - This is an output property that provides the calculated width of the entire table. It automatically adjusts based on the visibility and width of individual columns.

8. **`selectedRow`** (output: text) 
   - An output property that returns the currently selected row as a JSON string. You can use this property to capture and interact with user selections.

### 7. Examples 📸

This section provides an example of how to configure the **DynamicTable** component with a JSON dataset and column settings.

#### Example Data 📝

Here’s a sample JSON array representing country details that you can use as the **`Data`** input for the **DynamicTable** component:

```json
[
    {
        "Country": "United States",
        "Capital": "Washington, D.C.",
        "Population": 331002651,
        "Currency": "USD",
        "Language": "English",
        "Continent": "North America",
        "Timezone": "UTC-5",
        "GDP": 21137518,
        "Area": 9833520,
        "CallingCode": "+1"
    },
    {
        "Country": "Canada",
        "Capital": "Ottawa",
        "Population": 37742154,
        "Currency": "CAD",
        "Language": "English/French",
        "Continent": "North America",
        "Timezone": "UTC-5",
        "GDP": 1647115,
        "Area": 9984670,
        "CallingCode": "+1"
    },
    {
        "Country": "Brazil",
        "Capital": "Brasília",
        "Population": 212559417,
        "Currency": "BRL",
        "Language": "Portuguese",
        "Continent": "South America",
        "Timezone": "UTC-3",
        "GDP": 1444873,
        "Area": 8515767,
        "CallingCode": "+55"
    },
    {
        "Country": "Germany",
        "Capital": "Berlin",
        "Population": 83783942,
        "Currency": "EUR",
        "Language": "German",
        "Continent": "Europe",
        "Timezone": "UTC+1",
        "GDP": 3845630,
        "Area": 357022,
        "CallingCode": "+49"
    }
]
```

#### Column Definitions and Structure 📐

To define the columns of the table, you can use the **`Columns`** property. This property allows you to specify the column names, widths, and visibility settings for each column. In this example, the following Power Fx expression is used to automatically generate the column definitions:

```powerfx
AddColumns(ColumnNames(First(ParseJSON(Self.Data))), "_width", 200, "_visible", true)
```

1. **`_width:`**  Specifies the width of each column, in this case, set to 200 pixels.
2. **`_visible:`** Defines whether each column is visible. Here, all columns are set to true (visible).

This setup ensures that all columns from the JSON data will be displayed in the table with a default width of 200 pixels.

#### Customizing Appearance 
You can further customize the table's appearance by setting various properties:

3. **`HeaderFill: Color.WhiteSmoke`**  Sets the background color of the table header to a light gray (WhiteSmoke).

4. **`selectorHoverFill: RGBA(180, 214, 250, 0.25) `**  Applies a semi-transparent blue color when hovering over a row, providing feedback for user interaction.

5. **`selectorFill: RGBA(180, 214, 250, 0.25)`** Sets the default background color for the selector (first column) to a matching blue.

6. **`selectorPressedFill: Color.Transparent `** Ensures no color change when a row is pressed.

### 9. Contributing 🤝

We welcome contributions from the community! To contribute to the **DynamicCanvasComponents** project:

- **Example App**: Please refer to the included example Canvas App in the solution for guidance on how to use the components and ensure consistency.

- **Pull Requests**: Feel free to submit pull requests with improvements, new features, or fixes. Make sure your changes are well-tested and documented.

- **Issue Reporting**: If you encounter any issues or have feature suggestions, open an issue in the [Issues](https://github.com/melamriD365/DynamicCanvasComponent/issues) section.

Your contributions help make this project better for everyone. Thank you for your support! 🙌

