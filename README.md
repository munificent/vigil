Vigil is a *very safe* programming language, and an entry in the [January 2013 PLT Games competition](http://www.pltgames.com/competition/2013/1).

Many programming languages claim to take testing, contracts and safety seriously, but only Vigil is *truly* vigilant about not allowing code that fails to pass programmatic specifications.

## Syntax and semantics

Vigil is very similar to Python with the minor proviso that you must provide a `main()` function which will be automatically called for you.

Infinitely more important than mere syntax and semantics are its addition of **supreme moral vigilance**. This is similar to contracts, but less legal and more medieval.

### The `implore` statement to beseech your needs

Often, a function will require that parameters have certain desirable properties. A function in Vigil can state what it requires by using `implore`:

```
def square_root(n):
    implore n >= 0
    return math.sqrt(n)
```

If a caller fails to provide valid arguments, it is *wrong* and must be punished.

### The `swear` statement to state what you provide in return

If a good caller meets its obligations, the onus is thus on you to fulfill your end of the bargain. You can state the oaths that you promise to uphold using `swear`:

```
def fib(n):
    if n < 2:
        result = n
    else:
        result = fib(n - 1) + fib(n - 2)

    # fib() never returns negative number.
    swear result >= 0
    return result
```

If a function fails to uphold what it has sworn to do, it is *wrong* and must be punished.

### Unhandled exceptions

It goes without saying that any function that throws an exception which isn't caught is *wrong* and must be sent to Purgatory until such wrongs can be righted.  This preserves the sanctity of the code.

## Runtime vigilance

This is where Vigil sets itself apart from weaker languages that lack the courage of their convictions. When a Vigil program is executed, Vigil itself will monitor all oaths (implorations and swears) that have been made. If an oath is broken, the offending function (the caller in the case of `implore` and the callee in the case of `swear`) *will be duly punished.*

How?

**Simple: it will be deleted from your source code.**  Meanwhile, it will be added to the global variable Purgatory until higher authorities fix the offending code or purged.

The only way to ensure your program meets its requirements to absolutely forbid code that fails to do so. With Vigil, it will do this for you *automatically*. After enough runs, Vigil promises that all remaining code meets its oaths.

## Usage

Vigil is a command-line executable. Pass it the path to a file to run:

```
$ ./vigil example/hello.vg
```

The "example" directory has some to get you started.

## FAQ

### Is this serious?

Eternal moral vigilance is no laughing matter.  When creating a data paradise for the programming high-priests, one cannot allow sloppiness or favor.  The perfect application for the language is towards the creation of a data ecosystem, where many snippets have to interact with each other and the implications of running incorrect code could be disastrous--even collapse a society.  In such case, like attending Church, one wants to be *clean* when one's frottage.

### But isn't a language that deletes code crazy?

No, wanting to keep code that demonstrably has bugs *according to its own specifications* is crazy. What good could it possibly serve? It is corrupted and must be cleansed from your codebase.

Vigil will do this for you automatically.

### Vigil deleted a function. Won't that cause the functions that call it to fail?

It would seem that those functions appear to be corrupted as well. Run Vigil again and it will take care of that for you. Several invocations may be required to fully excise all bugs from your code.  A list of those functions of ill-repute will be noted in future versions.
