# RobotMan2412's general style guide
This describes some general rules for code style in my projects.

Note: Style applies to each git repository separately, submodules do not count towards their parent repository.

# Comment style
1. Use descriptive comments (see [README.md](README.md))
2. Avoid commenting out code (to avoid visual clutter)
3. Avoid block comments (`/* comment */`) because they are hard to edit

# Brace style
Same-line braces, including if...else

### Example
```c
void function() {
    // Something happens...
    if (condition) {
        // More code.
    } else if (condition) {
        // Yet another path.
    } else {
        // Final path.
    }
}
```

# Type style
Pointer on the right.

### Example
```c
struct mystruct;

// Type description.
typedef const  char    *mytype_t;
// Type description.
typedef struct mystruct mystruct_t;

// Struct description.
struct mystruct {
    // Members go here.
};
```

# Indentation style
Try to match the place of names and assignments.
Tabs/spaces apply to the whole git repository, but not to it's submodules.

### Example
```c
// Returns a string which is allocated using malloc().
char *function() {
    // Make an empty string buffer.
    int   size   = 123;
    char *buffer = malloc(size);
    *buffer      = 0;
    
    // Add something, e.g.:
    strcat(buffer, "Hello, World!\n");
    
    return buffer;
}
```

# Other notes
- Try to describe mathematics used where possible (mainly which algorithm is used)
- If a file differs from the guide, make sure to avoid merge conflicts by asking before refactoring
- Try to keep indentation on empty lines for editing convenience (some IDEs remove empty line indentation)
