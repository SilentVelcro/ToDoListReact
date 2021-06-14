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
