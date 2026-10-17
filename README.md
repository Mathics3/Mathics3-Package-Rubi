# Introduction

> [!WARNING]
> This Mathics3 package is under development.

This package is a copy of version 4.17 of [Rubi](https://rulebasedintegration.org), a Rule-based integration package written for WMA, customized for Mathics3.

Mathics-core branch dependency: https://github.com/Mathics3/mathics-core/tree/at-most-one-TimeConstrained

# Setting up and Running

To develop

```
        $ git clone git@github.com:Mathic3/Mathics3-Package-Rubi.git
        $ cd Mathics3-Package-Rubi
        $ mathics3
```

```mathematica
	    Mathics3 10.0.1
	    Running on linux CPython 3.14.6 (main, Jul 11 2026, 11:12:13) [GCC 13.3.0]
	    using SymPy 1.13.3, mpmath 1.3.0, numpy 2.5.2, cython 3.2.8, scipy 1.17.1, skimage 0.26.0

	    Copyright (C) 2011-2026 The Mathics3 Team.
        This program comes with ABSOLUTELY NO WARRANTY.
        This is free software, and you are welcome to redistribute it
        under certain conditions.
        See the documentation for the full license.

        Quit by evaluating Quit[] or by pressing CONTROL-D.

        In[1]:= << Rubi.wl
        Loading Rubi 4.17.3.0 will take a minute or two. In the future this will take less than a second.
        ...
        Patching With[]...

        Loading /home/ark/git/mathics/rubi/ShowStepFormatting.wl...
        SetDelayed::write: Tag HoldPattern in HoldPattern[Dist[u_, v_, _]] is Protected.
        SetDelayed::write: Tag HoldPattern in HoldPattern[Int[expr_, x_]] is Protected.


        Out[1]= None

        In[2]:= << Test.wl
        Out[2]= None

        In[3]:= TestRubi["SanityCheck.wl"]
        Rubi 4.17.3.0 Integration Test Results
        on the problems in "SanityCheck.wl"
        ...
        Hold[IntegrationTestProgram`Private`Int[1 / x ^ (5 / 2), x]]
        Result optimal and 1 fewer steps used.
        Optimal(type 2, 9 leaves, 1 step): -2 / (3 x ^ (3 / 2))
        Result(type 2, 9 leaves, 0 steps): -2 / (3 x ^ (3 / 2))
        .
        Summary of Integration Test Results
        25 integration problems
        A - 24 optimal antiderivatives
        B - 0 valid but suboptimal antiderivatives
        C - 0 unnecessarily complex antiderivatives
        D - 0 unable to integrate problems
        E - 1 integration timeouts
        F - 0 invalid antiderivatives

        Rubi results 1.00 times size of optimal antiderivatives on average.
        Out[3]= None
```

Sanity test is a small subset of [Rubi's Integration Test Suite](https://rulebasedintegration.org/testProblems.html).
