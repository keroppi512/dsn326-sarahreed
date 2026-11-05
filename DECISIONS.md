# Decisions

*Every decision you make this term, with a date and a reason. Your AI log lives here too.*

Replace this placeholder in Week 1. Put something real in it — your backlog item and why you picked it is a decision like any other.

**What goes in:** decisions, the gaps you closed and how, what you declined to do, what you cut, system decisions, anything you re-framed later, and your AI log. **What doesn't:** raw findings. Those go in [EVIDENCE.md](EVIDENCE.md).

Write it as you go. Reconstructing this in Week 7 produces a file that reads like a case study rather than a record, and the design walkthrough will find the difference.

Full structure is in the **Decision Record** template. The short version:

```markdown
## 2026-09-14 — Chose Option B over A

**What I decided:** [one line]
**Why:** [the evidence, named]
**What I gave up:** [the cost]
**What would change this:** [what evidence would flip it]
```

For an AI entry, same shape: which tool, what for, what you kept, what you changed. Directing a tool is a decision.

---
Service density has larger body text to compensate for all of the parts of food service that would make an app on a handheld hard to view. Customers are likely in a low stress, stationary state where there isn't much going on around them. This means they can have smaller text. Service workers are constantly on the move and therefore it is harder to read the smaller text that comes with the comfortable or compact densities.

target-min doesn't get smaller with compact because it is a constant throughout all of the densities. It is a safety gate to keep elements compliant with accessibility needs. 

Component 1:  
List Row  
What it does:  
Displays information for the user to view and select.  
Variants:  
Basic - Heading only  
Detailed with secondary text - Heading with secondary text  
With trailing price - Heading with secondary text and a price on the side.  
States:   
Default - background is transparent with a small surface/subtle outline on the bottom of the item.   
Hover - color changes to surface-subtle when mouse hovers.  
Focus - outline with border-focus with a width of focus-ring-width and an offset of focus-ring-offset.  
Active - surface-subtle background color.  
Disabled - background color becomes surface/subtle with a 0.5 opacity.  
Selected - surface-brand-subtle background, outline to the left with border interactive-default. There is a hover variant that does not change anything, as the background is the only property declared and it stays the same.  
Tokens used:   
space-inline-md, list-row-min-height, space-inset-sm, space-inset-md, border-subtle, surface-subtle, surface-brand-subtle, focus-ring-width, border-focus, focus-ring-offset, interactive-default, list-row-leading--size, radius-full, text-secondary, type-body-size, type-body-line, type-label-weight, text-primary, type-caption-size, type-caption-line, type-caption-weight, space-gap-sm, text-tertiary, type-caption-size, type-caption-line, target-min, radius-sm.  
What surprised me:   
This component seemed very simple at first glance, however once I looked into the CSS and saw what when into it I was amazed at how many tokens and states go into this component.   

Component 2:  
Stepper  
What it does:  
Allows the user to enter a number via increment and decrement buttons. 
Variants: N/A. 
States:  
Default - Contains a background color of surface-raised as well as a thin border. Has two buttons on either side, one to increment the number and another to decrement the number. The buttons have a hover, active, and focus state. Hover changes the button to surface-subtle when hovered over, active changes the color to interactive-subtle, and focus adds a focus ring that is border-focus color and is focus-ring-width in width.  
Min reached - the decrement button is disabled and can no longer be pressed.  
Max reached - the increment button is disabled and can no longer be pressed.  
Fully disabled - the stepper cannot be incremented or decremented. Color changes to surface-subtle and border-subtle.  
Tokens used:  
stepper-total-width, border-default, radius-sm, surface-raised, stepper-button-size, target-min, type-body-size, type-label-weight, text-primary, surface-subtle, interactive-subtle, focus-ring-width, border-focus, stepper-value-width, type-body-size, type-body-line, type-label-weight, text-disabled, border-subtle.  
What surprised me:  
I didn't think about the need for a state to disable the increment and decrement buttons until I looked at the source and saw the states. It made sense when I saw it, but it did not come to mind at first.   


## 2026-10-13 - Created 5 Task Script

**What I decided: The tasks that I would have my testers complete**  
**Why: I would like for them to encounter the ticket's problem head-on, and these tasks will bring them to it.**  
**What I gave up: n/a**. 
**What would change this: If there was another piece to the puzzle, I would alter the tasks to include this as well.**  

## 2026-11-4 - Gap Closure

Week 2 Studio A: Gap Closure  

Gap 1: The Missing Number  

The Gap: The specific percentage of abandoned checkouts, and how much they have grown since before the March change.  
What I found: The number of abandoned carts has grown from 24% to 29% after the change in March. No step-level breakdown is available according to Dev.  
Source: PM Pack Metrics confirmed with Dev.  
What it changes: This number is very dramatic and demands a fix to encourage customers to complete their purchases without confusion or frustration about where fees are coming from. By adding this metric, it makes the severity of the problem more apparent. Not knowing where specifically customers leave in the checkout process is a handicap, and I will have to monitor that.  

Gap 2: The solution disguised as a problem  

What the ticket asks for: Running breakdown added to the cart.  
The problem underneath it: Customers see a total price on screen that they can’t account for and, feeling misled or surprised by the fees, abandon the checkout process.  
How I know they are different: By only giving this proposed solution, ideas for simpler solutions are not in the equation. By presenting the problem at hand instead, there is more room for these ideas.  
Does the proposed solution address the real problem? Partly. It would technically solve the problem by showing the user the fees up front and eliminate any surprises, however this would be difficult to implement without the screen becoming cluttered. I think there are more elegant solutions to be explored here.  

Gap 3: The unstated constraint  

The constraint: Legal compliance changes in March require fees to be shown before the charge via an itemized cost breakdown.   
Where I found it: PM Pack Constraint Registry. 
What it rules out: Hiding fees within the cost of food items, one-tap checkout, explaining the fees after the customer pays, lumping fees together.  
