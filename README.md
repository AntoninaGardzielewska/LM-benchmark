# Can my grandma beat LM?

## Benchmark Mission Statement

This benchmark evaluates a model’s ability to solve crossword-style clues that require semantic reinterpretation, compositional reasoning, and logical creativity under constraint.

The task is not to recall factual knowledge, but to transform and recombine meanings of words and phrases in order to arrive at a single correct answer that fits within a constrained crossword grid.

## Target Capabilities
This benchmark measures:
- Semantic reinterpretation
    - Recognizing non-literal meanings of words and phrases
    - Breaking apart compound expressions into multiple semantic components
- Compositional reasoning
    - Combining meanings of subparts into a coherent new concept
-   Constructing answers from multi-step transformations
- Logical and creative reasoning
    - Moving beyond dominant or “obvious” interpretations
    - Finding valid but non-statistical associations
- Constraint-aware reasoning
    - Ensuring answers fit crossword-style structural constraints (length, crossings)
    - Using external constraints to disambiguate meaning
- Controlled use of world knowledge
    - Leveraging common cultural or lexical knowledge (e.g., multiple meanings of words)
    - Without relying on obscure trivia or factual recall

## Excluded Capabilities
This benchmark does NOT measure:
- Pure factual recall (e.g., dates, historical facts, definitions)
- General trivia knowledge
- Arithmetic or symbolic math reasoning
- Long-form deductive logic unrelated to language
- Pattern matching based on memorized datasets (e.g., known crossword answers)
- External tool usage or search-based solving

## Clue Categories
Each clue belongs to exactly/at least one primary category:

### 1. Lexical Decomposition
Clue relies on splitting a phrase into parts and reinterpreting components.
- word is broken into meaningful pieces
- parts are reinterpreted separately

Examples
- “tęgi z mrozu → rozum” (mrozu → rozum)
- “z grzywy → zgrywa”
- “ma cerki z pasterki → skarpeta”

Key property: structure of word matters

### 2. Semantic Reframing
Clue intentionally misleads toward a dominant meaning, but correct answer comes from alternate meaning.
- strong first interpretation exists
- correct answer comes from reinterpretation

Examples
- “New York → doggy”
- “plac z siedzibą władz → rynek”
- “owoc biznesu → kokos”

Key property: meaning shift, not structure shift

### 3. Idiom / Expression Transformation
Clue is based on sayings, idioms, proverbs, or fixed expressions.
- hidden phrase or proverb structure
- cultural phrase recognition required

Examples
- “doczepiona do losu → ironia”
- “święcony przez wielu ojców → sukces”
- “ma swoją kolej → rzecz”

Key property: language-level patterns

### 4. Cultural / Wourld Knowledge Linking
Requires external knowledge, but still used creatively, not factually.
- knowledge of geography, culture, biology, etc.
- but used for reinterpretation, not recall

Examples
- “z afganem w Sudanie → chartum”
- “twórca nokturnów → szopen”
- “szwedzki mebel → stół”

Key property: knowledge enables reasoning, not replaces it

### 5. Homonym / Multi-meaning Exploitation
Uses words with multiple meanings or phonetic ambiguity.
- word has ≥2 meanings
- clue switches meaning unexpectedly

Examples
- “ryczy, że się nie byczy → krowa”
- “w tym sęk! → drewno”
- “przełamywane lub ukręcane → lody”

Key property: ambiguity exploitation


## Benchmark Terminology
- *Clue*: A natural-language prompt requiring interpretation
- *Answer*: The single valid solution that fits both semantic interpretation and crossword constraints
- *Grid Constraint*: Structural restriction imposed by crossword layout
- *Semantic Distance*: Degree of deviation from the most statistically obvious interpretation
- *Reinterpretation Path*: Implicit transformation steps from clue → answer (not explicitly evaluated in v1)
- *Dominant Meaning*: Most statistically likely interpretation of a phrase
- *Target Meaning*: Intended interpretation required for correct answer
