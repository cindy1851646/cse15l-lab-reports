# Lab Report 5

All tests were found through diff of running the bash on two files.

## Test One
The file used: 201.md
</br></br>

Our current inplementation is incorrect and it produced the output ``` [] ```. 
</br></br>

The provided implementation is correct and produces the output ```
[baz]```.
</br></br>

The part of code that needed to be fixed: 
```
if (nextOpenBracket > 0 && 
        markdown.charAt(nextOpenBracket - 1) == '!' ||
        markdown.charAt(openParen - 1) != ']' || 
        newline2 < closeParen && newline2 > openParen) {
    currentIndex = closeParen + 1;
    continue;
}
```

The problem in our code is that things in bwtween closed bracket and open parentheses was being ignored in some parts so we couldn't get the expect output. 


## Test two
The file used: 41.md
</br></br>
Our current inplementation is incorrect and the output is ```
[url &quot;tit&quot;]``` 
</br></br>

The provided implementation is incorrect and the output is ``` [] ``` 
</br></br>

The part of code that needed to be fixed: 
```
toReturn.add(markdown.substring(openParen + 1, closeParen));
```


The problem in our code is that we returns all the things in between the parentheses and in some cases when there are other things within the link it also returns it. Therefore it has bug that needed to be fixed. 
</br></br>



