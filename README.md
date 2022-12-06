# A template repository for Advent of Code in Kotlin

## Project Structure

```tree
src
├── main
│   ├── kotlin
│   │   └── days                    <- Solution here
│   │       ├── Day.kt
│   │       ├── Day00.kt
│   │       └── Day01.kt
│   └── resources                   <- Real input here
│       └── day00.txt
└── test
    ├── kotlin
    │   └── days                    <- Test result here
    │       ├── Day00Test.kt
    │       └── Day01Test.kt
    └── resources                   <- Test input here
        └── day00.txt
```

Your solution files should go in `src/main/kotlin/days`, copying the format of `Day00.kt`.
Similarly, if you want to test your input, create a test class in `src/test/kotlin/days/`,
copying `Day00Test.kt` and replacing the result with the result for the test input.

For solution files, make sure to change the argument on class declaration line when calling
the constructor.

For test files, make sure you are creating an instance of the correct day's class.

## Running

Three run options:

To run a single day:

```bash
./gradlew run --args="19"
```

To run the entire month:

```bash
./gradlew run --args="-m"
```

To run the latest day (highest):

```bash
./gradlew run --args="-l"
```

Additionally, "-t" can be added to the arguments to time your solutions. e.g.

```bash
./gradlew run --args "-l -t"
```

## Helpers

The project contains a few helpers to make life easier, both for solving code
and for generating project files.

Firstly, a gradle task has been provided to create all of the required files
for the *next* day of AoC. *Note: This works by looking at existing files,
and incrementing the day number of the highest existing day.*

You can run this with

```bash
./gradlew newDay
```

Additional helpers within the code allow for reading in common input types.
Within each day, you can access the input file with the property `inputList`,
which is a `List<String>`. Additional helpers exist for reading a list of
integers, with `inputIntList`, or space-separated values with `inputSplitList`.

## Credits

Base taken from [hughjdavey](https://github.com/hughjdavey/aoc-kotlin-starter).
I used this last year, and tweaked slightly to my own needs.
