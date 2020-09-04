# Array Pool
Allows for "renting" arrays for intermediate storage without generating any garbage.

## Installation
- Inside Unity, click `Window/Package Manager`.
- Click `+` at the left top corner and select the option `Add package from git URL...`.
- Paste the URL of this repository in the text box.
- Install the package.


## Code example
```c#
// getting the pool
var pool = ArrayPool.Instance;
// get an array with the minimum length of 10
var array = pool.Rent(10);
// do work with the array
...
// return the array
pool.Return(array);
```