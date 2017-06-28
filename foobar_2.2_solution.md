package com.google.challenges; 

public class Answer {   
    public static int answer(int n) { 
        
        return findFibbonacci(n) - findMinimum(n);
    }

     static int findMinimum(int n) {
         
        int fr = 0;
        int sum = 0;
        int count = 0;
        
        while (sum + fr * 2 <= n) {
            if (fr == 0){
                fr = 1;
            } else fib = fib * 2;
            
            sum += fib;
            count++;
        }
        
        if (n - sum >= fr + fr / 2 ) {
            return count +1;
        } else return count;
    }

    private static int findFibbonacci(int n){

        int first = 0;
        int sec = 1;
        int sum = 0;
        int count = 0;

        while (sum + first + sec <= n) {
            first = first + sec;
            sec = first - sec;
            sum += first;
            count ++;
        }

        return count;
    }
    
}