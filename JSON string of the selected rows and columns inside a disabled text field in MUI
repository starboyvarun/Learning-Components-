//To save a JSON string of the selected rows and columns inside a disabled text field in MUI,
//you can use the TextField component and set the value prop to the JSON string.
//Additionally, you need to set the disabled prop to true to make the text field read-only.


import React from "react";
import TextField from "@mui/material/TextField";

const selectedColumns = ["desk", "commodity"];
const selectedRows = [
  { desk: "A1", commodity: "Gold", price: 100 },
  { desk: "B2", commodity: "Silver", price: 50 },
  { desk: "C3", commodity: "Platinum", price: 150 }
];

const filteredRows = selectedRows.map(row =>
  selectedColumns.reduce((obj, column) => {
    obj[column] = row[column];
    return obj;
  }, {})
);

const json = JSON.stringify(filteredRows);

export default function App() {
  return (
    <TextField
      id="json-text-field"
      label="Selected Rows and Columns"
      value={json}
      disabled={true}
      fullWidth
    />
  );
}

//In this example, we first filter the selected rows and columns as we did in the previous example.
//We then define a json variable that holds the JSON string of the filtered rows.

//Inside the App component,
//we render a TextField component with an id of "json-text-field", 
//a label of "Selected Rows and Columns", a value of the json variable, and a disabled prop of true.

//When the component is rendered, 
//the text field will display the JSON string of the filtered rows, 
//and the user will not be able to edit the text field.
