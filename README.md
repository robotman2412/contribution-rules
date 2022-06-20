# RobotMan2412's contribution rules
These are hard rules you must follow if you want to contribute to my projects.
If you don't, I will not accept your pull requests or issues.

## Categories
The rules fall into the following categories:
1. Be nice to eachother
2. Respect code style
3. Don't edit without permission
4. Be descriptive

# 1. Be nice to eachother
Don't intentionally anger people.
That's it.

Most people won't like it if you obsessively correct their grammar and spelling, so keep that in mind.

Note: This includes rule bending and "but technically the rules say so and so".

# 2. Respect code style
Most projects will have an implicit (or sometimes excplicit) style guide.
If you don't follow it, your contribution is likely to get rejected.

A general style guide to assume for my projects can be found [here](style-guide.md).

Note: Try not to mix tabs and spaces in one file and/or project.

# 3. Don't edit without permission
This rule mainly applies to people with merge privilege.

When you edit someone's code without telling them, it could easily create headaches for them.
Try to avoid editing without asking people for permission in their areas.

Example: If MrNamN is in charge of documentation, ask them before you start editing and request their review in your pull request.

# 4. Be descriptive
This is one of, if not the most important rule.

It is of critical importance that your comments be descriptive and well placed.
Comments must state what the code does to achieve which goal.
Avoid comments which spell out exactly what the line does (e.g. "Increment counter XYZ.")

### Good example:
```c
// Sets the mode for XYZ to new_mode and double-checks whether that is posssible.
// Returns true on success, false otherwise.
bool set_mode(mode_t new_mode) {
    
    // Check whether the new mode is valid.
    if (is_it_possible(new_mode)) {
        
        // The mode is valid
        the_mode = new_mode;
        printf("Mode set to %d\n", new_mode);
        return true;
    } else {
        
        // The mode is not valid.
        printf("Error: Invalid mode %d\n", new_mode);
        return false;
    }
}
```
This is good code because:
- Comments aren't literally translating their subjects.
- The function description says what to expect.
- Comments describe, in easily readable format, what is going on.
- There's some empty lines so it's easy on the eyes.

### Bad example:
```c
// Sets the mode.
bool set_mode(mode_t new_mode) {
    if (is_it_possible(new_mode)) {
        // Sets the_mode to new_mode.
        the_mode = new_mode;
        
        return true;
    } else {
        // Prints error.
        printf("Error\n");
        return false;
        
    }
}
```
This is bad code because:
- There's a comment missing.
- The function description is merely a translation of it's name.
- The comments literally translate the next line.
- The empty lines are not well placed.

