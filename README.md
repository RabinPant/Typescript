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


### loops and array:

```
let reviews: number[] = [5,5,4.5,1,3];

for(let i=0;i<reviews.length;i++){
 console.log(reviews[i]); 
}
```

```
let sportsOne: string[] = ["Golf","Cricket","Tennis","Swimming"];

for(let i=0;i<sportsOne.length;i++){
  console.log(sportsOne[i]);
}
```

##### simplified for loop

```
let sportsOne:string[] = ["golf", "Cricket", "Tennis","Swimming"];
for(let tempSport of sportsOne){
 console.log(tempSport);
}
```

```
let sportsTwo: string[] = ["golf","cricket","Tennis"];
sportsTwo.push("BaseBall");
sportsTwo.push(Futbol);
for(let i of sportsTwo){
 console.log(i);
}
```

### Classes and OOP:
```
class Customer{

  firstName:string;
  lastName:string;
}

let myCustomer = new Customer();
myCustomer.firstName = "rabin";
myCustomer.lastName = "Dixon";

```
### constructor:
```
class Customer{
 firstName: string;
 lastName: string;

 constructor(theFirst:string,thelast:string){
  this.firstName = theFrist;
  this.lastName = theLast;
 
 }

}
let myCustomer = new Customer("Mrtin", "dixon");
console.log(myCustomer.firstName);
console.log(myCustomer.lastName);

```

To prevent the compiler to generate the JS file when it shows error is:
tsc --noEmitOnError cutomer.ts

### Getter/Setter Method:
```
class Customer{

   private firstName: string;
   private lastName: string;

   public getFirstName():string{
    return this.firstName;  
   }
   public setFirstName(theFirst:string):void{
    this.fistName = theFirst;
   
   }

}
```
This is the way to do in the traditional approach <br>
but there is another way to do it as well:

#### Accessors -GET/SET

```
class customer{

  private firstName:string;
  private lastName:string;

 public get firstName():string{
  return this.firstName;
 }

 public set firstName(first:string ){
  this.firstName = first;
 }

}
```
1) you can use get and set accessor in the method
2) in the set method you dont need to write the return type of the method.

To have this feature run in the local you've to do :<br>

tsc --target ES5 --noEmitOnError customer.ts <br>

because we have this feature on after ES5.<br>

we can set all this in the tsconfig.js file. Instead of writing all in the terminal we can do so in the config file. <br>

in config file add this after initaiting config file tsc --init <br>
"target": "es5", 
    "module":"commonjs",
    "noEmitOnError": true,                              

### parameter Properties:

we saw the traditional way of constructor initializing the parameter: how can we reduce the boilerpate code:
```
class customer{

 constructor(private _firstName:string, private _lastName:string){
}
```
### modules:import and export

```
export class customer{

}
```
```
import {customer} from "./customer";
```




