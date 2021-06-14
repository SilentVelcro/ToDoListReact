**-- 75.Setting CSS Classes Dynamically --**

We can use a template literal to control boolean statements for dynamic values using { useState }
<Courseinput.js> = <div className={`form-control ${!isValid ? "invalid" : ""}`}>

<Courseinput.js> = style={{
            borderColor: !isValid ? "red" : "#ccc",
            background: !isValid ? "salmon" : "transparent",
          }}

**-- 76. Introducing Styled Components --**

o - clear terminal with = CTRL + C
o - than enter: npm install --save styled-components
o - npm install --save styled-components

you can use global css class names with values and add them to a element so that it can't spill over to other components of the app. Unique to that component! in the example below it shows that you use the backtick (``) and place the elements inside.

const Button = styled.button`
width: 100%;
font: inherit;
padding: 0.5rem 1.5rem;
border: 1px solid #8b005d;
color: white;
background: #8b005d;
box-shadow: 0 0 4px rgba(0, 0, 0, 0.26);
cursor: pointer;

@media (min-width: 768px) {
width: auto;
}

&:focus {
outline: none;
}

&:hover,
&:active {
background: #ac0e77;
border-color: #ac0e77;
box-shadow: 0 0 8px rgba(0, 0, 0, 0.26);
}
`;

**-- 77. Styled Components & Dynamic Props --**
//--components in JSX should start with a capital letter. <FormControl>
//-- can use props to make special senarios like invalid using useState.

const FormControl = styled.div`
margin: 0.5rem 0;

& label {
font-weight: bold;
display: block;
margin-bottom: 0.5rem;
color: ${(props) => (props.invalid ? "red" : "black")};
}

& input {
display: block;
width: 100%;
border: 1px solid ${(props) => (props.invalid ? "red" : "#ccc")};
background: ${(props) => (props.invalid ? "#ffd7d7" : "transparent")};
font: inherit;
line-height: 1.5rem;
padding: 0 0.25rem;
}

& input:focus {
outline: none;
background: #fad0ec;
border-color: #8b005d;
}
`;

**--78. Styled Components & Media Queries--**
