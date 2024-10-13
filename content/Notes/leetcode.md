---
title: ・LeetCode 75
date created: 2024-09-02
tags:
  - java
---
To anyone reading this, I'm still active on Leetcode/cf, just lazy to take notes. 

Decided to start working on LeetCode upon entering college and finding a group of people who were willing to work on a problem set with me. Prior to this, I've done ~100 problems on CodeForces, ~30 problems on LeetCode, and ~60 USACO Bronze/Silver questions. However, I started working on this in 10th grade (when I started learning how to code), and I wasn't really focused on learning the algorithms behind a question.

Tl;dr: The way I've been learning is flawed and I'm trying to change that! This will include my notes on (almost) all the questions. 

## Helpful methods 
### Array/String 
Learned about a few beneficial String methods
```java
str.trim(); // will remove any trailing/leading whitespaces from str
str.split(regex, limit); // will remove the regex string or character limit amount of times.
                         // returns an array of substrings.
                         // Limit can be left empty.

str.split("\\s+"); // can be particularly helpful when given a string with unknown whitespaces 
                   // between each 'word'.
```

## Specific algorithms
### 151 - Two Pointer
*** Reverse the order of the words
Trim and split to return an array of only words (without whitespaces).
```java
String[] st = s.trim().split("\\s+");
```
Use 2 pointer for the fastest efficency in reversing the order of the words
```java
int start = 0;
int end = st.length - 1;
while(start<end){
    String temp = st[start];
    st[start] = st[end];
    st[end] = temp;
    start++;
    end--;
}
```
Using StringBuilder to concatenate the final array into a string.
```java
StringBuilder str = new StringBuilder();
for (int i = 0; i < st.length; i++) {
  str.append(st[i]);
}
return str;
```
