//Objects

const student = {
    name:"anmol",
    marks:96,
    printMarks:function (){
        console.log("marks=",this.marks);
    }
};

//Prototype   to add 1st obj`s function in 2nd

const employee={
    calTax(){
        console.log("tax rate is 10%");
    }
}

const anmolShivam={
    salary:50000,
};

const anmolShivam2={
    salary:50000,
    calTax(){
        console.log("tax rate is 30%");
    }
};    

anmolShivam.__proto__=employee;

anmolShivam2.__proto__=employee;

//Classes   is a blueprint of objects

class Uber{
    start(){
        console.log("start");
    }

    stop(){
        console.log("stop");
    }
    bookRide(ride) {
        this.rideName=ride;
    }

};

//create object in class

let Rapido = new Uber();

//Add variable in class
Rapido.bookRide("Rapido");

//Constructor method

class MyClass{
    constructor(st,mark){
        console.log("create a constructor");
        this.stuNAme=st;
        this.mark=mark;
    }

    passStudent(){
        console.log("total number of passStudent is 49");
    }

    failStudent(){
        console.log("total number of failStudent is 3");
    }
};

let stu = new MyClass("preet",25);
console.log(stu);

//Inheritance  property given to from parent class to child class

class Parent{
    hello(){
        console.log("hello");
    }
}

class Child extends Parent{}

let obj= new Child();

class Engineer{
    coding(){
        console.log("coding");
    }

    rest(){
        console.log("no rest");
    }
}

class Engi extends Engineer{
    repeat(){
        console.log("no rest, just coding back to back work");
    }
}

let anmol = new Engi();

//Super Keyword  access properties from child class to parent class

class Person{
    constructor(){
        console.log("enter parent constructor");
        this.species = "homo sapiens";
    }
    eat(){
        console.log("eat");
    }
}

class Foodie extends Person{
    constructor(menu){
        console.log("enter child constructor");
        super(); //to invoke parent class constructor
        this.menu = menu;
        console.log("exit child constructor");
    }
    work(){
        console.log("no work, whole day eating");
    }
}

let foodObj = new Foodie("pizza,burger");
