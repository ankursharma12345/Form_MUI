# Form_MUI


import React, { useState } from "react";
import {
  Grid,
  InputLabel,
  MenuItem,
  Select,
  TextField,
  withStyles,
} from "@mui/material";

function App() {
  const [data, setData] = useState();
  function myFunc() {
    setData({
      Name: "Ankur Sharma",
      gender: "Male",
      EmailId: "abc@gmail.com",
      Nationality: "Indian",
      age: 23,
      phone: "0123456789",
    });
  }
  return (
    // <TextField variant = "outlined"></TextField>
    <>
      <h2>My Details</h2>
      <Grid
        container
        //spacing={2}
        rowSpacing={2}
        columnSpacing={2}
        columns={16}
      >
        <Grid item xs={6} md={12}>
          <TextField id="standard-basic" label="Name" variant="outlined" />
        </Grid>
        <Grid item xs={6} md={12}>
          <TextField id="standard-basic" label="Gender" variant="filled" />
        </Grid>
        <Grid item xs={6} md={12}>
          <TextField id="standard-basic" label="EmailId" variant="standard" />
        </Grid>
        <Grid item xs={6} md={12}>
          <TextField
            id="standard-basic"
            label="Nationality"
            variant="standard"
          />
        </Grid>
        <Grid item xs={6} md={12}>
          <InputLabel id="demo-simple-select-label">Age</InputLabel>
          <Select
            labelId="demo-simple-select-label"
            id="demo-simple-select"
            // value={age}
            label="Age"
            // onChange={handleChange}
          >
            <MenuItem value={10}>Ten</MenuItem>
            <MenuItem value={20}>Twenty</MenuItem>
            <MenuItem value={30}>Thirty</MenuItem>
          </Select>
        </Grid>
        <Grid item md={12}><TextField id="standard-basic" label="Phone No." variant="standard" /></Grid>
        <Grid item xs = {100} md={12}><button onClick={myFunc}>Click Here</button></Grid>
      </Grid>
    </>
  );
}

export default App;
