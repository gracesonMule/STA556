# STA 556 — Conceptual Exam (Weeks 1–5)

**Name:** ______________________  **Date:** ______________

**Instructions:** Answer each question in 1–3 sentences. Questions test concepts, not memorized syntax. Short code fragments may be used where helpful. Each question is worth 2 points (100 total).

---

## Part I — Professional Computational Workflow (Week 1)

**1.** The course aims to move students from "I can write some Python code" to a broader capability. Describe that broader capability.

**2.** What is a GitHub Codespace, and why does the course use one as its official environment?

A remote machine that you connect to. We use it to avoid system conflicts and dependency issues.

**3.** Why should analysis code use relative paths rather than absolute paths? Give one example of a path that would break portability.

**4.** Distinguish Git from GitHub.

**5.** Describe the roles of the working directory, the staging area, and the repository in the basic Git workflow. Which commands move changes between them?

**6.** Explain why version control is a *research reproducibility* tool, not only a software engineering practice. Use the example of an estimate that changes between two dates.

**7.** What is the distinction between a Jupyter notebook and a Python module/script, and when is each most appropriate?

**8.** The course states that "your code is only one part of a computational analysis." What else matters, and how does the course repository address it?

---

## Part II — Data Types and Data Structures (Week 2)

**9.** Every Python object has three properties. Name them and briefly describe each.

**10.** Why is a Python variable better described as "a name bound to an object" than as "a box containing a value"?

**11.** Given `x = [1, 2, 3]` and `y = x`, then `x.append(4)`, what does `y` contain and why?

**12.** Distinguish *mutating* an object from *rebinding* a name, using a short example.

**13.** What question can you ask to decide whether a type is mutable or immutable? Name two types of each kind.

**14.** Explain the difference between a shallow copy and a deep copy. Why does `x = [[1, 2], [3, 4]]; y = x.copy()` still allow changes to `x[0]` to appear in `y`?

**15.** Why can mutable arguments be a hazard when writing statistical functions?

**16.** Explain why Python is described as dynamically typed yet not "untyped." Give an example.

**17.** Do type annotations make Python statically typed? State what annotations do provide.

**18.** Name the four major collection types covered, and for each give the kind of relationship it is best suited to represent.

**19.** Give one situation where a list comprehension improves code, and one where a regular loop is preferable. What principle governs the choice?

**20.** A list of dictionaries such as `[{"id": 1, "score": 82}, ...]` is described as a "bridge" to tabular data. Explain why.

---

## Part III — DataFrames, Indexing, Slicing, and Filtering (Week 3)

**21.** What are the components of a pandas DataFrame, and why does it match the rectangular datasets used in statistics?

**22.** What is the difference between `df["age"]` and `df[["age"]]`?

**23.** Why should you inspect a dataset before analyzing it? List at least three things you want to learn.

**24.** Distinguish `.loc` from `.iloc`.

**25.** A DataFrame has index labels 101, 205, 310, 412. Explain how `df.loc[205]` and `df.iloc[1]` differ in meaning even though they may return the same row.

**26.** How do endpoint rules differ between `df.iloc[1:4]` and `df.loc[101:103]`?

**27.** Explain how a Boolean condition such as `df["score"] > 80` functions as an indicator variable, and how it implements an inclusion rule.

**28.** Why must `&`, `|`, and `~` be used instead of `and`, `or`, `not` when combining conditions in pandas? Why are parentheses around each condition needed?

**29.** In `df.loc[df["score"] >= 85, ["group", "score"]]`, what does each of the two arguments specify?

**30.** What is chained assignment, why should it be avoided, and what is the preferred alternative?

---

## Part IV — Joining, Reshaping, and Missing Data (Week 4)

**31.** What is a join key? List at least three questions you should ask about keys before joining.

**32.** Explain inner, left, right, and outer joins in terms of set logic.

**33.** Why is a left join often appropriate when one table defines the study population? What happens to left rows with no match?

**34.** Why can an inner join be dangerous even when the code runs without error?

**35.** What does `indicator=True` add to a merge result, and how is it used to audit a join?

**36.** What does the `validate=` argument do in `merge()`? Give an example of an expectation it can enforce.

**37.** Two tables each have two rows for `id = 1`. What happens in a merge on `id`, and why might this be a problem?

**38.** Distinguish `merge()` from `concat()`. Why can `concat(..., axis=1)` produce incorrect results when entities must be matched by a key?

**39.** Define wide and long data. Is either format universally better?

**40.** Explain the difference between `pivot()` and `pivot_table()`. Why should you not use `pivot_table()` just to make a duplicate-key error disappear?

**41.** Give three reasons a value might be missing, including one introduced by a data transformation. Why does the reason matter?

**42.** Explain why filling missing scores with 0, or with the mean, is a statistical decision and not just a coding convenience.

---

## Part V — I/O and External Data Sources (Week 5)

**43.** What problem does the phrase "a reproducible boundary between external data and internal analysis" describe?

**44.** Why is successfully reading a CSV not proof that pandas interpreted it correctly? Name three possible ingestion problems.

**45.** Why might an ID column be better read as a string than a number?

**46.** Explain why filtering in a SQL `WHERE` clause can be preferable to loading a full table and filtering in pandas.

**47.** What is a parameterized SQL query, and why is it preferable to inserting values directly into query strings?

**48.** Nested JSON data are often not directly suitable for a DataFrame. What tool does the course use to handle this, and what does it do?

**49.** Name three issues that may arise when collecting data from web APIs, and explain why caching a raw snapshot improves reproducibility.

**50.** Compare CSV and Parquet. Give two advantages of each, and explain what "columnar" storage means for analytical workloads.

---

*End of exam.*
