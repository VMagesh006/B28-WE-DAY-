# B28-WE-DAY-4
**1. QUESTION:**
 How to compare two JSON have the same properties without order?
var obj1 = { name: "Person 1", age:5 };
var obj2 = { age:5, name: "Person 1" };

**ANSWER:**

var obj1 = { name: "Person 1", age:5 };
var obj2 = { age:5, name: "Person 1" };

let flag = true;
if(Object.keys(obj1).length==Object.keys(obj2).length){
    for(mags in obj1){
      if ( obj1[mags]==obj2[mags]){
          flag = true;
      }
      else{
          flag = false;
          break;
      }
    
    }
}
    else{
        
       flag = false; 
    }
    console.log(flag);
    
    **OUTPUT: True**
    
   ** **2.QUESTION****
   
   
