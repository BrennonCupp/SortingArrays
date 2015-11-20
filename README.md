# SortingArrays

## Introduction
This is a program to sort numbers using arrays. 

## Outline
1. 	Create an array of random numbers.
2.	Sort the numbers and display them sorted. 

## Reference and Literature
* Liang, Y. (2014). *Introduction to Java programming: Comprehensive version* (Tenth ed.).
* Dr. Evert and the class work posted on git hub.
	
## Code
``` java

import java.util.*;
public class ArraySorting {
	public static void main(String[] args) {

	System.out.print("Hello class, "); 
	System.out.println("this is a sorting algorithm using arrays.");
			
	// call the sorting algorithm
	SortAlgorithm();
			}
	public static void SortAlgorithm() {

	// generate a set of random numbers to sort
	int listSize = 6;
	int[] numberArray = new int[listSize];
	numberArray = buildRandomArray(listSize);
	System.out.print("Our random array is: ( ");
	for (int i = 0; i < listSize; i++ ){
	System.out.print(numberArray[i] + " ");
			}
	System.out.println(").");
			
			
	// sort our array of numbers
	numberArray = sortOurArray(numberArray, listSize);
	System.out.print("Our sorted array is: ( ");
	for (int i = 0; i < listSize; i++ ){
	System.out.print(numberArray[i] + " ");
			}
	System.out.println(").");
			
		}
	public static int[] buildRandomArray(int listSize) {
	int[] numberArray = new int[listSize];
	// populate the array
	numberArray = populateRandomArray(numberArray, listSize);
	
	// Test the array to see if there are duplicates.
			
	return numberArray;
		}
public static int[] populateRandomArray(int[] numberArray, int listSize) {
			
	int randomRange = listSize * 1000;
	for (int i = 0; i < listSize; i++ ){
	numberArray[i] = (int)(Math.random()*randomRange);
			}
	return numberArray;
		}
		
	public static int[] sortOurArray(int[] numberArray, int listSize) {
			
	int holder_1;
	int holder_2;
	for (int passCounter = 1; passCounter <= listSize; passCounter++ ){
				
	for (int i = 0; i < listSize-1; i++ ){
					
	holder_1 = numberArray[i];
	holder_2 = numberArray[i+1];
					
	if(holder_2 < holder_1){
	numberArray[i] = holder_2;
	numberArray[i+1] = holder_1;
						
					}
					
				}
			}
	return numberArray;
		}
	}
```

## Console Output
```
1.)
	Hello class, this is a sorting algorithm using arrays.
	Our random array is: (2152 4613 3053 2234 5934 209).
	Our sorted array is: (209 2152 2234 3053 4613 5934).
2.)
	Hello class, this is a sorting algorithm using arrays.
	Our random array is: (203 3220 1922 5127 2324 699).
	Our sorted array is: (203 699 1922 2324 3220 5127).
3.)
	Hello class, this is a sorting algorithm using arrays.
	Our random array is: (5963 4791 1318 1945 5329 1910).
	Our sorted array is: (1318 1910 1945 4791 5329 5963).


```



## Summary
This assignment was helpful in teaching how arrays work and how to store information in them. We were going to learn how to use the array sort function but ran into problems with that in class. This will help lead into applying arrays into the addition game. 

