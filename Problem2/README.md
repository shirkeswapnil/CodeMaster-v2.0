# Movie Theater 

Animation movies are always treat not only for kids but for adult. People who have seen the movie once want to see again and again.

In nearby theater, they were showing a wonderful short animation film. There was a queue outside the theater.
Some people were alone, and some are with the family. And of course, people who are with family want to go inside the theater together.
As it was a short movie, the cost was just 10 rupees per person. We need to find how much money the theater will make on a given day.

The theater has a capacity of say **P** people.
The family enters in theater one at a time, until there is no more family left in the queue or there is no room for next family. Then the movie starts, whether theater is full or not.
Once the movie is over, since the movie is so great all families re-queue in the same order. The theater runs **S** shows per day.

Let me simplify, say S=3, P=5, and there are four families with size: 3, 4, 1, 2 in the queue. For the 1st show, only one family enters, i.e. [3] keeping 2 seats empty (as 2nd family won't fit, and as we know family wants to go together).
After the 1st show is over 1st family goes back and re-queue, so the queue will be 4, 1, 2, 3. For the 2nd show, as capacity is 5 people, two families can go ahead : [4, 1].
When 2nd show over and families re-queue again, the queue now looks like 2, 3, 4, 1. The 3rd show which last (as **S** is 3) show for this theater, [2, 3] can go inside.

At the end of a day, for this case theater makes a total of 130 rupees!

## Input

The first line of the input gives the number of Theaters around, **T**. **T** Theaters follow

Each Theater will have two lines on input.
The first line consists three numbers separated by space: **S**, **P** and **FC**. **FC** is families in queue.
The second line consists FC space-separated integers say **Fi**, each number represent size of each family, so F0 will be size of 1st family, F1 will be size of 2nd family and so on.

## Output
For each theater, output should be like "**Theater-TN: R**", where TN is the Theater number (starting from 1) and **R** is the total Rupees made by that theater.

### Sample Input
```
3
5 5 10
2 4 2 3 4 2 1 2 1 3
1 10 9
1 1 1 1 1 1 1 1 1
100 10 1
1
```

### Sample Output

```
Theater-1: 200
Theater-2: 90
Theater-3: 1000
```