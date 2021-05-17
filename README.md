
![image](https://user-images.githubusercontent.com/66803124/118511957-3bafa700-b6e7-11eb-94c4-ad3afd5bae47.png)

# Algorithm_Binary_Search

![image](https://user-images.githubusercontent.com/66803124/118511758-128f1680-b6e7-11eb-9cb8-fbe17e5b5b4e.png)

The best way I have seen a Binary Search Algorithm explained has been in Harvard's CS50 Computer Science course. 

https://www.youtube.com/watch?v=DSffdCT5Cx4

Here, Professor David Malan works his way through this algoritm using a phone book.

One fundemental part of Binary searches is that the list you are iterating through must have already been ordered. That is why the phone book in this example works perfectly. 

Say we are looking for some hot shot in the phone book, let's call her Kristi Gordon. 

We could flip through every single page of the phone book and eventually get to the correct entry, however this is painfully slow. That is where a binary search comes in!

Instead, since our phone book is ordered, we can open it half way and see maybe the M's or N's. We then know that we have passed Gordon so we can tear the phone book in half because we know Gordon isn't in the second half of the book. 

That means we just tore our problem in half, literally! From say 1,000 pages to 500 in this case but this number can be astronomical depending on the circumstance. 

Now, we can If we do this again to our book, we end up at a point in the H's. That just halved our problem again down to 250. We keep iterating through this loop until we have found our target. 

Ok! We've found Kristi Gordon. Looks like she's an experienced Technical Program Manager looking for employment! Let's wrap up this algorithm and give her a call. 

Lastly, this can be done with so much more than a name in a phone book, including numbers. Here is a graphical representation of the above explanation followed by an example solution. 

![image](https://user-images.githubusercontent.com/66803124/118507993-9d6e1200-b6e3-11eb-929d-d5443b7c8fe2.png)
