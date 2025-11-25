# Palindrome Checker with Custom Data Structures

A Java implementation of a palindrome detection system built entirely with custom data structures including Node, LinkedList, Queue, and Stack - all implemented recursively without using Java's built-in collections.

## 🎯 Project Overview

This project demonstrates fundamental data structures and algorithms concepts by building a complete palindrome checker from the ground up. Every component is implemented from scratch using recursive algorithms, showcasing the power and elegance of recursive thinking.

## ✨ Features

- **Fully Custom Data Structures**: No built-in Java collections used
- **Recursive Implementation**: All LinkedList operations use recursion (no loops)
- **Dual Palindrome Detection Methods**:
  - Queue + Stack method (demonstrates FIFO vs LIFO comparison)
  - Stack-only method (more memory efficient)
- **Interactive Mode**: User-friendly CLI for testing custom phrases
- **Comprehensive Test Cases**: Pre-defined test suite with edge cases
- **Generic Type Support**: Works with any Comparable type (Character, Integer, String, etc.)
- **Smart Space Handling**: Correctly handles single spaces (ignored) vs multiple spaces (preserved)

## 📁 Project Structure

```
Question_1/
├── Node.java           # Basic building block for linked structures
├── LinkedList.java     # Recursive linked list implementation
├── Queue.java          # FIFO queue using LinkedList
├── Stack.java          # LIFO stack using LinkedList
└── DataAnalysis.java   # Palindrome checker (main application)
```

## 🏗️ Architecture

```
DataAnalysis
    ├── Uses Queue (FIFO)
    │   └── Uses LinkedList
    │       └── Uses Node
    └── Uses Stack (LIFO)
        └── Uses LinkedList
            └── Uses Node
```

## 🚀 How It Works

### Palindrome Detection Algorithm

1. **Input Cleaning**: Converts to lowercase, handles spaces appropriately
2. **Queue + Stack Method**:
   - Adds all characters to both Queue and Stack
   - Queue maintains original order (FIFO)
   - Stack reverses order (LIFO)
   - Compares characters one by one
3. **Stack-only Method**:
   - Pushes first half onto stack
   - Compares second half with popped elements
   - Skips middle character if odd length

### Example Flow
```
Input: "Racecar"
Clean: "racecar"

Queue: r → a → c → e → c → a → r
Stack: r ← a ← c ← e ← c ← a ← r

Compare:
Queue front: r = Stack top: r ✓
Queue front: a = Stack top: a ✓
Queue front: c = Stack top: c ✓
...
Result: PALINDROME!
```

## 💻 Usage

### Compile
```bash
javac Question_1/*.java
```

### Run
```bash
java Question_1.DataAnalysis
```

### Menu Options
1. **Interactive Mode** - Test your own words/phrases
2. **Run Test Cases** - Execute pre-defined test suite
3. **Compatibility Demo** - Show dual String/Array compatibility

### Example Interactive Session
```
PALINDROME CHECKER APPLICATION
Choose how you want to run the program:
1. Interactive mode (enter your own words/phrases)
2. Run pre-defined test cases only
3. Demonstrate LinkedList/LinkedListTest compatibility
Enter your choice (1, 2, or 3): 1

--- INTERACTIVE PALINDROME CHECKER ---
Choose an option:
1. Check a word/phrase for palindrome
2. Run pre-defined test cases
3. Exit
Enter your choice (1-3): 1

Enter a word or phrase to check: A man a plan a canal Panama
Analyzing: "A man a plan a canal Panama"

Choose analysis method:
a) Queue + Stack method (shows detailed process)
b) Stack-only method (more efficient)
c) Both methods
Enter your choice (a/b/c): a

--- QUEUE + STACK METHOD ---
Adding characters to Queue and Stack:
  Added 'a' to both structures
  Added 'm' to both structures
  ...

Comparing characters:
Queue (original) vs Stack (reversed):
  'a' vs 'a'
  'm' vs 'm'
  ...
  → All characters match! It's a palindrome!

=== FINAL RESULT ===
"A man a plan a canal Panama" is a PALINDROME!
```

## 🧪 Test Cases

The project includes comprehensive test cases:
- Simple palindromes: "racecar", "madam"
- Phrase palindromes: "A man a plan a canal Panama"
- Non-palindromes: "hello", "race a car"
- Edge cases: empty string, single character, double spaces
- Case sensitivity: "Aa", "Never odd or even"

## 🔑 Key Implementation Details

### Node Class
- Generic type supporting `Comparable` interface
- Implements `equals()` for data comparison
- Implements `compareTo()` for ordering
- Null-safe comparison methods

### LinkedList Class
- **100% Recursive**: No loops anywhere
- Operations: add, addHead, addInOrder, remove, contains
- Time Complexities:
  - addHead: O(1)
  - add: O(n)
  - remove: O(n)
  - get: O(n)

### Queue Class
- FIFO (First In, First Out)
- Operations: enqueue, dequeue, peek, isEmpty
- Enqueue at tail, dequeue from head

### Stack Class
- LIFO (Last In, First Out)
- Operations: push, pop, peek, isEmpty, clear
- Both push and pop at head for O(1) performance

### DataAnalysis Class
- Dual mode: String input or generic array
- Two palindrome checking algorithms
- Smart space handling (single vs multiple spaces)
- Verbose output for educational purposes

## 📊 Time & Space Complexity

| Operation | Time | Space |
|-----------|------|-------|
| isPalindrome (Queue+Stack) | O(n) | O(n) |
| isPalindrome (Stack-only) | O(n) | O(n/2) |
| Queue enqueue | O(n) | O(1) |
| Queue dequeue | O(1) | O(1) |
| Stack push | O(1) | O(1) |
| Stack pop | O(1) | O(1) |

## 🎓 Learning Objectives Demonstrated

- ✅ Recursive algorithm design
- ✅ Generic programming in Java
- ✅ Custom data structure implementation
- ✅ Queue (FIFO) vs Stack (LIFO) principles
- ✅ Linked list operations
- ✅ Algorithm analysis
- ✅ Test-driven development
- ✅ Clean code practices

## 🛠️ Technical Highlights

1. **No External Libraries**: Pure Java implementation
2. **Generic Type Support**: Works with any Comparable type
3. **Null Safety**: Proper null handling throughout
4. **Memory Efficient**: Stack-only method uses ~50% less space
5. **Educational Output**: Detailed step-by-step process visualization

## 📝 Code Quality

- Extensive inline documentation
- Descriptive variable names
- Clear method separation
- Comprehensive error handling
- Educational comments explaining each step

## 🤝 Contributing

This is an academic project demonstrating data structures concepts. Feel free to fork and experiment with:
- Additional data structures (Deque, Priority Queue)
- Different palindrome algorithms
- Performance optimizations
- GUI implementation

## 📄 License



## 👤 Author

Suemon Kwok 


---

**Note**: This implementation prioritizes educational clarity over performance optimization. The recursive approach and verbose output make it ideal for learning data structure concepts.
