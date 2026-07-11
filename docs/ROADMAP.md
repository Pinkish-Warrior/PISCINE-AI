# AI.GO Roadmap

Visual learning path through the AI.GO curriculum (01-edu). Same content as [`WORKFLOW.md`](WORKFLOW.md), as a diagram instead of tables.

```mermaid
flowchart TD
    Start([Start: No coding experience needed]) --> SetupChoice{{Own machine or<br/>college machine?}}

    SetupChoice -->|Own machine| SetupA
    SetupChoice -->|College machine| SetupB

    subgraph SetupA["Option A — Own machine"]
        SA1[Install text editor]
        SA2[Install Git]
        SA3[Clone 01-edu/public repo]
        SA4[Sign up for AI assistant]
        SA1 --> SA2 --> SA3 --> SA4
    end

    subgraph SetupB["Option B — College machine"]
        SB1["Log in: student / student"]
        SB2[Clone 01-edu/public repo]
        SB3[Sign up for AI assistant]
        SB1 --> SB2 --> SB3
    end

    SetupA --> P1
    SetupB --> P1

    subgraph P1["Phase 1 — Foundations: HTML and CSS"]
        direction TB
        e1["1. first-hello<br/>show/hide text"] --> e2["2. first-move<br/>CSS transforms"]
        e2 --> e3["3. first-wink<br/>interactive animation"]
        e3 --> e4["4. first-function<br/>intro to JS functions"]
    end

    P1 --> C1{{"Checkpoint:<br/>explain a CSS transform<br/>+ a button-click handler"}}
    C1 --> P2

    subgraph P2["Phase 2 — Core JavaScript Concepts"]
        direction TB
        e5["5. declare-everything<br/>variables and scope"] --> e6["6. play-with-variables<br/>data types"]
        e6 --> e7["7. i-win-arguments<br/>parameters and arguments"]
        e7 --> e8["8. good-recipe<br/>clean functions"]
        e8 --> e9["9. only-if<br/>conditionals"]
        e9 --> e10["10. listed<br/>arrays"]
    end

    P2 --> C2{{"Checkpoint:<br/>function with an argument,<br/>a condition, and a loop"}}
    C2 --> P3

    subgraph P3["Phase 3 — DOM Manipulation and Events"]
        direction TB
        e11["11. objects-around<br/>objects and properties"] --> e12["12. call-it<br/>invocation and callbacks"]
        e12 --> e13["13. class-it<br/>dynamic CSS classes"]
        e13 --> e14["14. select-then-style<br/>DOM selection and styling"]
        e14 --> e15["15. colorful-arms<br/>CSS animations"]
        e15 --> e16["16. colorful-legs<br/>advanced styling"]
    end

    P3 --> C3{{"Checkpoint:<br/>select an element and<br/>change it on interaction"}}
    C3 --> P4

    subgraph P4["Phase 4 — Advanced Concepts"]
        direction TB
        e17["17. embedded-organs<br/>nested DOM structures"] --> e18["18. glance-on-power<br/>operators and expressions"]
        e18 --> e19["19. robots-harmony<br/>multi-object state"]
        e19 --> e20["20. transform-objects<br/>object transformation"]
        e20 --> e21["21. star-forge<br/>complex animations"]
        e21 --> e22["22. the-skeleton<br/>semantic HTML"]
        e22 --> e23["23. the-smooth-operator<br/>animation timing"]
        e23 --> e24["24. JSPowered Mode<br/>capstone"]
    end

    P4 --> Done([Done: build features end-to-end<br/>HTML + CSS + JS, no template])
```

---

Haven't done the [setup](SETUP.md) yet? Do that first.
