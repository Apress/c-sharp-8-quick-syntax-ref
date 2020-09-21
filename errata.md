# Errata for *C# 8 Quick Syntax Reference*

On **page 44** [technical accuracy]:
 
Pass by Reference For reference data types, C# uses true pass by reference. This means that when a reference type is passed, it is not only possible to change its state but also to replace the entire object and have the change propagate back to the original object.
Chapter 9 Methods

void Set(int[] i) { i = new int[] { 10 }; } static void Main() { MyApp m = new MyApp(); int[] y = { 0 }; // reference type m.Set(y); // pass object reference System.Console.Write(y[0]); // 10 }

This paragraph is wrong, C# does not pass reference types by reference but by value. Without using the ref keyword, a method cannot pass a reference type instance by reference. As a result, the code sample displays 0, not 10.


***

On **page xx** [Summary of error]:
 
Details of error here. Highlight key pieces in **bold**.

***
