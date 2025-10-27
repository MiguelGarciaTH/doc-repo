# Things I Learnt The Hard Way (in 30 Years of Software Development)

**Author:** Julio Biasson

**Date:** 2019-06-10

**Source:** [Julio Biason .Me 4.3 Old school dev living in a 2.0 dev world](https://blog.juliobiason.me/thoughts/things-i-learnt-the-hard-way/)

This is a lesson-like post, the author goes on different lessons from his last 30 years of software developmenet. Some of the lessons are very technical, some are very language/tool/framework specific, others are more related to team work and company culture and envirement.

Here I will cover just the ones that are were more relevant to me and add my opinion on it.

## Software Development

### Spec first, then code

>If you don't know what you're trying to solve, you don't know what to code.
>
>Write something specifying how the application works before writing any code.
>
>"Without requirements or design, programming is the art of adding bugs to an empty text file." -- Louis Srygley
>
>Sometimes, even an "elevator pitch" -- up to two paragraphs that describe what the application does -- is enough.
>
>The times I stood longer looking at my own code wondering what to do next were when we didn't have the next step defined. It is a good sign that it's time to stop and discuss it with your coworkers -- or maybe rethink the solution.

Sometimes, I struggle starting coding without a clear specification. Usually, I am too far from the final user, and I am asked to start on solving vague problems. If there is something that does not match with vague is software. Software is very concrete. Typically, bad specifications (by bad you can assume also inexistent specs), lead to unhappy users and a frustrated developers. We wasted time and energy trying to solve something, and in the end, we need to re-do if not everything a big part of it. Important note, this is very different than evolving code/features/requirements. We can start with a concrete spec and later find (hopefully with the user's help) that we did not solve exactly what he was expecting. 

These type of problems, which tend to be in a vicious cycle, are mostly caused by misalignment of expectations.

### Write steps as comments

> If you have no idea how to start, describe the flow of the application in high level, pure English/your language first. Then fill the spaces between comments with the code.
>
> Better yet: think of every comment as a function, then write the function that does exactly that.

I started doing this not long ago; it is a very simple trick to break down the approach to solving the problem. I usually prefer pen and paper, but sometimes this is quicker, and doing it in the code helps to frame the solution in its place. Besides helping the reasoning process, it also hints at how many auxiliary methods will be needed. In a few lines of description, you can see blocks of logic that are directly mapped to functions.


### Future thinking is future trashing

> When developers try to solve a problem, they sometimes try to find a way that will solve all the problems, including the ones that may appear in the future.
>
> But here is the thing: The problems from the future will never come and you'll end up either having to maintain a huge behemoth of code that will never be fully used or you'll end up rewriting the whole thing 'cause there is a shitton of unused stuff.
>
> Solve the problem you have right now. Then solve the next one. And the next one. At one point, you'll realize there is a pattern emerging from those solutions and then you'll find your "solve everything".

I have mixed feelings about these statements. First, this is not a golden rule; sometimes you can anticipate inevitable problems and accommodate resources in that direction. As a rule of thumb, I always consider scalability and maintainability. In particular, for maintainability, I take a bottom-up approach: start with a data model that grows easily and keep code modular. When everything is well encapsulated and has good quality tests, you can perform changes without pain.

Nevertheless, I think the author is mainly referring to feature-like problems. For example:
> "We may also need a service to upload profile photos, this should be cached, crop the images, and support access to old photos, etc."

In these types of scenarios, yes, don't fall into the "what if" pit. Keep features clear and concise, addressing them with focus. A principle I like is "divide and conquer."
