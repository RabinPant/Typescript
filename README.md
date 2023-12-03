# Typescript

### Why we need this?
 Answer is pretty simple, in a large prod project we need something that is strongly typed and also showcases the compile time error in our local itself.<br>
 so using javascript in react we may face lots of runtime error after deploying the application. But with typescript it will be pretty simpler, since it will transpile and can log error locally itself<br>

 ### how can we use it?
 we can simply install typescript and add a typescript config file which will help us to start TS.



 ### Defining a variable:
 ```
 let <variableName>:<type> = <initial value>;
```

```
let found:boolean = true;
```

```
let grade:number = 88.6;
let firstName: string = "Anup";
let lastName: string = 'kumar';
```

Here in above code we can assign new values to the same variable: for example<br>
```
grade = 90;
firstName = "rabin";
lastName= "pant";
```
This is possible but if we try to add grade  = "rabin" then it will be a compile error because of type mismatch<br>

To add any values to a variable we can do this:
```
let myData:any  = 50.0;
myData = false;
myData = "rabin"
```
Since we define varibale as "any" we can assign anything
<br>
Complile the file with "tsc sample-types.ts" <br>
we will get the javascript file and we can run that file: <br>
node sample-types.js


