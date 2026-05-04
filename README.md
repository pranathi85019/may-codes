Given an array of integers of size N, rearrange the elements into a wave-like array.

An array is said to be in wave form if:

a1 ≥ a2 ≤ a3 ≥ a4 ≤ a5 ...

If multiple answers are possible, return the lexicographically smallest wave array.

Input Format

First line contains an integer N — size of the array Second line contains N space-separated integers

Constraints

1 ≤ N ≤ 10⁵ -10⁹ ≤ array[i] ≤ 10⁹

Output Format

Print the array in wave form

Sample Input 0

4
1 2 3 4
Sample Output 0

2 1 4 3
Sample Input 1

6
1 1 2 2 3 3
Sample Output 1

1 1 2 2 3 3
PROGRAM:

import java.util.*;
class Solution {
public static void main(String[] args){
    Scanner in=new Scanner(System.in);
    int n=in.nextInt();
    int[] a=new int[n];
    for(int i=0;i<n;i++){
    a[i]=in.nextInt();}
        Arrays.sort(a);
    for(int i=0;i<n-1;i+=2){
        int temp=a[i];
        a[i]=a[i+1];
        a[i+1]=temp;
    }
        for(int i=0;i<n;i++){
            System.out.print(a[i]+" ");
        }}}
