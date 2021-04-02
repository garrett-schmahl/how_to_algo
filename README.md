"# how_to_algo" 
// How to Algorithm

For many of us solving problems is almost intuitive. You look at a problem and know the steps to work out the answer. That's great, but only works if your mind already knows how to do the thing. If you look at problem and your mind goes "ohgodohfu wadu-i-doooo"; First, don't panic. Then try this:

Step 1: Know it.
Step 2: Plan it.
Step 3: Build it.
Step 4: Test it.
Step 5: Break it.

...daft punk can sue me, it's easy to remember.


For this document I will be using this example question:
Create a function that takes the smallest value of an array and moves it to the front of an array. Do not use any inbuilt functions. If there are multiple instances of the smallest number, the first should be taken.



Step 1: Know it.
The most successful guy I know has a mantra, "Know what you're making." It is excellent advice for anyone building anything. Split it into two parts. What do you have, and what do you need?

This seems obvious, but often times I got caught doing things without really understanding where I was going. It really does help to firmly write out what you have and where you are going.

Example
I have an array and a function that I need to work within. I am not allowed to use any inbuilt functions other than .pop(). I know previously we did a problem similar to this where we needed to shift an array, I can probably reference the code from that.

I need to return the given array with the smallest thing moved to the front. In order to do that I need a tool to sort through the array to find the smallest, and a tool to manipulate the array.


const nums1 = [6, 4, 5, 1, 3, 2];
const expected1 = [1, 6, 4, 5, 3, 2];

const nums2 = [1, 5, 2, 9];
const expected2 = [1, 5, 2, 9];

const nums3 = [5, 1, 0, 2, 3, 0];
const expected3 = [0, 5, 1, 2, 3, 0];

function minToFront(nums) { 
  return num
}


Step 2: Plan it
Seperate the problem out into its parts. If you don't know what parts you need, try using steps 1 and 2 on each part, working back from the return, or forward from the top, whichever seems easier. If you're stuck, try and take your data and turn it into something closer to what you want. You can and should run all 5 steps on each part if the problem is complex enough. 

This step is also sometimes referred to as "pseudo-code". I like to write in the loops with a description, usually people do it as all text. However works for you is great.

It also may be good idea to build a library of parts. Just a bunch of different functions and parts of functions, made by you or seen by you, that do interesting things. This is likely how the first programming libraries got started. It also helps you to remember things that you've seen before.

Performed on the example problem...
I think I will need four parts. Find the smallest index, store the value saved at the smallest index, shift the array to open up a spot at the front while overwriting my index, and overwrite the first value with the value from the smallest index. 

First I need to find the smallest thing. That means looking through the array (for loop) and comparing values (if statement), and save the index number (var).

function minToFront(nums){
  var smallestIndex  //create variable to store index of smallest number
  for() {
    if() {           //find index of smallest number

return num

Second, I need to store the value from that index because I'm going to overwrite the array. That's just saving a new variable.

function minToFront(nums){
  var smallestIndex   //create variable to store index of smallest number
  for() {
    if() {            //find index of smallest number

  var smallestNumber  //store value at index of smallest number
  return num

Third, I need to shift the array. That's a for loop. I can use that index number I got earlier to tell it where to start shifting.

function minToFront(nums){
  var smallestIndex     //create variable to store index of smallest number
  for() {
    if() {              //find index of smallest number

  var smallestNumber    //store value at index of smallest number

  for() {               //shift array
  return num

Fourth, I need to overwrite the first value of the array with the value I got at the second step.

function minToFront(nums){
  var smallestIndex       //create variable to store index of smallest number
  for() {
    if() {                //find index of smallest number

  var smallestNumber      //store value at index of smallest number

  for() {                 //shift array
  arr[0] = smallestNumber //overwrite first value with smallest number
  return num

okay, now I have a plan that I think will get me where I need to go.

3. Build it.
Usually people sorta just jump to this step. You can definitely do that if you intuitively understand what needs to happen. However, if you find out you actually don't, start from the beginning. It doesn't take long, you'll lose more time fumbling than you will if you run through the steps.

function minToFront(nums) {
  var smallestIndex = 0
  for(var i = 0; i < nums.length;i++){
    if(nums[i] < nums[smallestIndex]){
      smallestIndex = i
    }
  }
  var smallestNumber = nums[smallestIndex]
  for(var j=smallestIndex; j > 0 ;j--){
    nums[j]= nums[j-1]
  }
  nums[0] = smallestNumber
  return nums
}

4. Test it.
I filled in the above with the correct answer, but my group did not get it on the first go. We had to iterate. First look for easy things: Typos, bad variable callouts, bad math, misspelling, missing brackets, etc. 

Second, go through each part and make sure it actually works. Start putting console.logs everywhere. See what each variable is during each step. Find out where the problem actually is. Make sure each of your parts actually works.

For example, if you have a console.log(smallestIndex) inside the "if" statement, if it never returns anything you know the if statement is never firing. If it returns a number you aren't expecting, it means your logic has an error in it somewhere.

This step gets easier with experience. To know what's wrong, first we have to know what's right. Eventually we'll be able to look at code and instantly spot things out of place, but for now we struggle T.T

You may find that the problem wasn't what you thought it was. Go back to the start and try again from the top. With new knowledge from attempting the problem once you may be able to re-contextualize what you have and what you need in a better way. Depending on how complex the problem is this may need to be done several times.

You may realize you need to change your resources. The tools you have are not sufficient to the task. That could mean research, getting help, or rethinking through what you have. The most important thing is not to panic, get frustrated, or give up.


5. Break it.
This step is important, but far too often overlooked. Find parameters that can break your solution. Throw everything you can at your algorithms. Don't hope that your code will work. Know that your code will work. 

A huge problem in the world at large is half-assery. Don't contribute to the plague of sloppily made crap that doesn't work. Make it good, make it to last. Don't leave things at "good enough". A small amount of polish is often what sets apart the great from the average.