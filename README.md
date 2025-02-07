# Elixir Enum.each and throw Exception

This example demonstrates a potential pitfall when using the `throw` keyword within `Enum.each` in Elixir.  The `throw` will halt execution, but code *after* the `if` but *within* the `Enum.each` function will still run before the exception is handled. 

To see the issue in action, run the `bug.exs` file. Observe that even after the `throw` is executed, "After if" will be printed to the console before the exception is raised.