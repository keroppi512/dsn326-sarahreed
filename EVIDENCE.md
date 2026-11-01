# Evidence

*Raw findings. Not summaries.*

Replace this placeholder in Week 1. Your token values from the parity check go in first.

**The rule:** somebody else should be able to open this file and audit your conclusions without asking you a question.

**What goes in:**

- **Forum quotes** with their source URL and date. The actual quote, not your paraphrase.
- **Per-participant session results.** One block per person: date, which round, how you ran it, task by task, what they did, what they said, where they stopped.
- **Consent records.** For a live session, that you read the line. For an asynchronous one, their "yes" reply with the date.
- **Coded themes**, with how many items fell into each.
- **Token values** from the Week 1 parity check, both sides.
- **Cancellations**, with the date you booked and the date they dropped.

**What doesn't:** conclusions, arguments, anything you have already interpreted. Those go in [DECISIONS.md](DECISIONS.md) or your Studio submission.

Keeping raw evidence separate from your reading of it is what lets you change your mind without losing the data.

---

## Week 1: Rail parity check

| Token | Figma value | `tokens.css` value | Agree? |
|---|---|---|---|
| text-secondary | #524C46 | #6E675F | no |
| type-label-line | 20px | 20px | yes |
| space-inset-md | 16px | 16px | yes |
| radius-full | 9999px | 9999px | yes |
| target-comfortable | 48px | 48px | yes |

Density:
This table records the values of each token changing based on density.
| Token | Comfortable | Compact | Service |
|---|---|---|---|
| type-body-size | 16px | 14px | 24px |
| space-inset-md | 16px | 12px | 24px |

Environment:
This table records target-min at each environment setting.
| Environment | Comfortable | Compact | Service |
|---|---|---|---|
| standard | 44px | 44px | 44px |
| high-glare | 56px | 56px | 56px |

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
Default - background is transparent with a small surface/subtle outline on the bottom of the item
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
Allows the user to enter a number via increment and decrement buttons
Variants: N/A
States:
Default - Contains a background color of surface-raised as well as a thin border. Has two buttons on either side, one to increment the number and another to decrement the number. The buttons have a hover, active, and focus state. Hover changes the button to surface-subtle when hovered over, active changes the color to interactive-subtle, and focus adds a focus ring that is border-focus color and is focus-ring-width in width.
Min reached - the decrement button is disabled and can no longer be pressed.
Max reached - the increment button is disabled and can no longer be pressed.
Fully disabled - the stepper cannot be incremented or decremented. Color changes to surface-subtle and border-subtle.
Tokens used:
stepper-total-width, border-default, radius-sm, surface-raised, stepper-button-size, target-min, type-body-size, type-label-weight, text-primary, surface-subtle, interactive-subtle, focus-ring-width, border-focus, stepper-value-width, type-body-size, type-body-line, type-label-weight, text-disabled, border-subtle.
What surprised me:
I didn't think about the need for a state to disable the increment and decrement buttons until I looked at the source and saw the states. It made sense when I saw it, but it did not come to mind at first. 

---


## Sessions

### P1 — YYYY-MM-DD, round [1/2]

**Consent:** 
**Setup:** 
**Task 1:** 
**Task 2:** 
