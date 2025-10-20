
# The Paradox of Alerts — Notes from Charity Majors

**Source:** [Charity Majors – The Paradox of Alerts](https://speakerdeck.com/charity/the-paradox-of-alerts)

Most of the presentation is about alerts/on-call — how teams can organize themselves to handle them more efficiently, and how to reduce the suffering of being on-call. But there are other interesting and thought-provoking ideas that are worth highlighting. Disclaimer, I am not on-call rotation, nevertheless, I am close to some people who are.

## Table of Contents

1. [The Paradox of Alerts — Notes from Charity Majors’ Talk](#the-paradox-of-alerts--notes-from-charity-majors-talk)
2. [🔥 The Pain of Being On-Call](#-the-pain-of-being-on-call)
3. [🧩 Making On-Call “Enjoyable”](#-making-on-call-enjoyable)
4. [💻 Software Ownership](#-software-ownership)
5. [🚨 Managing Alerts](#-managing-alerts)
   - [Align User Pain with Engineering Pain](#align-user-pain-with-engineering-pain)
   - [Delete Flappy Alerts](#delete-flappy-alerts)
   - [Keep a Second Lane for Alerts](#keep-a-second-lane-for-alerts)
   - [Set a High Bar for Wake-Up Alerts](#set-a-high-bar-for-wake-up-alerts)
   - [Include Documentation Links](#include-documentation-links)
   - [Training Is Mandatory](#training-is-mandatory)
6. [☕ Managing the On-Call Experience](#-managing-the-on-call-experience)
7. [🧠 Reducing the Number of Problems](#-reducing-the-number-of-problems)
8. [👩‍💼 Managers Matter](#-managers-matter)
9. [🧭 Final Thought](#-final-thought)


---

## 🔥 The pain of being on-call

The talk opens with several quotes showing the physical and mental toll of being on-call. This suffering doesn’t just harm individuals — it also hurts the company. When engineers are burned out from late-night firefighting, we stop delivering our best work.

It’s impossible to sustain an on-call rotation and simultaneously ship high-quality features if it’s the same people doing both.

---

## 🧩 Making on-call “enjoyable”

Charity Majors proposes several fixes to make on-call less painful — even enjoyable.

First, let’s look at her ideal definition of on-call:

- An essential part of software ownership    
- A social contract between engineers and managers    
- A set of expert practices and techniques in its own right    
- A proxy metric for how well your team is performing, how functional the system is, and how happy your users are    

---

## 💻 Software ownership

Those who write the code should also be on-call for it. This closes the feedback loop, reduces unnecessary stress for others, and leads to faster fixes — and ultimately, happier users.

Managers, on the other hand, should “move mountains” to make sure that owning the code doesn’t suck. If they don’t, you should quit and end the suffering loop.

---

## 🚨 Managing alerts

We can’t avoid alerts — but we can make them meaningful. It’s far more stressful to receive false alarms for components we don’t own than real ones for systems we understand deeply.

Let’s take an example:

- 8-person on-call rotation    
- 1 week per person    
- 4 serious alerts per month    

That adds up to roughly **4–5 serious alerts per person per year**, which is manageable if the alerts are relevant and actionable.

### Practical principles

1. **Align user pain with engineering pain.**    
    - Stop alerting on symptoms — use SLOs (Service-Level Objectives) instead.        
    - Make code fail fast.        
    - Design architecture for partial, graceful degradation.        
2. **Delete flappy alerts.**  
    They’re distracting and often ignored. If they indicate a real issue, handle it outside the alerting system.    
3. **Keep a “second lane” for alerts.**  
    Not everything needs to page someone at 3 a.m. Some can wait until morning.    
4. **Set a high bar for wake-up alerts.**    
5. **Every page should include a link to documentation** on how to fix the problem.    
6. **Training is mandatory.**  
    Everyone who goes on-call should be prepared and confident to handle alerts. Frustration makes stress worse — encourage escalation and teamwork.
    
---

## ☕ Managing the on-call experience

No one should be on-call the night after a brutal shift. Imagine you’re on-call when a new, unstable feature goes live. After two sleepless nights, you’re exhausted — unproductive during the day and irrational at night.

When you’re on-call, focus on improving the system: write tests, refactor, fix small things, explore ideas — and have fun. Don’t work on roadmap features during that week.

Also, think about **incentives**: give the next Friday off, or pay generously enough that finance asks to invest in reliability to save on on-call costs.

---

## 🧠 Reducing the number of problems

1. **Anticipate debugging.**  
    Inspect code, review dashboards, and look for outliers before users find them.    
2. **Remember the cost curve.**  
    The cost of fixing a bug increases exponentially the closer it gets to production.    
3. **Encourage retrospectives.**  
    If an issue is too large to fix during on-call, bring it to the roadmap. Be explicit about the impact, pay off tech debt, and strengthen resiliency.  
    Reliability, performance, security, and tech debt are not “secondary features” — they belong on the roadmap.    
4. **On-call gives moral authority.**  
    The people who suffer the pain have the right to demand change.    
5. **(Controversial but valid) Test in production.**  
    Many bugs only appear in real conditions — due to context, infrastructure, load, or complexity.  
    Invest in observability and resilience: chaos experiments, fault injection, and continuous stress testing.    
6. **Redefine success.**  
    Success isn’t “no incidents.” It’s handling incidents safely, confidently, and sustainably — and being ready to go on-call again.    

---

## 👩‍💼 Managers matter

Managers who run their teams into the ground should never be promoted.

High-performing teams spend most of their time solving interesting problems and creating value. Low-performing teams are trapped in endless firefighting: chasing bugs, debugging flaky tests, answering complaints, wrestling with infrastructure and tools.

Build only what you must. The engineering cycle is expensive — misuse leads to frustration and poor retention.

It’s always easier to **avoid the pit of doom** than to climb out of it.

---

### 🧭 Final thought

Sustainable on-call isn’t about eliminating pain.  
It’s about designing systems, cultures, and incentives where **reliability is shared ownership** — and where engineers can take pride, not punishment, in keeping things running.