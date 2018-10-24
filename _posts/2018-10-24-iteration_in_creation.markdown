---
layout: post
title:      "Iteration in Creation"
date:       2018-10-24 12:54:40 -0400
permalink:  iteration_in_creation
---


Iteration is an interesting and time-saving concept in Ruby. The definition of iterate, according to the Merriam-Webster dictionary, is to say or do again or again and again. If we have a collection of data in the format of an array (or hash) and we need to perform a specific, repetitive operation on each item within that array (or hash), we can use iteration to accomplish the task. 

There are several methods called iterators that can be performed on arrays or hashes and will yield different types of results (feel free to Google them for more information). Iterators do not need counter variables and manual incrementation because they have the ability to keep track of this information. In this post, I will demonstrate the use of the **.each** iterator to create a phrase using strings from an array.

When I first encountered the concept of iteration, it brought to mind the account of creation from the book of Genesis. I could imagine God sitting in front of a dark, empty terminal screen coding creation; from nothing to something. Listed below, I have an array of a few items from the account of creation:

```
creation = ["day", "night", “sky”, ”land", “sea”
```

If I want to easily create a phrase about each item in this array, here is the code I will use:

```
creation.each do |item|
  puts “Let there be #{item} And the #{item} was good.”
end
```


Here, I have applied the .each iterator to my creation array. I opened the block of code with the do keyword and closed the block of code with the end keyword. 

I declared a local variable “item” and enclosed it inside of a set of pipes. The variable name in the pipes is arbitrary. Any name would be just fine.

The .each iterator will cause every single item in the collection to be set equal to the variable in the pipes and passed into the block of code. A block is a chunk of code between braces { }. Each time the block of code is run is considered an iteration. 

Here are the results of running this operation.

```
Let there be day. And the day was good.
Let there be night. And the night was good.
Let there be sky. And the sky was good.
Let there be land. And the land was good.
Let there be sea. And the sea was good.
=> ["day", "night", "sky", "land", "sea"]
```

As you see, a separate phrase was created for each item in the array. Keep in mind that the actual return value of the .each iterator will always be the original collection of items that it was called upon.

```
=> ["day", "night", "sky", "land", "sea"]
```

Since our block of code is short, we can also write it this way and leave out the “do/end” keywords:

```
creation.each {|item| puts "Let there be #{item}. And the #{item} was good.”}
```

We will receive the exact same results. 

```
Let there be day. And the day was good.
Let there be night. And the night was good.
Let there be sky. And the sky was good.
Let there be land. And the land was good.
Let there be sea. And the sea was good.
=> ["day", "night", "sky", "land", "sea"]
```

Hopefully, you will find iteration helpful along your coding journey. 

