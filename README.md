# Self study for Week 7 (CI/CD Basics)

## Install

```bash
python -m pip install pytest
```

## Task 1

Run the following on the pycharm built-in terminal:

```bash
pytest -v
```

You can see that `test_simple_function2` is failed. Fix the code (line 2 in `main.py`) to make the test case pass.

When it's fixed, push the change to GitHub to see the GitHub Actions in action.

## Task 2

If you uncomment `test_complex_function` in `test_main.py`, you can see that the test case is most likely failed.
This is because the behaviour of `complex_function` is non-deterministic (depending on `random_function`).

Such non-deterministic behaviour is not uncommon in real-world software system.
How can we test such non-deterministic behaviour? Think about this. (No need to implement anything)

Answer - it said to "submit in repository", so this is the same answer as in Blackboard, but submitted "in repository"

If a function returns "random" or non-deterministic results then we can run it many times enough that it forms a predictable "average" of results. i.e. for a coin flip if flipped enough it will eventually give 50/50 true false results (give or take an error margin).

The more we run it the smaller the error margin as we're taking a greater average. That's how we could test non-deterministic behaviour.

I want to add that I did uncomment test_complex_function but didn't include the file in the commit for task 2 as I didn't want to break the auto marker, which I assume is looking for all tests passing to check the correctness of q1.
