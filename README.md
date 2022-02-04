IDEAS
=======

Project summary
---

The website is a platform for a potluck-style competition. Users can both contribute problems and participate in the 
competition.

First, any competitor or contributor must create an account. In the account creation, the user chooses topics that they 
are comfortable with. This allows the website to determine if the user is capable of solving a given challenge problem 
without giving directly giving away any information about the problem. We also require a username and password. The username will be used for both sharing 
scores and displaying creators of problems. We don't want other users to see each other's scores without permission or 
problems in advance, so we require a password. Users can provide an email to be notified of the competition start and 
score updates. We allow users to opt in or out of public score statistics. The user can change any of these options at 
any time.

Each user can upload up to one problem. The user selects 1-2 topics related to the problem to "claim" them. 
Similarly to how we only want one person bringing a cake, plates, etc. in a real potluck, having many similar problems
can make the competition less interesting. Once a topic has been claimed, it is no longer visible so nobody can even 
know that it was an option. The user can elect to (and should) choose a topic prior to uploading the problem, which will 
again hide it from the list. When uploading the problem, the user also selects from the list of background topics to 
denote which topics the problem/solution require knowledge of. The user can preview, change, or delete the problem until 
the competition starts.

Once the competition opens, logged-in users of the website can see the problems, whether they have the background for 
them, and the option to submit a solution. This submission box will be open until the competition closes, but all other 
elements of the table will still be visible. 

Once the competition closes, problem contributors will have access to a table of submissions to their problems. Once one 
problem has been graded, the table will be updated to show scores for all problems (incomplete if grades are not 
submitted). The problem contributor can opt to grade the problems or have the competition organizers do it. They will 
have a month to grade. If it is not done by this time, the organizers will grade the problem.

**Questions to people working on this with me:**

- Should we hide topics that have already been claimed (what if a user submits a problem that doesn't match a visible 
topic because they didn't realize that the topic had been claimed)? However, this feature ensures as little information 
is known about the problems contributed as possible.
- Should we wait until the full month passes before displaying graded scores or just display as they come?


Background list:
---

- Store as JSON
- Calculus 1: limits and differentiation
- Calculus 2: integration and series
- Calculus 3: multivariable calculus 1&2, Green's, Stoke's, Divergence
- Discrete math: logic, modular arithmetic, naive set theory, basic combinatorics, relations
- General topology: limit points, connectedness, compactness
- Real analysis: structure of real line, limits, continuity
- Complex analysis: Cauchy-Riemann equations, Cauchy's theorem, residue theorem
- Group theory: Lagrange's theorem, Sylow theorems

Topic list: 
---
Select 1-2 from background list + additional choices

- Store as JSON
- Parity problem
- Invariant/Monovariant problem
- TODO: Add more

User sign-up:
---

- Username
- Password (hash before sending to server)
- Optional email
- "I want my name to be visible in public score statistics." (This can be changed at any time, even after scores are 
shared)
- "I acknowledge that regardless of my previous choice, my score (without my name) will be visible in public score statistics."
- Select from background list for topics user is comfortable with (confident, familiar, no understanding)

Update account to admin account:
---

- Enter admin password to become admin
- Admins can view/delete problems at any time
- Admins can delete user accounts and view their emails
- Admins can add/remove background items and topics
- Admins cannot view names on statistics/solutions that are not visible to general users
- After grading deadline or after a grade is submitted, admins can view/adjust grades and solutions 

Topic claim:
---

- Before problem upload, a user can claim a topic from the topic list so that they can fully develop their problem without needing to rush before someone else claims it

Problem upload:
---

- Upload as pdf, png, jpg, or tex
- Select from background list for topics needed to solve problem (heavy, light, none)
- Select topic or confirm topic chosen before
- Select additional allowed resources
- "I confirm that I have a full solution of this problem and that it requires no knowledge beyond the topics selected."
- "I will grade this problem within one month of the competition end date." (if not checked or deadline missed, 
competition organizers will grade the solutions) 
- Preview problem
- Users who upload problems can provide access to view the problem/solution to any other user

Problem table:
---

| Problem creator    | Problem | Has background | Submit solution           |
|--------------------|---------|----------------|---------------------------|
| Username of writer | Link    | X/Checkmark    | Upload pdf, png, jpg, tex |

Grading table:
---

| Submission | Enter grade (integer 0-10) |
|------------|----------------------------|
| Link       | Text box                   |

Score statistics:
---

Total scores

| Username               | Score               |
|------------------------|---------------------|
| Username of competitor | Nonnegative integer |

Statistics by problem

| Problem creator    | Problem | Has background (if logged in)  | My score (if logged in) | Number of submissions | Average score of submissions | Top score | Top score recipients    | Detailed summary      |
|--------------------|---------|--------------------------------|-------------------------|-----------------------|------------------------------|-----------|-------------------------|-----------------------|
| Username of writer | Link    | X/Checkmark                    | 0-10                    | 0+                    | Round to 2 digits            | 0-10      | Usernames (if opted in) | Link to expanded info |

Detailed summary: lots of statistics/plots/etc + this table

| Username               | Score               |
|------------------------|---------------------|
| Username of competitor | Nonnegative integer |
