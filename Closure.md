#Closure

----------
1.Closure is when function remembers its value ..even when its called outside the lexical scope.

Example:-
function foo(){
   var bar = "Its me";
   return function(){ console.log(bar); };
}
foo();
foo()();//console.log(bar);


2.for(var i=0;i<5;i++){
  setTimeOut(function(){ console.log(i) },i*100);
}

output:-4,4,4,4,4
Explanation:- setTimeout function will get store in Stack queue when all events get over then stack will get empty after that mean last value will only get pointed out.

for(var i=0;i<5;i++){ 
 (function(i){
      setTimeOut(function(){ console.log(i) },i*100);
   })(i);
}
IIFE

for(let i =0;i<5;i++){
  console.log(i);
}
let keyword

