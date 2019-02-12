#Big (O) of Nested Loop with Multiplication
~~~
const n = 10;
const pie = 3.14;
let sum = 0;

var i = 1;

while (i < n) {
    console.log(pie);
    for (var j = 0; j < i; j++) {
        sum = sum + 1;
    }
    i *= 2;

}
console.log(sum)

 
 Statement                                Number of Executions
 n = 10                                     1

 sum = 0                                      1

 pie = 3.14                                    1

 console.log(pie)                              log2(n)

 i = 1,(1)2,(1*2)2, (1×2×2)2,⋯,n             ≤nlog2(n)

 sum+=1                                              ≤nlog2(n)

i*=2                                             log2(n)               

console.log(sum)                                 1


running time Complexity

1+1+1+log2(n)+nlog2(n)+nlog2(n)+1
4+2log2(n)+2(nlog2(n))
4+2log2(n)+2nlog2(2)

Now to find the Big-Oh complexity,

drop leading constants=nlog2(n)+n
drop lower constant=nlog2(n)

Big O Time Complexity:O(nlog2(n))
~~~

# Nested Loop with Multiplication (Advanced)
~~~
const n = 10;
const pie = 3.14;
let sum = 0;
var i = 1;
while (i < n) {
    console.log(pie);
    for (var j = 1; j < n; j += 2) {
        sum = sum + 1;
    }
    i *= 3;
}
console.log(sum)



Statement                                Number of Executions
 n = 10                                     1

 sum = 0                                      1

 pie = 3.14                                    1

   i = 1                                        1

   while i < n:                               log3(n)

 console.log(pie);                                   log3(n)      

 for (var j = 1; j < n; j += 2)               log3 (n) *n/2                                

console.log(sum)                                 1

sum++;	                                         log3(n)*n/2

console.log(sum)                                        1


1+1+1+1+1+log3(n)+log3(n)+(log3(n)*n/2)+(log3(n)*n/2)
5+2log3(n)+2(nlog3(n))/2
5+2log3(n)+nlog3(n)

Now, to find the big O complexity,

Drop the leading constants=>nlog3(n)+n
Drop lower order terms=>nlog3(n)

Big O Time Complexity:O(nlog3(n))

~~~

#Nested Loop with Multiplication (Complex)
~~~
const n = 10;
const pie = 3.14;
let sum = 0;
var j = 1;
for (var i = 1; i < n; i += 3) {
    console.log(pie);
    while (j < n) {
        sum = sum + 1;
        j *= 3;
    }

}

console.log(sum)




Statement                                Number of Executions
 n = 10                                     1

 sum = 0                                      1

 pie = 3.14                                    1

 for (var i = 1; i < n; i += 3)               n/3

 console.log(pie)                              n/3


    while j < n:                             n/3*log3(n)

 sum+=1                                       n/3*log3(n)

     j*=3                                     n/3*log3(n)              

console.log(sum)                                 1


Running Time Complexity

1+1+1+n/3+n/3+n/3*log3(n)+n/3*log3(n)+n/3*log3(n)+1
4+2n/3+nlog3(n)

Now to find the big O complexity,

leading constants =>n+nlog3(n)

lower order constant=nlog3(n)

now, big O Time Complexity: O(nlog_3(n)).

~~~


#Challenge 6 : Nested Loop with Multiplication (Pro)

~~~
const n = 10;
const pie = 3.14;
let sum = 0;
var j = 1;
for (var i = 0; i < n; i++) {
    console.log(pie);
    while (j < i) {
        sum += 1;
        j *= 2;

    }

}
console.log(sum)



Statement                                Number of Executions
 n = 10                                     1

 sum = 0                                      1

 pie = 3.14                                    1

 for (var i = 0; i < n; i++)                   n

     while j < var:                           n*(log2n)
                       

 sum+=1                                       n*(log2n)
                                      

    j *= 2;                                n*(log2n)            

console.log(sum)                                 1




Running Time Complexity=
1+1+1+n+3log2(n)
3+n+3log2(n)
now, Big O time complexity,
drop leading constants=>n+nlog2(n)
drop lower constants=>nlog2(n)

now, Big O time complexity of the above is hance, O(nlog(n))O(nlog(n))

~~~





​