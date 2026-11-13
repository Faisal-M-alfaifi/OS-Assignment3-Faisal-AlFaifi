# 📝 MY_WORK: Student Information, Development Log, Reflection & Answers

> This is the **only file** your instructor reads to grade Parts 3 and 4 (documentation and video). Everything you write here must be **in your own words**.

---

## 🛑 STOP: Read This Before You Do Anything Else

> ### 1️⃣ Read the whole `README.md` first
> The `README.md` in this repository contains the full instructions: how this assignment continues Assignment 1, the Chapter 5 recap, class descriptions, feature specifications, question prompts and the video script. **If you skip it, you will lose marks.**
>
> ### 2️⃣ Understand the full code before answering any question
> Open `SchedulerSimulationSync.java` and read it **from top to bottom**. You must be able to explain what `SharedStats`, `ReadyQueue`, `CpuWorker`, `RaceWindow.pause()`, `ReentrantLock` and `Semaphore` do **before** you write a single answer in Parts B and C. **Run the original starter first** (it is intentionally broken) and **save its output**: you need it for Question 1 of Part C.
>
> ### 3️⃣ Use only the code of this repository
> Work **only** on `SchedulerSimulationSync.java` from this repository. Do **not** copy or paste code from your previous assignments.
>
> ### 4️⃣ Commit many times, not once
> A single commit, or all commits made in the last hour, costs you **-0.5 mark**. See the [Commit Rules](#-commit-rules-mandatory) below.

**How to use this file:**
1. Fill in your **Student Information** (below) right now.
2. Follow the steps in the **Work Roadmap** in order.
3. Update the **Development Log** *every time* you work on the assignment, not at the end.
4. Do not delete any section header. Replace the `[...]` placeholders with your own text.

---

## 👤 Student Information

> ⚠️ **WARNING:** Fill this in first. Your name and ID must match the student ID you set in `SchedulerSimulationSync.java` (line 304) and the one you say in your video.

| Field | Your Answer |
|-------|-------------|
| **Full Name** | Faisal Mohammed Al-Faifi |
| **Student ID** | 445050079 |
| **University Email** | 445050079@std.psau.edu.sa |
| **GitHub Username** | Faisal-M-alfaifi |
| **Repository Link** | https://github.com/Faisal-M-alfaifi/OS-Assignment3-Faisal-AlFaifi |
 
---

## 🎥 Video Link

**Video Link** :https://drive.google.com/file/d/1kX9Bm7pKSaJQLed1SRwCqM0CjoWHbF4l/view?usp=sharing

> ⚠️ **WARNING:** The video must be **publicly accessible** ("Anyone with the link can view") on **Google Drive**, **YouTube (Unlisted or Public)** or any other cloud file-sharing system. A private, restricted or broken link counts as a **missing video (-1 mark)**.
>
> 💡 **TIP:** Open the link in a **private/incognito window** before you submit. If it asks you to log in or request access, it is not public.
>
> 📌 **NOTE:** The link goes in **this file only** (`MY_WORK.md`), **not** in `README.md`. Name your video file `StudentID_Assignment3_Demo.mp4`. It must last **2 to 3 minutes**.

---

## 🗺️ Work Roadmap (follow in this order)

| Step | What to do | Where | Marks |
|:----:|------------|-------|:-----:|
| 0 | Read `README.md`, read the full code, **run the original starter and save its output** (it fails on purpose) | Your IDE | – |
| 1 | Fork, rename, keep the repo **PUBLIC**, set your student ID (line 304), **commit** | GitHub + code | Part 1 (1) |
| 2 | Feature 1: Mutex lock on the ready queue, **commit** | Code | Part 2 (0.25) |
| 3 | Feature 2: Mutex lock(s) on the shared statistics, **commit** | Code | Part 2 (0.25) |
| 4 | Feature 3: Counting semaphore instead of busy waiting, **commit** | Code | Part 2 (0.5) |
| 5 | Development Log (5+ entries, different dates) | This file, Part A | Part 3 (0.5) |
| 6 | Reflection (4 questions) | This file, Part B | Part 3 (0.5) |
| 7 | Technical Answers (4 questions) | This file, Part C | Part 3 (0.5) |
| 8 | Record the video, upload it, paste the link above | Video + this file | Part 4 (1.5) |
| 9 | Final check, then submit the repo link on Blackboard | Blackboard | – |

> 💡 **TIP:** Tick each step off as you go. Do not leave the log, the reflection or the video for the last day.

---

## 🔁 Commit Rules (MANDATORY)

> ### ⚠️ MANY COMMITS ARE REQUIRED. A single bulk commit is penalized (-0.5 mark).

**Minimum: 4 meaningful commits. Aim for 7 or more.**

| # | Commit | Example message |
|:-:|--------|-----------------|
| 1 | Student ID set | `Set my student ID: 441234567` |
| 2 | Feature 1: Ready queue lock | `Feature 1: Protected the ready queue with a ReentrantLock` |
| 3 | Feature 2: Statistics locks | `Feature 2: Added locks to the shared statistics counters` |
| 4 | Feature 3: Semaphore | `Feature 3: Replaced busy waiting with a counting semaphore` |
| 5 | Development log entries | `Docs: Added development log entries 1-3` |
| 6 | Reflection and answers | `Docs: Completed reflection and technical answers` |
| 7 | Video link | `Docs: Added demo video link` |

**Rules:**
- ✅ **One commit per feature.** Do not put all three features in one commit.
- ✅ **Commit after each work session**, and after each part of this file.
- ✅ **Spread your commits over different dates.** Not all in one day.
- ❌ **Do not make all commits in the last hour** before the deadline (November 14, 2026).
- ❌ **No vague messages** like `done`, `update` or `final version`.

> 💡 **TIP:** Your commit history is checked and you **show it in your video** (at least 4 commits visible). Your development log dates should match your commit dates.
>
> 💡 **TIP:** **Use VS Code** (see *Recommended Development Environment* in `README.md` for the full setup). Sign in to GitHub in VS Code, then commit from the Source Control panel (Ctrl+Shift+G) → stage → write a message → Commit → Sync/Push. You can edit and commit this file the same way. **Pushing** matters: commits that are not pushed to GitHub are invisible to the instructor.

---

# Part A: Development Log (0.5 mark)

> ⚠️ **WARNING:** Minimum **5 entries**, spread over **different dates**. Five entries written on the same day, or written all at once at the end, will lose marks and look like a copy. Entry dates should be **between the start of the assignment and the deadline (November 14, 2026)**.
>
> 💡 **TIP:** Write an entry at the **end of each work session**, while you still remember what happened. It takes 5 minutes.
>
> 💡 **TIP:** Be specific. "Worked on the code" is a weak entry. "Added a `ReentrantLock queueLock` to `ReadyQueue` and wrapped the body of `poll()` in `lock()` / `try` / `finally { unlock() }`" is a strong one.
>
> 📌 **NOTE:** Each entry needs: date and time, what you did, details, challenges, solution, and time spent. Real challenges are fine (and expected). Do not invent fake ones.

## Example Entry (do not copy it, write your own)

### Entry 1 - [November 2, 2026, 4:30 PM]
**What I did**: Forked the repository, set my student ID, and ran the original starter

**Details**:
- Forked the starter repository and renamed it
- Changed student ID on line 304 to my actual ID (441234567)
- Ran the original program: 4 CPUs started, three of them picked `P1`, then `IllegalThreadStateException` and the watchdog stopped the program
- Saved the output in a text file for Question 1
- Committed and pushed: `Set my student ID: 441234567`

**Challenges**: I did not understand why the same process was picked by three CPUs

**Solution**: Read `ReadyQueue.poll()` again and found the `RaceWindow.pause()` between reading the head and removing it

**Time spent**: 45 minutes

---

## Your Development Log

### Entry 1 - [October 23, 2026, 7:04 PM]

**What I did**: Set up my GitHub repository and tested the original starter code.

**Details**:
- Forked the starter repository and opened it in VS Code.
- Changed the student ID to 445050079.
- Ran the original program before making synchronization fixes.
- The program showed incorrect counters and a WATCHDOG warning.
- Created my first commit: `Set my student ID: 445050079`.

**Challenges**: The original program did not always complete correctly because of race conditions.

**Solution**: I reviewed the code and compared the expected and observed values to understand where synchronization was needed.

**Time spent**: Approximately 1 hour.

---


### Entry 2 - [October 29, 2026, 1:50 AM]

**What I did**: Implemented Feature 1 to protect the shared ready queue using a ReentrantLock.

**Details**:
- Added queueLock inside the ReadyQueue class.
- Used lock() and try/finally to protect add(), poll(), processOf(), and snapshot().
- Tested the program several times to check the queue behavior.
- Created and pushed the commit: Feature 1: Protected the ready queue with a ReentrantLock.

**Challenges**: Multiple CPU threads could access and modify the ready queue at the same time, causing race conditions.

**Solution**: I used one ReentrantLock to protect the queue and made sure it was always released in the finally block.

**Time spent**: Approximately 40 minutes.

---

### Entry 3 - [November 6, 2026, 5:49 PM]

**What I did**: Implemented Feature 2 to protect the shared statistics counters using ReentrantLock.

**Details**:
- Added statsLock inside the SharedStats class.
- Used one lock to protect contextSwitchCount, completedProcessCount, and totalServiceTime.
- Protected the three update methods and the three getter methods.
- Used try/finally to make sure the lock was always released.
- Tested the program five times and confirmed that all three statistics matched the expected values.
- Created and pushed the commit: Feature 2: Added locks to the shared statistics counters.

**Challenges**: Multiple threads were updating the shared counters at the same time, causing lost updates and incorrect results.

**Solution**: I used one ReentrantLock for all three statistics and protected both reading and updating operations.

**Time spent**: Approximately 2 hours.

---

### Entry 4 - [November 10, 2026, 9:15 PM]

**What I did**: Implemented Feature 3 to replace busy waiting with a counting semaphore.

**Details**:
- Imported Semaphore and created readySemaphore inside the ReadyQueue class with an initial value of 0.
- Added release() to signal when a process is added to the ready queue.
- Used acquire() inside CpuWorker to wait for an available process.
- Removed the busy waiting loop and its unnecessary CPU polling.
- Added a shutdown signal to wake up waiting CPUs after all processes finished.
- Created and pushed the commit: Feature 3: Replaced busy waiting with a counting semaphore.

**Challenges**: The CPUs could remain blocked forever after the last process finished.

**Solution**: I used release(totalCPUs) to wake up the waiting CPUs and allow them to terminate correctly.

**Time spent**: Approximately 1 hour.

---

### Entry 5 - [November 11, 2026, 7:30 PM]

**What I did**: Reviewed the completed assignment and started preparing the documentation in MY_WORK.md.

**Details**:
- Reviewed the three completed synchronization features.
- Checked the final testing results from five consecutive runs.
- Confirmed that all four verification values matched the expected results.
- Reviewed the GitHub commit history for all three features.
- Started completing the Development Log using the actual work completed during the assignment.
- Checked the documentation requirements in README.md.

**Challenges**: Organizing the work completed across different sessions and making sure the documentation matched the actual code and test results.

**Solution**: I reviewed my GitHub commits, previous test results, and assignment instructions to document the work accurately.

**Time spent**: Approximately 1 hour.

---

### Entry 6 - [Optional - Date and Time]
**What I did**:

**Details**:

**Challenges**:

**Solution**:

**Time spent**:

---

## Development Log Summary

> 💡 **TIP:** Fill this in **last**, after all entries are written.


**Total time spent**: Approximately 5 hours and 40 minutes.

**Most challenging part**: Implementing the counting semaphore and making sure all CPU threads terminated correctly after the last process finished.

**Most interesting thing I learned**: I learned how ReentrantLock prevents race conditions and how Semaphore allows threads to wait without busy waiting.

**What I would do differently next time**: I would test each synchronization change earlier, document my progress after every session, and make smaller commits throughout development.


---

# Part B: Reflection (0.5 mark)

> 🛑 **STOP:** Do **not** start this part until you have read the `README.md`, read the **entire** `SchedulerSimulationSync.java`, run it, and finished the three features.
>
> ⚠️ **WARNING:** Each answer must be **5 to 7 sentences**, in **your own words**. Copied or AI-generated answers without understanding get **0 marks for the whole assignment**. You may be asked to explain them in person.
>
> 💡 **TIP:** Mention concrete things you actually did: a method you wrote, an error you hit, a line of output you saw. Generic answers score low.
>
> 💡 **TIP:** Draft your answer in a few bullet points first, then turn them into sentences.

## Question 1: What did you learn about synchronization?

> 💡 **TIP:** Talk about race conditions (read-modify-write), critical sections, mutual exclusion with `ReentrantLock` and `try/finally`, the role of a counting semaphore, and what surprised you when the starter failed.

**Your Answer:** *(5-7 sentences)*


I learned that synchronization is important when multiple threads access shared data at the same time. In the original program, race conditions caused incorrect results because threads updated the same variables without protection. I used ReentrantLock to protect the ready queue and shared statistics. I also learned that try/finally makes sure the lock is released correctly. Using a counting semaphore helped me replace busy waiting with a more efficient way for CPU threads to wait. After applying these changes, the program produced correct results in repeated tests.

## Question 2: What was the most challenging part of this assignment?

> 💡 **TIP:** Pick **one** specific challenge (understanding why the starter failed, choosing the lock granularity, the initial value of the semaphore, the shutdown of the CPUs, Git, the video) and say *why* it was hard.

**Your Answer:** *(5-7 sentences)*


The most challenging part of this assignment was implementing the counting semaphore correctly. I needed to understand how CPU threads should wait when the ready queue is empty. At first, I was concerned that some threads might remain blocked after all processes finished. I had to make sure the semaphore released enough permits to wake up the waiting CPUs. I solved this by using release(totalCPUs) when the last process completed. This helped me understand how important thread termination is in synchronization.

## Question 3: How did you overcome the challenges you faced?

> 💡 **TIP:** Describe your method: reading the slides and the documentation, adding `System.out.println` to debug, running the program many times, re-reading the README, testing after each small change, asking for help.

**Your Answer:** *(5-7 sentences)*


I overcame the challenges by working on one feature at a time. First, I reviewed the code to understand where race conditions happened. Then, I added locks to protect the ready queue and shared statistics. For the semaphore, I checked how threads wait and how they wake up when a process becomes available. I tested the program multiple times after making changes to make sure everything worked correctly. Comparing the expected and observed results helped me confirm that my solutions were successful.

## Question 4: Where can synchronization concepts be applied in real-world applications?

> 💡 **TIP:** Use real applications you know (banking and money transfers, ticket or seat booking, a shared counter on a website, a print queue, a database) and connect each one to what you built here (shared data, critical section, lock or semaphore).

**Your Answer:** *(5-7 sentences)*


Synchronization is used in many real-world applications where multiple users or threads access shared resources. In banking systems, locks help prevent incorrect account balances when transactions happen at the same time. Online ticket booking systems use synchronization to prevent two customers from booking the same seat. Databases also use locks to protect shared data during updates. A print queue is another example where a semaphore can help manage available work. These examples are similar to my assignment because multiple CPU threads need safe access to the shared ready queue.

### Optional: What would you like to learn more about?

[Any topics related to synchronization or operating systems that you're curious about?]

### Optional: How confident do you feel about synchronization concepts now?

[Beginner / Intermediate / Confident. What do you understand well? What needs more practice?]

### Optional: Feedback on the assignment

[Any comments? Was it helpful? Too easy or hard? Suggestions?]

---

# Part C: Technical Answers (0.5 mark)

> 🛑 **STOP:** You cannot answer these questions without understanding the code. Re-read `SchedulerSimulationSync.java` and **run it** first. Your answers must reference **your own code and your own output** (your student ID makes your output and your expected values unique).
>
> ⚠️ **WARNING:** Each answer must be **3 to 5 sentences**, with specific examples from your code or output. Use correct terms: race condition, critical section, mutual exclusion, mutex lock, semaphore, busy waiting, deadlock, producer, consumer.
>
> 💡 **TIP:** Keep the output of the **original starter** and the output of your **final version** in text files or screenshots, so you can copy real snippets for Question 1.

## Question 1: Race Condition in Your Own Output

**Question**: Run the **original starter** (before any fix) and paste the **verification block** of that run. Which value was wrong (expected vs observed)? Explain **step by step**, with two named threads/CPUs, how **one lost update** happens on one of the shared variables (read, `RaceWindow.pause()`, write). Why can the same bug happen on a real machine even without `RaceWindow`, and why is it hard to detect?

> ⚠️ **WARNING:** The snippet must come from **your own run** (with your student ID), not from a classmate or from this README.
>
> 💡 **TIP:** Use a small timeline: *CPU-1 reads `contextSwitchCount` = 12 → CPU-2 reads 12 → CPU-1 writes 13 → CPU-2 writes 13 → one increment is lost.* If your starter run crashed before printing numbers, run it several times (or paste the exception and the watchdog message and explain it).

**Your Answer:** *(3-5 sentences)*


In my original run, context switches were 29 instead of 35, completed processes were 14 instead of 17, and total service time was 66574 instead of 80047. This happened because multiple CPU threads could read and update shared variables at the same time. RaceWindow.pause() increased the chance of a lost update by allowing two threads to read the same value before writing. This can also happen without RaceWindow.pause() because thread execution order is unpredictable, making the problem difficult to detect. After using ReentrantLock, the final program produced the expected results.

Verification block of the **original starter**:
```
Context switches: Expected 35, Observed 29
Completed processes: Expected 17, Observed 14
Total service time: Expected 80047, Observed 66574
Busy-waiting polls: Expected 0, Observed 560
WATCHDOG triggered after 27 seconds
```

Verification block of **my final version**:
```
Context switches: Expected 35, Observed 35
Completed processes: Expected 17, Observed 17
Total service time: Expected 80047, Observed 80047
Busy-waiting polls: Expected 0, Observed 0
All verification checks passed.
```

**Explanation of the timeline:**

CPU-1 reads contextSwitchCount = 12, and CPU-2 also reads 12 before CPU-1 finishes updating it. CPU-1 writes 13, then CPU-2 writes 13 instead of 14. As a result, one increment is lost because both threads updated the same shared value without mutual exclusion.

## Question 2: Critical Sections and Lock Granularity

**Question**: List the **critical sections** you protected (variables and methods) and the lock(s) you used. **Lock granularity:** did you use **one lock** for the three statistics or **one lock per variable**? Why, and what is the trade-off? Why is the **ready queue** protected by a **different** lock than the statistics? Explain how your solution provides **mutual exclusion**, and discuss **progress** and **bounded waiting** (a default `ReentrantLock` is not fair: what does that imply?).

> 💡 **TIP:** The three counters are independent: does updating `contextSwitchCount` need to block an update of `totalServiceTime`? Also think about what could go wrong (deadlock, or long waiting) if the queue lock and the statistics lock were the **same** lock and a thread held it while doing something slow.

**Your Answer:** *(3-5 sentences)*


I protected the ReadyQueue methods using queueLock and the three shared statistics using statsLock. I used one lock for all three statistics because it was easier to manage, but separate locks could reduce unnecessary waiting. I used a different lock for the ready queue so queue operations would not block statistics updates. Both locks provide mutual exclusion by allowing only one thread to access each protected critical section at a time. The default ReentrantLock is not fair, so bounded waiting is not guaranteed, although threads can make progress when locks are released.

| Critical section (variable / method) | Lock used | Why it needs protection |
|---|---|---|
| ReadyQueue: add(), poll(), processOf(), snapshot() | queueLock | Prevents multiple CPU threads from accessing or modifying the shared queue at the same time. |
| SharedStats: contextSwitchCount, completedProcessCount, totalServiceTime (update methods and getters) | statsLock | Prevents race conditions and lost updates when CPU threads access the shared statistics. |
## Question 3: Busy Waiting vs Semaphore

**Question**: Describe the **busy waiting** of the starter and its cost (give the `Busy-waiting polls` number from your **starter** run). What does the **value of your semaphore** represent? What is its **initial value** and why? What is its value right after the `numProcesses` initial `add()` calls? Why does the last CPU call `release(totalCPUs)` at the end, and what would happen if it did not?

> 💡 **TIP:** Think about what a CPU does when the queue is empty in the starter, and what a CPU does in your final version (is it running, ready or blocked?). Also check what happens to a CPU blocked in `acquire()` when no process will ever be added again.

**Your Answer:** *(3-5 sentences)*


In the original program, CPU threads repeatedly checked the empty ready queue, causing 560 busy-waiting polls and wasting CPU resources. I replaced this with a counting semaphore that represents the number of available processes in the queue. The semaphore starts at 0 because the queue is initially empty, and after numProcesses initial add() calls, it has numProcesses permits before any CPU consumes them. When the queue is empty, acquire() blocks the CPU thread instead of repeatedly checking the queue. When the last process finishes, release(totalCPUs) wakes up waiting CPU threads so they can exit; without it, some threads could remain blocked forever.

## Question 4: Classical Problems and Deadlock

**Question**: The CPUs and the ready queue look like a classical synchronization problem of Chapter 5. **Name it**, and say who plays the **producer** and the **consumer** roles (careful: here the CPUs also re-enqueue processes). If the ready queue were **bounded** (capacity `K`), name the **three semaphores** you would need and their **initial values**. Describe a **deadlock scenario** that appears if a thread acquired the **mutex before** waiting on the semaphore (or if two locks were acquired in different orders), and say **which of the four necessary conditions** you would break to prevent it.

> 💡 **TIP:** Recall the bounded-buffer solution of the slides (`empty`, `full`, `mutex`) and the order of `wait()` calls in the producer and the consumer. For the deadlock, think about a producer that holds the mutex while waiting for a free slot that only a consumer (who needs the mutex) can create.

**Your Answer:** *(3-5 sentences)*

This assignment follows the producer-consumer problem, where the main thread initially adds processes and CPU threads consume them, while CPUs can also re-enqueue unfinished processes. For a bounded queue of capacity K, I would use three semaphores: empty initialized to K, full initialized to 0, and mutex initialized to 1. A deadlock could happen if a producer holds mutex while waiting for an empty slot because the consumer cannot acquire mutex to remove a process. To prevent this, I would acquire empty before mutex, breaking the hold-and-wait condition.

**Classical problem and roles**:

The classical problem is Producer-Consumer. The main thread is the initial producer because it adds processes to the ready queue. CPU threads are consumers because they take processes from the queue, but they also act as producers when they re-enqueue unfinished processes.

**Semaphores for a bounded queue (name and initial value)**:

For a bounded queue with capacity K, the three semaphores are:
- empty = K (counts available empty slots)
- full = 0 (counts available processes)
- mutex = 1 (provides mutual exclusion)

**Deadlock scenario and prevention**:

A deadlock can happen if a producer holds the mutex while waiting for an empty slot in a full queue. The consumer cannot acquire the mutex to remove a process, so both threads remain blocked. To prevent this, the producer must wait for an empty slot before acquiring the mutex, avoiding the hold-and-wait situation that caused the deadlock.

## Summary

**Key concepts I understood through these questions:**
1. ReentrantLock protects critical sections and prevents race conditions.
2. Counting semaphores allow threads to wait without busy waiting.
3. Proper synchronization prevents lost updates and helps avoid deadlocks.


**Concepts I need to study more:**
1. Deadlock prevention and the four necessary conditions for deadlock.
2. Advanced semaphore usage and solving complex synchronization problems.


---

# ✅ Final Checklist (complete before submitting)

> ⚠️ **WARNING:** Go through every line. Blackboard does not accept submissions after the deadline, which is **November 14, 2026**.

**Repository**
- [x] Repository is **PUBLIC** (Settings → Danger Zone → Visibility)
- [x] Repository is renamed to `OS-Assignment3-YourFirstName-YourLastName`
- [x] GitHub account uses the university email (`@std.psau.edu.sa`)

**Code**
- [x] Student ID is set in `SchedulerSimulationSync.java` (line 304)
- [x] My code is based **only** on the starter of this repository (nothing copied from previous assignments)
- [x] Code compiles and runs with no errors, and terminates by itself (no `⛔ WATCHDOG`)
- [x] Feature 1 (ready queue lock), Feature 2 (statistics locks) and Feature 3 (semaphore, no busy waiting) all work
- [x] **The four verification lines are ✔ in 5 consecutive runs**
- [x] Every lock is released in a `finally` block
- [x] `RaceWindow`, `Config`, the verification block and the watchdog are **unchanged**
- [x] Each feature has clear comments

**Commits**
- [x] **At least 4 meaningful commits, ideally 7 or more**
- [x] **One commit per feature**
- [x] Commits are spread over **different dates** (not all in the last hour)
- [x] Everything is **pushed** to GitHub

**This file (`MY_WORK.md`)**
- [x] Full name and student ID filled in at the top
- [x] Development log has **5+ entries** on different dates
- [x] Reflection: 4 questions, 5-7 sentences each
- [x] Technical answers: 4 questions, 3-5 sentences each, with examples from **your** output (starter output **and** final output pasted in Question 1)
- [x] No `[...]` placeholders left
- [x] No section headers deleted

**Video**
- [x] 2-3 minutes long, named `StudentID_Assignment3_Demo.mp4`
- [x] Shows your name, ID, repository, 3 features (and your lock granularity choice), IDE execution with the verification block, one synchronization concept, and commit history
- [x] Link is **public** (tested in an incognito window) and pasted in the **Video Link** section above

**Blackboard**
- [x] Submit **only** the link to your public GitHub repository

> 🎯 **Good luck!** Start early, commit regularly, and make sure you can explain every line you submit.
