# Week 44

## Saturday. Session 1

I am learning Go again. I have some experience with it, but that was a while back. I want to refresh my knowledge of the language and its ecosystem before diving into more mature projects. I asked Claude for resources, and he recommended starting with "A Tour of Go". Since I learn better by writing code than just reading, I'm going to work through all the examples in the book, not just the exercises.

Time spent: 72 minutes
Links:
- https://github.com/stay-focused-dev/tour-of-go/tree/v2025.44.6.1


## Sunday. Session 1

Read a few chapters on slices and maps in Go.

Time spent: 62 minutes
Links:
- https://github.com/stay-focused-dev/tour-of-go/commit/80539bafb4ad98ed6aa1a41adfc55280a7982c06


# Week 45

## Monday. Session 1

Read a few chapters on methods and interfaces in Go.

Time spent: 101 minutes
Links:
- https://github.com/stay-focused-dev/tour-of-go/commit/ed8830e19ed11405d3c3aa27089ab6d55c216e6d


## Wednesday. Session 1

Read a few chapters on interfaces and generics in Go.

Time spent: 72 minutes
Links:
- https://github.com/stay-focused-dev/tour-of-go/commit/501402823301549e151b1c74c6e5f10628531528


## Wednesday. Session 2

Read a few chapters on channels in Go.

Time spent: 43 minutes
Links:
- https://github.com/stay-focused-dev/tour-of-go/commit/28b4aefb5550289f94a8f1337962dd8be10b9d02


## Friday. Session 1

I've just finished 'A Tour of Go', so now I'll read through the articles it recommended.

Time spent: 27 minutes
Links:
- https://github.com/stay-focused-dev/tour-of-go/commit/31a44b69c404ac26f8652312beac8b0ae8c14d57


## Friday. Session 2

I read the article "How to Write Go Code", which was recommended in "A Tour of Go" for learning how to organize and work with code.

Time spent: 31 minutes
Links:
- https://go.dev/doc/code
- https://github.com/stay-focused-dev/go-hello


## Friday. Session 3

I watched Rob Pike's video "Go Concurrency Patterns" that was recommended in "A Tour of Go". It reminded me of a saying about Erlang and its capabilities - something like 'we can make hard things easy and impossible things possible'.

Time spent: 84 minutes
Links:
- https://www.youtube.com/watch?v=f6kdp27TYZs
- https://github.com/stay-focused-dev/go-concurrency-patterns/tree/v1


# Week 46

## Wednesday. Session 1

I watched Sameer Ajmani's video from Google I/O 2013 "Advanced Go Concurrency Patterns". He built a simple RSS client and showed how to avoid some bugs in a naive implementation. He emphasized:

- possible data races from concurrent mutation of shared state
- unresponsive behaviour when doing I/O or sleeping before the next event
- possible deadlocks when a channel is closed and a goroutine tries to send to it

I was fascinated by these examples especially by "chan chan error" and how we can make our code simpler (without nested cases) using select and message passing. 

It was a 34-minute video, but I had to spend a lot of effort to grasp these ideas. I watched the video for the first time, then implemented the functionality, understood some details, and then watched the video again. Now I feel like I understand it.

Time spent: 215 minutes
Links:
- https://www.youtube.com/watch?v=QDDwwePbDtw
- https://github.com/stay-focused-dev/go-concurrency-patterns/commit/a8c8affff253acf1a75e1691834df1116a4e35dc


## Friday. Session 1


I decided to dive into one of the popular Go projects on GitHub and found Traefik interesting. The project provides a getting-started page where two services run using Docker Compose:

- Traefik
- whoami (a simple HTTP server)

Traefik automatically discovers the whoami service and configures it so I can curl some of the whoami endpoints.

Then I thought: building a webserver is a typical programming task—it would be nice to collect tasks like this in my own library. When I learn a new language, I can use these exercises to learn the basics of the language and its ecosystem. So I created a repo for such exercises and added a whoami-like service exercise to it.

Time spent: 91 minutes
Links:
- https://github.com/traefik/whoami
- https://github.com/stay-focused-dev/exercise-library/commit/91bd285d6fab4d6d5002feac9fbb0e391fcc4a31



## Saturday. Session 1

I tried LeetCode for the first time. I watched some beginner videos that introduce the UI, then solved one of the problems (very easy, to be honest). It was an interesting experience - the task was very easy, but I felt like a super guru! I like this feeling of a small victory.
 
Time spent: 81 minutes
Links:
- https://leetcode.com/problems/two-sum/description/
- https://github.com/stay-focused-dev/leetcode/commit/705c21790a0ce66cb4e4958d4ae7d66274222722


## Saturday. Session 2

I solved the LeetCode problem 'Add Two Numbers' (you're given two linked lists representing numbers, and you need to sum them and return the result as a linked list). I'm not yet in the habit of writing tests in Go, working with pointer-based structures like linked lists, or writing methods like `String()` for custom types. It takes some extra time right now. I believe that later these techniques will be at my fingertips and won't take nearly as much time.

Time spent: 55 minutes
Links:
- https://leetcode.com/problems/add-two-numbers/
- https://github.com/stay-focused-dev/leetcode/commit/7df26e1bd3a990c7c25fd64ad41adc9f1e834051


# Week 47

## Wednesday. Session 1

I have a pet project written in Rust that helps me with EVE Online. It lets me check my assets, especially mutated items—the game doesn't have a proper interface for finding mutated items with specific stats. I've written a lot of code for this project but only just pushed it to GitHub today. While this project might seem like a small toy, it actually has a surprisingly robust feature set typical of production applications, including:

- Saga-based background jobs
- request tracing
- structured logging
- comprehensive error handling
- real-time frontend communication via WebSockets
- and more

Time spent: 125 minutes
Links:
- https://github.com/stay-focused-dev/rust-eve-tools/commit/33b17835560d9093ffb266eb76bf49a7bff3e9e0


## Saturday. Session 1

I tackled one of the hard LeetCode problems using Rust—one that requires binary search. The solution concept was straightforward, but the implementation took considerable time. I had to work through all the edge cases on paper, which frustrated me. Why should such a simple idea take so long? I asked Claude about this, and Claude reassured me that it's perfectly normal when you're encountering a pattern for the first time without having internalized it yet. With practice, I'll recognize the pattern instantly and implement solutions quickly. I believe this, because when I was at school, I practiced math extensively and excelled in competitions. It's all about patterns and pattern recognition. I solved the problem independently, then compared my solution to the standard approach (which was more elegant and concise). Now I've planted the seed for the 'binary search' pattern in my mind.

Time spent: 222 minutes
Links:
- https://leetcode.com/problems/median-of-two-sorted-arrays/
- https://github.com/stay-focused-dev/leetcode/commit/1f504f9356a21d0d13b5db87c25ee5269270957e
- https://github.com/stay-focused-dev/leetcode/commit/6c1c6cf37159a52471882f11d6c200e001c53556
