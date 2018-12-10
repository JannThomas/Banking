# Banking

## Objects

### Step (A step might be a string with the path to a json file representing a step object)
| Key | Type | Description | Optional | Default Value |
| :---: | :---: | :---: | :---: | :---: |
| type | String | The type of the step. See below for options. | no | - |
| nextStep | Step | The step to take after this one has been evaluated. This does not wait for asyncronious tasks to complete (for example, a web request). | yes | - |

The type values are appended to the step object.

#### Types

##### request

| Key | Type | Description | Optional | Default Value |
| :---: | :---: | :---: | :---: | :---: |
| url | String | The url. | no | - |
| method | String | The HTTP method. | yes | GET |
| resultVariable | String | The state variable to put the result in. | yes | result |
| onSuccess | Step | The step when the url request is successful. | yes | - |
| onFailure | Step | The step when the url request is not successful. | yes | - |

##### regex

| Key | Type | Description | Optional | Default Value |
| :---: | :---: | :---: | :---: | :---: |
| variable | String | The variable to apply the regular expression to. | no | - |
| expression | String | The expression. | no | - |
| resultVariable | String | The state variable to put the result in. This will contain an array of arrays containing all group data  | no | - |
| onSuccess | Step | The step when the regex is successful. | yes | - |
| onFailure | Step | The step when the regex is not successful. | yes | - |

##### 

