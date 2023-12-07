======================
 Python Primer
======================

----------------------
 Topics
----------------------

- Python's REPL
    - Data types
        - str (string)
        - int (integer)
        - float
        - list
        - dict (dictionary)
        - set
        - tuple
    - conditionals
       - if / elif / else
    - loops
        - for
        - while
        - loop control
            - break
            - continue
- The built-in interactive help

~~~~

------------------------
 Python's REPL
------------------------

 Read, Execute, Print, and Loop

.. code:: python
    $ python3
    >>> "Hello World!"
    'Hello World!'
    >>>

~~~~

-----------------------
 Strings
-----------------------

    - Strings in python are surrounded by either single quotation marks, or
      double quotation marks.
    - Strings are indexed and you can access individual characters or "slices"
      of the strings by using it's indexes.

.. code:: python
    >>> mystring = "This is my string. There are many like it, but this one is mine."
    >>>
    # This is my...
    # 0123456789...

Subscripting a string
``mystring[<start>:<end>[:<step>]]``

.. code:: python
    >>> mystring[0]
    'T'
    >>> mystring[0:4]
    'This'
    # zeroth position up to, but not including the fourth position.
    >>> mystring[-1]
    '.'
    # One character from the end of the string
    >>> mystring[::2]
    'Ti sm tig hr r aylk t u hsoei ie'
    # Start at T(index 0) select every second character
    >>> type(mystring)
    <class 'str'>
    >>> len(mystring)
    64
    >>> mystring[64]
    Traceback (most recent call last):
    File "<stdin>", line 1, in <module>
    IndexError: string index out of range

 Escaping special characters
-----------------------------
You can escape special characters that may interrupt a complete string with a
backslash.

>>> "He said, \"I dont want to go to the store!\""
'He said, "I dont want to go to the store!"'

~~~~

-----------------------
 Integers
-----------------------

    - a number that is not a fraction; a whole number.

.. code:: python

    >>> myint = 5
    >>> myint
    5
    >>> type(myint)
    <class 'int'>
    >>> myint + 5
    10
    >>>

Operators:
    +   Addition
    -   Subtraction
    *   Multiplication
    /   Division
    %   Modulos (return the remainder of division)
    **  Exponentation
    //  Floor division
      

~~~~

-----------------------
 Float
-----------------------

    - stores numbers that are not integers because they include a fraction

.. code:: python

    >>> myfloat = 14.5
    >>> type(myfloat)
    <class 'float'>
    >>> myint + myfloat
    19.5
    >>>

Operators:
    +   Addition
    -   Subtraction
    *   Multiplication
    /   Division
    %   Modulos (return the remainder of division)
    **  Exponentation
    //  Floor division

- Math between an Integer and a Float will always result in a Float

~~~~

-----------------------
 List
-----------------------

    - Lists are used to store multiple items in a single variable.
    - They can be changed, mutable.

This is a bulleted list
    * one
    * two
    * three

This is a Python list

.. code:: python
    >>> mylist = ['one','two','three']
    >>> mylist
    ['one','two','three']
    >>> type(mylist)
    <class 'list'>

Lists, like strings, can be subscripted

.. code:: python
    >>> mylist[1]
    'two'
    >>> mylist[:2]
    ['one', 'two']
    >>> mylist[3]
    Traceback (most recent call last):
      File "<stdin>", line 1, in <module>
    IndexError: list index out of range
    >>>
    
~~~~

-----------------------
 Dictionary
-----------------------

Dictionaries and lists share the following characteristics:

    - Both are mutable.
    - Both are dynamic. They can grow and shrink as needed.
    - Both can be nested. A list can contain another list. A dictionary can
      contain another dictionary. A dictionary can also contain a list, and
      vice versa.

Dictionaries differ from lists primarily in how elements are accessed:

    - List elements are accessed by their position in the list, via indexing.
    - Dictionary elements are accessed via keys.

.. code:: python
    >>> mydict = {'key1': 'value1', 'key2': 'value2'}
    >>> mydict
    {'key1': 'value1', 'key2': 'value2'}
    >>> mydict['key1']
    'value1'
    >>> type(mydict)
    <class 'dict'>
    >>> mydict['key3']
    Traceback (most recent call last):
      File "<stdin>", line 1, in <module>
    KeyError: 'key3'
    >>>

  
~~~~

-----------------------
 Tuple
-----------------------

    - A tuple is a collection which is ordered and unchangeable or immutable.
    - Tuples are subscriptable

.. code:: python
    >> mytuple = ("apple", "banana", "cherry", "apple", "cherry")
    >>> mytuple[1]
    'banana'
    >>> mytuple[5]
    Traceback (most recent call last):
      File "<stdin>", line 1, in <module>
    IndexError: tuple index out of range
    >>> mytuple[1:4]
    ('banana', 'cherry', 'apple')
    >>> mytuple[0] = "Apple"
    Traceback (most recent call last):
      File "<stdin>", line 1, in <module>
    TypeError: 'tuple' object does not support item assignment
    >>>




~~~~

-----------------------
 Set
