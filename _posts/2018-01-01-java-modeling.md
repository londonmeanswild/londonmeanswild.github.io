---
layout: default
title:  "Modeling in Java and Python"
categories: research
---

Developed and implemented Java classes to model and analyze questions of time, scheduling, and organization. 

Compared banks teller lines efficiency against grocery store queues using Singly Linked Lists and simulated time-steps
Used a lexicon trie to simulate T-9 word texting.
Designed a final exam schedule using greedy algorithms, binary search trees, and graphs represented through adjacency lists.

Solved word subset and the Two Towers puzzles using vectors and iterators, comparing anticipated and actual big-O run times.

Java and Data Structures repository can be [found here](https://github.com/londonmeanswild/java)

Used Python to parse text, data, and represent population changes. 

Python and Data Structures projects can be found in [this repository](https://github.com/londonmeanswild/python_134_classwork). 


Below is a code excerpt from [scheduler.java](https://github.com/londonmeanswild/java/blob/master/Exam%20Scheduling%20(graphs)/Scheduler.java), which schedules a final exam based on student schedules and pre-determined rules. Output is a graph. 

```
  public Scheduler(Vector<Student> students){
        this.courses = new OrderedVector<String>();
        this.students = students;
        graph = new GraphListUndirected<String, Integer>();
        // divide student object into course names and name of student
        for (Student s : students){
            for(String course : s.getCourses()){
                if (!graph.contains(course)){
        // add courses to a vector
            courses.add(course);
                    graph.add(course);
                }

            }

        }

```

Below is a code excerpt from [oracle.py](https://github.com/londonmeanswild/python_classwork/blob/master/oracle.py), which takes a text file and uses a "window" to read and re-write text.

```

        for i in range(len(string) - self._window + 1):
            substring = string[i:i + self._window].lower()  # i is set to 0. sets to lower.
            front = substring[:-1]  # first half of the substring
            back = substring[-1]  # second half of the substring
            if front not in self._distribution:
                self._distribution[front] = dict() #  adding to dictionary
            if back not in self._distribution[front]:
                self._distribution[front][back] = 1  # initialize counter
            else:
                self._distribution[front][back] += 1  # if already in dict(), increment


    def follows(self, string):
        """ Returns random character likely to follow 'string' based on window_size.
        All strings are passed throughlower(), in case input text has uppercase.
            Args:
                string: character sequence of at least window_length - 1
            Returns:
                a character picked by random from the dictionary or None if no matching characters
                found
            """

        assert(len(string) >= self._window - 1), "Must be greater than window_size minus one"

```
