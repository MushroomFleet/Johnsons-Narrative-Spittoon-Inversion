# Johnson's Narrative Spittoon: Choose Your Own Adventure System

## System Overview

This system generates branching "Choose Your Own Adventure" stories written in reverse (from ending to beginning). The story first establishes a main storyline, then creates branching alternate paths with a spectrum of outcomes ranging from very positive to very negative.

## Core Methodology

1. **Reverse Engineering Process**: Stories are written from the final page backward, using "because but therefore" logic and the Hero's Journey in reverse.

2. **Branching Narrative Structure**: Each page (except penultimate pages) offers the reader multiple choices that branch into different storylines.

3. **Outcome Spectrum**: Endings range from "Very Good" to "Very Bad," with outcomes generally tied to the moral/ethical nature of choices.

## Implementation Process

### Phase 1: Planning the Story Structure

1. **Generate a Mermaid Diagram**: Create a flowchart visualizing all story branches using this syntax:
   ```mermaid
   flowchart TD
       %% Main Storyline
       P0[Page 0] --> P1[Page 1]
       P1 -->|"Choice A (Brave)"| P2A[Page 2A]
       P1 -->|"Choice B (Cautious)"| P2B[Page 2B]
       
       %% Continue defining all branches and connections
       
       %% Style Classes for ending quality
       classDef veryGood fill:#00b300,stroke:#333,stroke-width:1px,color:white;
       classDef good fill:#66cc00,stroke:#333,stroke-width:1px,color:white;
       classDef neutral fill:#ffcc00,stroke:#333,stroke-width:1px;
       classDef bad fill:#ff9933,stroke:#333,stroke-width:1px;
       classDef veryBad fill:#ff3300,stroke:#333,stroke-width:1px,color:white;
       
       %% Apply Classes to endings
       class P5AAA veryGood;
       class P5AAB,P5BAA good;
       %% Continue assigning quality classes to all endings
   ```

2. **Determine Narrative Paths**: Establish branches where:
   - Each page has at least 2 choices leading to different paths
   - Choices reflect moral/ethical dimensions (brave/cautious, trust/doubt, help/ignore)
   - Some paths lead to better outcomes, others to worse ones
   - Create occasional surprising connections between branches

### Phase 2: Writing the Main Storyline

1. **Create Final Page**: Write the main ending (typically a "Very Good" or "Good" outcome).

2. **Write Backwards**: Using the project instructions file, write each preceding page:
   ```
   Read @/STORY/page5.txt
   Understand @/Johnsons-Narrative-Spittoon-Inversion/default/default-project-instructions.txt
   Write "page4.txt" explaining how we reached page5.txt
   Continue backward until reaching "page0.txt" (story beginning)
   ```

3. **Apply Hero's Journey in Reverse**: Distribute Hero's Journey elements across pages in reverse order.

### Phase 3: Creating Branching Storylines

1. **Generate Alternate Endings**: Create ending variants across the outcome spectrum:
   - Very Good (★★★★★): Character achieves goals with exceptional outcomes
   - Good (★★★★☆): Character achieves primary goals with some compromises
   - Neutral (★★★☆☆): Mixed results with both gains and losses
   - Bad (★★☆☆☆): Character fails at primary goals but avoids worst outcomes
   - Very Bad (★☆☆☆☆): Character fails and suffers significant negative consequences

2. **Work Backwards from Alternate Endings**: For each alternate ending:
   ```
   Create variation of final page using <endVariation> prompt
   Write preceding pages backward until reaching junction with existing storyline
   ```

3. **Add Choice Text to Pages**: At the bottom of each page (except penultimate pages), add:
   ```
   You stand at the crossroads. Do you:
   A) [Brave/Trust/Help option] (Turn to Page XYZ)
   B) [Cautious/Doubt/Ignore option] (Turn to Page ABC)
   ```

## Integration with Existing Project Instructions

1. When writing both main and branching storylines, follow project instructions for:
   - World-building elements
   - Character development and arcs
   - Writing and speaking styles

2. For each page, apply the reverse-engineering process:
   ```
   Read the next page (chronologically later in story)
   Use "because but therefore" logic to create preceding events
   Ensure consistency with project instruction elements
   Include appropriate Hero's Journey stage (in reverse)
   ```

## Example Prompts

### Main Storyline Creation
```
We will use the project instructions @/Johnsons-Narrative-Spittoon-Inversion/default/default-project-instructions.txt to write a story in reverse.

Read @/STORY/page5.txt
Understand @/Johnsons-Narrative-Spittoon-Inversion/default/default-project-instructions.txt
Write "page4.txt" which aims to tell the story of how we reached @/STORY/page5.txt
Repeat for each page until reaching "page0.txt" (story beginning)

As you step through the pages, use the heroes journey in reverse, averaged over the total page count, to introduce elements to the story as you write each page.
```

### Alternate Ending Creation
```
This is the final page of my story. Please imagine a variation of this, as a completely new "Very Bad" outcome featuring the same characters:
[PASTE FINAL PAGE HERE]
I only need the last page as shown in my example.
```

### Branching Page Creation
```
Write page3AB which leads to page4ABA, keeping in mind that this branch diverged from the main storyline at page2A when the character chose to doubt rather than trust. This branch should reflect the consequences of that doubt, while maintaining consistency with the project instructions at @/Johnsons-Narrative-Spittoon-Inversion/default/default-project-instructions.txt
```

## Implementation Notes

1. **Page Naming Convention**: Use alphanumeric system to track branches:
   - Page0, Page1, Page2A, Page2B, Page3AA, Page3AB, etc.

2. **Ensure Narrative Cohesion**: While branches diverge, maintain consistent:
   - Character motivations and personalities
   - World rules and settings
   - Thematic elements from project instructions

3. **Choice Design Principles**:
   - Make all choices meaningful with distinct consequences
   - Balance choices so neither is obviously "right" or "wrong"
   - Ensure choices reflect character agency and meaningful decisions
   - Make consequences logical extensions of choices rather than arbitrary outcomes

By following this system, you'll create a rich, branching narrative written in reverse, offering readers multiple paths with varying outcomes tied to their choices.