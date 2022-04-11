# diagrams-markdown-mermaid

Include diagrams in your Markdown files with Mermaid

### IDE Support

Jetbrains IDEA enable Markdown mermaid extension:  

```Prefences > Languages & Frameworks > Markdown > Markdown extensions > Mermaid``` 

Visual Studio Code install Markdown mermaid support plugin:  
[VS Code Mermaid Support Plugin](https://marketplace.visualstudio.com/items?itemName=bierner.markdown-mermaid)

## Flowchart

### Example 1: Get Started Top-Down Diagram

```mermaid
flowchart TD
    A --> B
    A --> C
    B --> D
    C --> D
```

`flowchart TD` means `flowchart top-down`.

### Example 2: Get Started Left-Right diagram

```mermaid
flowchart LR
    A --> B
    A --> C
    B --> D
    C --> D
```

`flowchart LR` means `flowchart left-right`.

### Example 3: Block Name

```mermaid
flowchart
    A[Start Block] --> B[Block1]
    A --> C[Block2]
    B --> D[End Block]
    C --> D
```

The diagram `default` direction is `Top-Down`.

### Example 4: Line Length

```mermaid
flowchart TD
    A[Start Block] --> B[Block1]
    A --> C[Block2]
    B ---> D[End Block]
    C --> D
    
```

The line length of three-dash `---` is longer than the two-dash `--` one. And the least number of 
the dash must be 2.

### Example 5: Conditional Branch

```mermaid
flowchart TD
    A --> B{Is it Friday?}
    B -- Yes --> C[Enjoy your weekend!]
    B -- No --> D[Enjoy your workday!]
    C ---> E[Enjob your life!]
    D ---> E
```

The conditional block is marked as `Block_Label{}`.

## Sequence Diagram

### Example 6: Get Started
```mermaid
sequenceDiagram
    participant A
    participant B
    A ->> B: request something
    B ->> A: response something
    A ->> B: put something
    B ->> B: rander something
    participant C
    A ->> B: post something
    B ->> C: request something
    C ->> C: rander something
    C ->> B: 200 OK
    C ->> A: response 200 OK
```

- The `participant Label` represents a participant component of the sequence diagram.
- A line between participants follows the rule: `Label ->> Label: Comment above line`

## Reference Links

- https://github.blog/2022-02-14-include-diagrams-markdown-files-mermaid/
- https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/creating-diagrams