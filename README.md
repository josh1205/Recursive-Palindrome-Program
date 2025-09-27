# String Palindrome Checker and Reversal Tool

A C++ application that checks whether strings are palindromes and demonstrates both iterative and recursive string reversal algorithms. This project showcases fundamental algorithm design patterns and recursive problem-solving techniques.

## Project Overview

This program implements three core string manipulation algorithms: palindrome detection using a two-pointer technique, iterative string reversal, and recursive string reversal. The interactive command-line interface allows users to test multiple strings in a single session, making it useful for understanding algorithmic concepts and comparing different implementation approaches.

## Features

- **Palindrome Detection**: Two-pointer algorithm to efficiently check if a string reads the same forwards and backwards
- **Dual Reversal Implementations**:
  - Iterative approach using loop-based concatenation
  - Recursive approach using substring manipulation
- **Interactive Interface**: Continuous loop allowing multiple string tests without restarting
- **User-Friendly Output**: Clear formatting showing original string and both reversal methods
- **Case Sensitivity**: Preserves original case for accurate palindrome checking

## File Structure

```
└── palindrome.cpp    # Complete implementation with all algorithms
```

## Core Algorithms

### 1. Palindrome Detection
**Function**: `bool palindrome(const string& s)`

**Algorithm**: Two-pointer technique
- Starts with pointers at both ends of the string
- Compares characters moving inward
- Returns false immediately if mismatch found
- Returns true if all characters match

**Time Complexity**: O(n/2) → O(n)  
**Space Complexity**: O(1)

**Implementation Highlights**:
- Efficient early termination on mismatch
- No additional memory allocation needed
- Const reference parameter for performance

### 2. Iterative String Reversal
**Function**: `string printReversel(const string& s)`

**Algorithm**: Loop-based concatenation
- Iterates through string from end to beginning
- Builds new string by appending characters in reverse order

**Time Complexity**: O(n)  
**Space Complexity**: O(n) for the result string

### 3. Recursive String Reversal
**Function**: `string printIterReverse(const string& s)`

**Algorithm**: Divide and conquer recursion
- Base case: String of length ≤ 1 returns itself
- Recursive case: Reverses substring and appends first character
- Demonstrates recursive thinking and call stack usage

**Time Complexity**: O(n)  
**Space Complexity**: O(n) for recursion stack

**Key Concept**: Each recursive call processes one character, building the result from the inside out as the call stack unwinds.

## Technical Skills Demonstrated

### Algorithm Design
- **Two-pointer technique**: Efficient in-place comparison
- **Iterative algorithms**: Traditional loop-based approach
- **Recursive algorithms**: Breaking problems into smaller subproblems
- **Base case identification**: Critical for recursion termination

### C++ Programming
- **String manipulation**: Using `substr()`, `at()`, `length()`
- **Pass by const reference**: Optimizing parameter passing
- **Control flow**: While loops, conditionals, early returns
- **I/O handling**: `getline()` for multi-word input, `cin.ignore()` for buffer clearing
- **Function decomposition**: Breaking program into logical, reusable components

### Problem-Solving Patterns
- **Comparison of approaches**: Iterative vs recursive solutions
- **Edge case handling**: Single character and empty strings
- **User experience design**: Interactive, repeatable program flow

## Compilation

```bash
g++ -std=c++11 palindrome.cpp -o palindrome_checker
```

## Usage

```bash
./palindrome_checker
```

### Example Session

```
please enter string: racecar
racecar is a palindrome 
The Rec-reverse of "racecar" is "racecar"
The Iter-reverse of "racecar" is "racecar"

Do you wish to continue (y or Y for yes; n or N for no? y

please enter string: hello world
hello world is a not palindrome 
The Rec-reverse of "hello world" is "dlrow olleh"
The Iter-reverse of "hello world" is "dlrow olleh"

Do you wish to continue (y or Y for yes; n or N for no? n
```

## Algorithm Analysis

### Palindrome Detection Efficiency
The two-pointer approach is optimal for palindrome checking:
- Only examines n/2 characters in the worst case
- No extra space needed beyond two integer indices
- Early termination saves operations on non-palindromes

### Iterative vs Recursive Reversal

| Aspect | Iterative | Recursive |
|--------|-----------|-----------|
| **Readability** | More verbose | More elegant/concise |
| **Memory** | Single result string | Result string + call stack |
| **Performance** | Slightly faster | Function call overhead |
| **Concept** | Straightforward looping | Demonstrates recursion |

### Space-Time Tradeoffs
Both reversal methods have O(n) time complexity, but the recursive version uses additional stack space proportional to the input length, making it less efficient for very long strings.

## Learning Outcomes

This project demonstrates proficiency in:

### Algorithmic Thinking
- Recognizing when to use two-pointer techniques
- Understanding recursion mechanics and call stack behavior
- Comparing algorithmic approaches for the same problem
- Analyzing time and space complexity

### Data Structures
- String manipulation and traversal
- Understanding stack memory in recursive calls
- Building new data structures from existing ones

### Programming Practices
- Writing reusable, single-purpose functions
- Using const correctness for safety and optimization
- Proper input handling and buffer management
- Creating interactive, user-friendly programs

### Problem Decomposition
- Breaking complex problems into simpler functions
- Identifying base cases and recursive patterns
- Testing edge cases (empty strings, single characters)

## Design Decisions

### Function Naming
- `printReversel` and `printIterReverse` clearly distinguish the two reversal methods
- Descriptive names indicate both purpose and implementation type

### Parameter Design
- Const reference parameters prevent unnecessary copying
- Returns new strings rather than modifying input (pure functions)

### User Interface
- Multi-word string support via `getline()`
- Continue/exit option for efficient testing
- Clear output formatting for easy comparison

### Algorithm Selection
- Two-pointer for palindrome: Most efficient approach
- Both reversal types included: Educational value in comparing approaches

## Potential Enhancements

While this is a complete academic project, potential extensions could include:
- Case-insensitive palindrome checking
- Ignoring spaces and punctuation in palindrome detection
- Performance timing comparisons between iterative and recursive approaches
- Additional string algorithms (anagrams, permutations)

## Notes for Reviewers

This project showcases:
- **Algorithmic versatility**: Multiple approaches to similar problems
- **Recursive thinking**: Understanding how problems decompose into smaller instances
- **Efficiency awareness**: Choosing appropriate data structures and algorithms
- **Clean code practices**: Well-commented, single-responsibility functions

The comparison between iterative and recursive implementations demonstrates understanding of different programming paradigms and their tradeoffs, a key skill in data structures and algorithm analysis.

---

*Developed as part of coursework in Data Structures and Algorithm Analysis*
