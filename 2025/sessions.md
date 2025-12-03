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


# Week 48

## Monday. Session 1

I solved a medium LeetCode problem. It was straightforward once I understood the approach.

Time spent: 50 minutes
Links:

- https://leetcode.com/problems/longest-substring-without-repeating-characters/description/
- https://github.com/stay-focused-dev/leetcode/commit/71f721632f4618a1a55e35fa4bbea9854afb5bdd


## Wednesday. Session 1

I solved a medium LeetCode problem about finding the longest palindromic substring. The problem didn't seem interesting, so I didn't put much effort into it—I just wanted a working solution.

Time spent: 31 minutes
Links:

- https://leetcode.com/problems/longest-palindromic-substring/
- https://github.com/stay-focused-dev/leetcode/commit/7c1d60ab643a2ee6ac0a695e5c55516e44c1a1e5

## Wednesday. Session 2

Then I asked Claude about the optimal solution. It told me about a more effective approach than mine, which I implemented right away. I was blown away when it mentioned a solution with linear complexity—I'll implement that once I fully understand the idea!

Time spent: 42 minutes
Links:

- https://leetcode.com/problems/longest-palindromic-substring/
- https://github.com/stay-focused-dev/leetcode/commit/a67105c989937f1a2f5f5b1cc583d70e71b586b6


## Friday. Session 1

I learned Manacher's algorithm in detail and implemented it. It turned out to be surprisingly simple to code once I understood the idea. The algorithm is very elegant.

Time spent: 59 minutes
Links:

- https://leetcode.com/problems/longest-palindromic-substring/
- https://github.com/stay-focused-dev/leetcode/commit/2c16493bae45bd8164ad0fb5b30efae38a1d2e70

## Saturday. Session 1

I solved the zigzag conversion problem from LeetCode. The problem itself was easy—you just need to work out the indices on paper. Ironically, this was my first LeetCode problem  where I didn't pass all tests initially. I've noticed that when problems seem obviously simple, I don't scrutinize edge cases carefully enough. That's definitely a lesson I need to internalize.

Time spent: 43 minutes
Links:

- https://leetcode.com/problems/zigzag-conversion/
- https://github.com/stay-focused-dev/leetcode/commit/52b47f052c9954356e1cb1d46f0130d61b70b8ea

## Saturday. Session 2

I solved the reverse integer problem from LeetCode.

Time spent: 
Links:

- https://leetcode.com/problems/reverse-integer/
- https://github.com/stay-focused-dev/leetcode/commit/aa1e816d8b922ffc8db37cb4c72917d6829576e9
- https://github.com/stay-focused-dev/leetcode/commit/7c345d37d50d7a738b7b2aacb88dbe0a3dfbca52


# Week 49

## Monday. Session 1

I solved the LeetCode problem 'Merge k Sorted Lists'. One of the obvious approaches to me was the min-heap one—I implemented it. I was pleasantly surprised that Go's standard library includes heap support.

Time spent: 70 minutes
Links:

- https://leetcode.com/problems/merge-k-sorted-lists/
- https://github.com/stay-focused-dev/leetcode/commit/3a89cd07eb138ede541992c4bf09c263ee078349
- https://github.com/stay-focused-dev/leetcode/commit/917f6b967e6a4c1f6c6290f9bc56f9dbbef4a708


## Monday. Session 2

Then I asked Claude about other approaches—it told me that a divide-and-conquer approach could solve the problem with O(1) extra space instead of O(k) for min-heap approach, and with the same time complexity O(n * log k). I was fascinated by this—I implemented the suggested approach immediately. Now that I understand the pattern, I'll be able to implement it independently next time.

Time spent: 23 minutes
Links:

- https://leetcode.com/problems/merge-k-sorted-lists/
- https://github.com/stay-focused-dev/leetcode/commit/33e8a097890537b25d82f9552218d26ba1ef0350


## Tuesday. Session 1

I solved the LeetCode problem '3Sum'. It was an easy problem—I completed it in 51 minutes, spending 20 of those minutes on writing tests. After a successful submission, I asked Claude to review my code. It made several recommendations, and I implemented some immediately.

Time spent: 51 minutes
Links:

- https://leetcode.com/problems/3sum/description/
- https://github.com/stay-focused-dev/leetcode/commit/df3c1b4abfab03503df70a6b9ff73f7cabdd68a1
- https://github.com/stay-focused-dev/leetcode/commit/12cda9d6d7d687eb19befeda38163af11d88fc51


## Tuesday. Session 2

Then I asked about alternative approaches. Claude described the two-pointer method, which I implemented. Looking back, I'm curious why this approach didn't occur to me initially.

Time spent: 5 minutes
Links:

- https://leetcode.com/problems/3sum/description/
- https://github.com/stay-focused-dev/leetcode/commit/44a6ddde2705952ea4f81fb8188641c3a9768922


## Wednesday. Session 1

My lovely wife asked me to help her. She has some records about future events in Google Sheets and she wants to transform them into reminders in Telegram or Mattermost with appropriate messages addressed to specified people. I thought it was a good idea for a small pet project. 

I wanted notifications about changes to the target documents. Google Drive API allows this functionality but requires a callback URL—I set up a VPS immediately, configured a subdomain with HTTPS support, verified the subdomain in Google Cloud Console, and created a service account in the Google Cloud Console. I don't like this admin stuff, but I have some helpers to set up a new VPS using Ansible.

Time spent: 66 minutes
Links:

- https://github.com/stay-focused-dev/ansible-vps-setup


## Wednesday. Session 2

I needed to get acquainted with the API—so I asked Claude to write an example that would show me how to fetch data from a Google Sheet. I implemented a working program using this example.

Time spent: 20 minutes
Links:

- https://github.com/stay-focused-dev/go-gsheet-to-telegram/commit/ca292e2217a818b5d1564c13c453eaf756b2b544


## Wednesday. Session 3

Then I did the same thing to get acquainted with Google Drive API to get notifications about document changes.

Time spent: 78 minutes
Links:

- https://github.com/stay-focused-dev/go-gsheet-to-telegram/commit/feec74c26700d8405499a8c2e1e02a73b4aa9f19


## Wednesday. Session 4

I realized that I needed to refactor the code I'd written to reuse some shared variables (like callback url, sheet id) instead of hardcoding them. I did it immediately.

Time spent: 5 minutes
Links: 

- https://github.com/stay-focused-dev/go-gsheet-to-telegram/commit/560f5215846139ab0861521074959a393edb1b54