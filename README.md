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
   Use the rest countries API url -> https://restcountries.eu/rest/v2/all and display all the country flags in console
   
 **ANSWER:**
 
 var  request= new XMLHttpRequest();
 request.open('GET','https://restcountries.eu/rest/v2/all',true);
 request.send();
 request.onload=function(){
 var data=JSON.parse(request.response);
 for(i=0;i<data.length;i++){
    console.log(data[i].flags);
    }
    }
 
**** 3.QUESTION:**  

Use the same rest countries and print all countries name, region, sub region and population

**ANSWER**:

var  request= new XMLHttpRequest();
request.open('GET','https://restcountries.eu/rest/v2/all',true);
request.send();
request.onload=function(){
var data=JSON.parse(request.response);
for(i=0;i<data.length;i++){
    console.log("name: "+data[i].name+" & "+"region: "+data[i].region+" & "+"sub_region: "+data[i].sub_region+" & "+" Popultion: "+data[i].popultion);
}
}
   
