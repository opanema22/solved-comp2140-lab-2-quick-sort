Download Link: https://assignmentchef.com/product/solved-comp2140-lab-2-quick-sort
<br>



<strong>Objective:</strong>

to successfully sort all the numbers in an array, using your partition function.

<ol>

 <li>Your partition function should return the correct pivot index of the subarray.</li>

 <li>You must use a dynamically-allocated array for this lab; no other data structures may be used.</li>

 <li>The following summarizes the commands used in the Quicksort lab: (OK means no error was raised.)</li>

</ol>

<table width="671">

 <tbody>

  <tr>

   <td colspan="6" width="671"><strong>Function                                           DESCRIPTION                                       OUTPUT </strong></td>

   <td width="0"> </td>

  </tr>

  <tr>

   <td colspan="2" width="234"><strong>QuickSort constructor </strong></td>

   <td colspan="2" width="266">Create a quickSort array of size <em>capacity</em>. Set initial number of elements (Size) to 0.</td>

   <td colspan="2" width="171">OK orError</td>

   <td width="0"> </td>

  </tr>

  <tr>

   <td colspan="2" width="234"><strong>addToArray <em>&lt;int&gt;</em>  </strong></td>

   <td colspan="2" width="266">Add data (an integer value) to quickSort array. Duplicates are allowed.</td>

   <td colspan="2" width="171">OK orError</td>

   <td width="0"> </td>

  </tr>

  <tr>

   <td colspan="2" width="234"><strong>capacity </strong></td>

   <td colspan="2" width="266">Return the capacity of the quickSort array.</td>

   <td colspan="2" width="171">size</td>

   <td width="0"> </td>

  </tr>

  <tr>

   <td colspan="2" width="234"><strong>clear </strong></td>

   <td colspan="2" width="266">Delete all inserted nodes from theQuickSort array. (Do not delete QuickSort array – capacity stays the same.)</td>

   <td colspan="2" width="171">OK or</td>

   <td width="0"> </td>

  </tr>

  <tr>

   <td colspan="2" width="234"><strong>size </strong></td>

   <td colspan="2" width="266">Return the number of elements currently in the array.</td>

   <td colspan="2" width="171">An integer value</td>

   <td width="0"> </td>

  </tr>

  <tr>

   <td colspan="2" width="234"><strong>private quickSort <em>&lt;start&gt;</em> <em>&lt;end&gt;</em> </strong></td>

   <td colspan="2" width="266">quickSort the elements in the quickSort array from index <em>&lt;start&gt;</em> to index <em>&lt;end&gt;</em> (where <em>&lt;end&gt;</em> is one past last element) using median and partition functions.</td>

   <td colspan="2" width="171">OK orError</td>

   <td width="0"> </td>

  </tr>

  <tr>

   <td colspan="2" width="234"><strong>public quickSort </strong></td>

   <td colspan="2" width="266">quickSort all the elements in the quickSort array using median and partition functions.</td>

   <td colspan="2" width="171">OK or  Error</td>

   <td width="0"> </td>

  </tr>

  <tr>

   <td colspan="2" width="234"><strong>medianOfThree <em>&lt;start&gt;</em> <em>&lt;end&gt;</em> </strong></td>

   <td colspan="2" width="266">1) Calculate the middle index (middle = (start + end)/2), then 2) bubble-sort the values at the start, middle, and end indices. (<em>&lt;right&gt;</em> is one past last element.)</td>

   <td colspan="2" width="171">Index of the pivot(middle index); -1 if provided with invalid input</td>

   <td width="0"> </td>

  </tr>

  <tr>

   <td colspan="2" width="234"><strong>partition <em>&lt;start&gt;</em> <em>&lt;end&gt;</em> <em>&lt;pivot&gt;</em> </strong></td>

   <td colspan="2" width="266">Partition the quickSort array(<em>&lt;start&gt;</em>, <em>&lt;end&gt;</em> and <em>&lt;pivot&gt;</em> indexes) around the pivot value. Values smaller than or equal to the pivot should be placed to the start of the pivot while values larger than the pivot should be</td>

   <td colspan="2" width="171">Pivot’s ending index, -1 if provided with invalid input</td>

   <td width="0"> </td>

  </tr>

  <tr>

   <td width="0"> </td>

   <td colspan="2" width="234"> </td>

   <td colspan="2" width="266">placed to the right of the pivot. (<em>&lt;end&gt;</em> is one past last element.)</td>

   <td colspan="2" width="171"> </td>

  </tr>

  <tr>

   <td width="0"> </td>

   <td colspan="2" width="234"><strong>printArray </strong></td>

   <td colspan="2" width="266">Print the contents of the quickSort array as comma separated values (using a toString() function.)</td>

   <td colspan="2" width="171">Array values orEmpty</td>

  </tr>

  <tr>

   <td width="0"></td>

   <td width="233"></td>

   <td width="0"></td>

   <td width="266"></td>

   <td width="0"></td>

   <td width="171"></td>

   <td width="0"></td>

  </tr>

 </tbody>

</table>

Steps:

<ul>

 <li><strong>Step 1</strong> – Begin with a main function.

  <ol>

   <li>You will need to write your own main function.</li>

   <li>Use command line arguments for input and output files.</li>

  </ol></li>

 <li><strong>Step 2</strong> – Add your QuickSort class.

  <ol>

   <li>Your QuickSort class should contain a dynamically-allocated templated array. Before you focus too much on the actual sorting algorithm, make sure the logistics of the class work correctly. Focus on <em>addToArray(), clear(), getSize(), </em>and <em>toString()</em> member functions.</li>

   <li>The QuickSort class should ask the user to input an integer array size called <em>capacity</em> and create an array accordingly, by randomly generating <em>capacity (for example 100)</em> integers (you can use any random number generator). These created integers should be added to the array by the addToArray() function.</li>

  </ol></li>

 <li><strong>Step 3</strong> – Write your <em>medianOfThree()</em> function in the QuickSort class.

  <ol start="2">

   <li>The Median-of-Three function takes start and right indexes as parameters and then calculates the index in the middle of the indexes (rounding down if necessary). Note that these are being done on the array populated in Step2.b.</li>

   <li>Sort the left, middle, and right numbers from smallest to largest in the array.</li>

   <li>Finally, return the index of the middle value. This will be your pivot value in the sortAll() function.</li>

  </ol></li>

 <li><strong>Step 4</strong> – Write your <em>partition()</em> function in the QuickSort class.

  <ol>

   <li>The partition() function should begin by swapping the leftmost element of the array with the pivot index element.</li>

   <li>Now, follow partition the array such that all elements less than or equal to the pivot value are left of the pivot and all elements great than the pivot value are to the right of the pivot.</li>

   <li>The partition() function should return the location of the pivot index.</li>

  </ol></li>

 <li><strong>Step 5</strong> – Write the private quickSort<em>()</em> function, using your <em>medianOfThree()</em> and <em>partition()</em>

  <ol>

   <li>Note that this function will be recursive. Most people use public <em>quicksort()</em> as a starter function that then call another private quicksort function to do the sorting.</li>

   <li>To sort, first call your <em>medianOfThree()</em> function to sort the first, middle, and last elements and return the pivot index.</li>

   <li>Now, call your <em>partition()</em> function, using the index returned from <em>medianOfThree()</em> as the pivot index. This function will return a new pivot index where your array is split.</li>

   <li>Finally, recursively call your <em>sort()</em> function on the two halves of your array, with one half from the left to the pivot and the other half from the pivot to the right.</li>

   <li>Print the sorted array.</li>

  </ol></li>

</ul>





