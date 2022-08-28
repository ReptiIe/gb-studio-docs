---
sidebar_position: 2
#
# This file is autogenerated. DO NOT MODIFY DIRECTLY
#
---

import ScriptEventPreview from '@site/src/components/ScriptEventPreview';

# Math

## Evaluate Math Expression
<ScriptEventPreview title={"Evaluate Math Expression"} fields={[{"key":"variable","type":"variable","defaultValue":"LAST_VARIABLE","width":"50%"},{"key":"expression","type":"matharea","rows":5,"placeholder":"e.g. 5 + (6 * $health)...","defaultValue":""}]} />


## If Math Expression
<ScriptEventPreview title={"If Math Expression"} fields={[{"key":"expression","type":"matharea","rows":5,"placeholder":"e.g. $health >= 0...","defaultValue":""},{"key":"true","label":"True","type":"events"},{"key":"__collapseElse","label":"Else","type":"collapsable","defaultValue":true,"conditions":[{"key":"__disableElse","ne":true}]},{"key":"false","label":"False","conditions":[{"key":"__collapseElse","ne":true},{"key":"__disableElse","ne":true}],"type":"events"}]} />

- **True**  
- **False**  

## Math Functions
<ScriptEventPreview title={"Math Functions"} fields={[{"key":"vectorX","type":"variable","defaultValue":"LAST_VARIABLE"},{"key":"operation","type":"select","options":[["set","Set To"],["add","Add"],["sub","Subtract"],["mul","Multiply"],["div","Divide"],["mod","Modulus"]],"defaultValue":"set","width":"50%"},{"key":"other","type":"select","options":[["true","True"],["false","False"],["var","Variable"],["val","Value"],["rnd","Random"]],"defaultValue":"true","width":"50%"},{"key":"vectorY","type":"variable","conditions":[{"key":"other","eq":"var"}],"defaultValue":"LAST_VARIABLE"},{"key":"value","type":"number","conditions":[{"key":"other","eq":"val"}],"min":-32768,"max":32767,"defaultValue":"0"},{"key":"minValue","type":"number","conditions":[{"key":"other","eq":"rnd"}],"min":-32768,"max":32767,"label":"Min value","defaultValue":"0","width":"50%"},{"key":"maxValue","type":"number","conditions":[{"key":"other","eq":"rnd"}],"min":-32768,"max":32767,"label":"Max value","defaultValue":"32767","width":"50%"},{"key":"clamp","type":"checkbox","label":"Clamp value between 0 and 255","conditions":[{"key":"operation","in":["add","sub","mul"]}],"defaultValue":false,"alignCheckbox":true}]} />

- **Min value**  
- **Max value**  
- **Clamp value between 0 and 255**  

## Seed Random Number Generator
<ScriptEventPreview title={"Seed Random Number Generator"} fields={[{"label":"Place this to run in response to user input to ensure random numbers change between playthroughs"}]} />

