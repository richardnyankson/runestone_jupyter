=====================
This Is A New Project
=====================

.. Here is were you specify the content and order of your new book.

.. Each section heading (e.g. "SECTION 1: A Random Section") will be
   a heading in the table of contents. Source files that should be
   generated and included in that section should be placed on individual
   lines, with one line separating the first source filename and the
   :maxdepth: line.

.. Sources can also be included from subfolders of this directory.
   (e.g. "DataStructures/queues.rst").

SECTION 1: Introduction
:::::::::::::::::::::::

Congratulations!   If you can see this file you have probably successfully run the ``runestone init`` command.  If you are looking at this as a source file you should now run ``runestone build``  to generate html files.   Once you have run the build command you can run ``runestone serve`` and then view this in your browser at ``http://localhost:8000``

This is just a sample of what you can do.  The index.rst file is the table of contents for your entire project.  You can put all of your writing in the index, or  you can include additional rst files.  Those files may even be in subdirectories that you can reference using a relative path.
The link below is a Youtube video about Data Science.




   .. youtube:: aGu0fbkHhek





Section 2: Links
::::::::::::::::

Runestone uses the ``restructuredText`` (rst) markup language.  We chose this over markdown largely because rst is extensible.  Nearly all of the basic markup tasks are already handled by restructuredText.  You should check out the docs for the basics of restructuredText (link below). Our extensions are all for the interactive elements.  One key hint about restructuredText:  Its like **Python** -- *indentation matters!*

* `restructuredText Docs <http://docutils.sourceforge.net/rst.html>`_
* `Runestone Docs <https://runestone.academy/runestone/static/authorguide/index.html>`_
* Join the discussion on our `Google Group <https://groups.google.com/forum/#!forum/runestone_instructors>`_
* Tell us about problems on `Github <https://github.com/RunestoneInteractive/RunestoneComponents>`_



SECTION 3: Sample Directives
::::::::::::::::::::::::::::

ActiveCode
----------

.. activecode:: codeexample1
   :coach:
   :caption: This is a caption

   print("My first program adds a list of numbers")
   myList = [2, 4, 6, 8, 10]
   total = 0
   for num in myList:
       total = total + num
   print(total)

Multiple Choice
---------------

.. mchoice:: question1_2
    :multiple_answers:
    :correct: a,b,d
    :answer_a: red
    :answer_b: yellow
    :answer_c: black
    :answer_d: green
    :feedback_a: Red is a definitely one of the colors.
    :feedback_b: Yes, yellow is also correct.
    :feedback_c: Remember the acronym...ROY G BIV.  B stands for blue.
    :feedback_d: Yes, green is one of the colors.

    Which colors might be found in a rainbow? (choose all that are correct)

These are just two of the many interactive components for writing online course materials.  You can see examples of all of them `On our Example Page <http://interactivepython.org/runestone/static/overview/overview.html>`_

Now feel free to modify this file to start creating your own interactive page.


Section 4: Theme
:::::::::::::::::::

You can add your own CSS or JS files to every page of a book by modifying ``setup.custom_css_files`` or ``setup.custom_js_files`` in conf.py.

If you want to do more significant changes to the theme, you should copy the files you wish to modify from
the runestone/common/project/template/sphinx_bootstrap to a directory like ``_templates/``. Then make sure
the ``templates_path`` points to them in your conf.py.

conf.py:

.. code::

    templates_path = ["_templates"]


Section 5: Resources
:::::::::::::::::::::

The following will provide resources that will enable one to read more about data science.

* Carnegie Mellon `Practical Data Science Lecture <https://www.datasciencecourse.org/lectures/>`_

Section 6: ActiveCode
::::::::::::::::::::::
ActiveCode
--------------------------

.. activecode:: ac_ex_content
   :language: python

   Fix the following code so that it **always** correctly adds ``two`` numbers.

   * Your solution must use the parameters a and b
   ~~~~
   def add(a,b):
       return 4

   ====
   # TODO: add unit tests

   Section 7: more
   :::::::::::::::
   Adding more features to the book


Section 7: Codelens
::::::::::::::::::::::
Implementation of Codelens
------------------------------
.. codelens:: cl_ex1

   # from: http://www.ece.uci.edu/~chou/py02/python.html
   def InsertionSort(A):
       for j in range(1, len(A)):
           key = A[j]
           i = j - 1
           while (i >= 0) and (A[i] > key):
               A[i+1] = A[i]
               i = i - 1
           A[i+1] = key

   input = [8, 3, 9, 15, 29, 7, 10]
   InsertionSort(input)
   print(input)

Section 8: JupyterLite
::::::::::::::::::::::::::
Integrating jupyter notebook
--------------------------------
.. jupyterlite:: NumPy_Basics.ipynb
   :width: 100%
   :height: 800px
   :prompt: Try JupyterLite!
   :prompt_color: #00aa42