-----------------------

    - Set items are unordered, unchangeable, and do not allow duplicate values.
    - Sets are not subscriptable

.. code:: python
    >>> myset = {'one', 'two', 'three', 'two'}
    >>> myset
    {'three', 'one', 'two'}
    >>> type(myset)
    <class 'set'>
    >>> myset.discard('one')
    >>> myset.add(1)
    {'three', 1, 'two'}

~~~~

=======================
Conditionals
=======================

-----------------------
 if / elif / else
-----------------------

Conditionals provide the ability to create decision trees in an application.

    if condition boolean:
        do this
    elif some other condition boolean:
        # There can be a number of ``elif`` statements in the tree
        do that
    else:
        just do this this if neither of the others is true|false

.. code:: python

    >>> tootsie_pop_licks = 252
    >>> if tootsie_pop_licks == 3:
    ...     print("The Owl says 3, 3 licks to get to the center of a Tootsie Roll Tootsie Pop ")
    ... elif tootsie_pop_licks == 252:
    ...     print("Perdue University says it take 252 licks to get to the center of a Tootsie Roll Tootsie POP")
    ... else:
    ...     print("We may never know how many licks it takes to get to the center of a Tootsie Roll Tootsie POP")
    ...
    Perdue University says it take 252 licks to get to the center of a Tootsie Roll Tootsie POP

`Tootsie Roll Tootsie Pop Experiment <https://tootsie.com/howmanylick-experiments>`_

Keywords:
    - in    : test if character is in a string or if a item is in a list, set, or tuple 
    - not   : check for the condition to be False
Equality:
    - == equal to
    - != not equal to
    - >  greater than
    - <  less than
    - <= less than equal to
    - >= greater than equal to

~~~~

=======================
Loops
=======================
-----------------------
 for
-----------------------

The ``for`` loop will iterate over any iterable object, these include
    - strings
    - lists
    - tuples
    - sets
    - dicts: will use the keys by default

.. code:: python
    for item in mylist:
        # do something with the item
        pass

    for tup in enumerate(mylist):
        # do something with the item
        index = tup[0]
        value = tup[1]
        pass

    for index, value in enumerate(mylist):
        # unpacks the tuple into separate items
        pass

    for idx in range(len(mylist)):
        # access items with mylist[idx]


Keywords:
    - in: for every item in this string, list, tuple, set, or dict keys do
      these instructions 
Functions:
    - enumerate(iterable) produces a 2-tuple with the index and the value at that index.
    - range([start=0,] end[, step=1]) produces an iterable that will 
~~~~

-----------------------
 while
-----------------------

The ``while`` loop will keep executing a set of instructions as long as it's
condition is met.

.. code:: python
    # Find all the i's
    mystring = "This is my string. There are many like it, but this one is mine."
    start = 0
    pos = 0

    while pos != -1:
        pos = mystring.find('i', start)
        start = pos + 1
        if pos == -1:
            continue 
        print(mystring[pos], "found at", pos)

~~~~

-----------------------
loop control
-----------------------
    - continue : Skip any instruction left in the loop and move to the next
                 item in the iterable or test of the condition.
    - break    : Stop the loop immediately and continue on with the rest of the
                 application.

~~~~

=======================
 Help
=======================

.. code:: python
    >>> help()
    >>> help(str)
    >>> help(list)
    >>> help(dict)
    >>> help(set)
    >>> help(for)

~~~~

=======================
Bonus Rounds
=======================
-----------------------
I/O
-----------------------

 Take user input
-----------------------
You can take user input with theh builtin ``input`` function

.. code:: python
    >>> input("Show me the money: ")
    Show me the money: 10000
    10000
    >>>

 Print output
-----------------------
The builtin function ``print`` can be used to print data to a file like object.
It can take any number of variables to display.

.. code:: python
    print(arg1[, arg2..], sep=" ", end="\n", file=sys.stdout, flush=False)

~~~~

 Reading and Writing files
---------------------------
Reading and writing files can be accomplished with the builtin function ``open()``
You can open a file in different modes

open can be used to generate a file like object or as a context manager.

.. code:: python
    >>> # open a file for reading
    >>> ro_file_pointer = open('path/to/file', 'r')
    >>> # open a file for writing
    >>> w_file_pointer = open('path/to/file', 'w')
    >>> # get contents as a string
    >>> contents = ro_file_pointer.read()
    >>> # get contents as a list
    >>> content_list = ro_file_pointer.readlines()
    >>> # write content to file
    >>> w_file_pointer.write("the content")
    >>> # be responsible with the files
    >>> close(w_file_pointer)
    >>> close(ro_file_pointer)
    >>> # context manager style
    >>> with ('path/to/file', 'r') as ro_fp:
    ...     contents = ro_fp.read()
    ...
    >>> # ro_fp is closed as soon as the script is out scope of the ``with`` 

All the modes to open a file in

    'r'       open for reading (default)
    'w'       open for writing, truncating the file first
    'x'       create a new file and open it for writing
    'a'       open for writing, appending to the end of the file if it exists
    'b'       binary mode
    't'       text mode (default)
    '+'       open a disk file for updating (reading and writing)


