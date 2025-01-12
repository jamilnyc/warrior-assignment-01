# Warrior Assignment

## Overview

This is a Java assignment to practice some fundamental concepts like

* Basic Object-Oriented Programming (OOP)
* Exception handling
* File I/O
* Collections and Looping

The basic premise is a text-based simulation of "Warriors" that fight each other.

## Specification

### Input

Your program will process an input plain text file.

The file will have commands that either create a warrior or make them fight.

The first word on each line of the file is the command, followed by necessary input for the command.

Here is an example:

```text
Warrior Adam 15
Warrior Barry 40
Warrior Charlie 30
Fight Adam Barry
Fight Barry Charlie
Fight Barry Adam
```

The command `Warrior` is followed by the `name` (String) of the warrior and their `strength` (integer).
This command should create a `Warrior` object with the given `name` and `strength`.
A Warrior is _uniquely identified_ by their `name`.

The command `Fight` is followed by the names of two Warriors (two Strings).
This command should simulate a fight between the two given Warriors.
The warrior with the higher strength wins, and their strength is reduced by an amount equal the weaker warrior's strength.
The weaker warrior dies, and their strength becomes 0.

In the above example, after the first fight, Barry wins and has 40-15 = 25 `strength`. Adam dies and has 0 strength.

After the second fight, Charlie wins and has 30-25 = 5 strength, while Barry dies.

### Output

At the beginning of your program simply output:

```text
Welcome to the Warrior Fighting Simulation!
```

Everytime a new `Warrior` is created, output:

```text
Adam was born with 15 strength
Barry was born with 40 strength
Charlie was born with 30 strength
```

When a `Fight` occurs, output the result of the fight.

```text
Barry defeats Adam
Charlie defeats Barry
Fight Cancelled: Both combatants are dead
```

At the end of the program, when all fights are finished, output the warriors again:

```text
=== WARRIORS ===
Adam is dead
Barry is dead
Charlie has 5 strength
```

### Assumptions

You can assume the following to simplify your logic:

* The input file will be well-formatted and only have valid commands.
* The commands will always have valid data (String and integers)
* Only existing warriors will fight each other
* Warriors will never fight themselves

### Extra Credit

Update your program so that it works even if all the [assumptions](#assumptions) are false.