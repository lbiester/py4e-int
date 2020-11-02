Write Code Questions
---------------------
#.
  .. tabbed:: list_writeMyList

      .. tab:: Question

          Fix the 5 syntax errors in the code below so that it runs. It should print the length
          of ``myFirstList`` and print the result of ``myFirstList * 3``. Then it should set
          ``mySecondList`` to the concatenation of ``myFirstList`` and a list containing ``321.4``.
          Then it should print the value of ``mySecondList``.

          .. activecode:: list_writeMyListq
              :nocodelens:

              myFirstList = [12,"ape"13]
              print(len(myFirstList)
              print(myfirstList * 3)
              mySecondList = myFirstList + [321.4
              print(mySecondList

      .. tab:: Answer

          .. activecode:: list_writeMyListA
              :optional:

              1. List elements are separated by commas
              2. Parentheses need to be in pairs (the print statement is missing the closing ")")
              3. Python is case sensitive, use myFirstList
              4. Brackets also need to be in pairs
              5. Parentheses again need to be in pairs.
              ~~~~
              myFirstList = [12,"ape",13]
              print(len(myFirstList))
              print(myFirstList * 3)
              mySecondList = myFirstList + [321.4]
              print(mySecondList)

#.
    .. activecode::  list_writeItemsq
        :nocodelens:

        Fix 5 syntax errors in the code below so that it runs and prints the contents of ``items``.
        ~~~~
        def itemLister(items):
            items[0] = "First item'
            items[1] = items0]
            items[2] = items[2] + 1
           print items

        itemLister([2,4,6 8])

#.
    .. tabbed:: list_writeAvg

        .. tab:: Question

            Complete the code on lines 4 and 5 so that the function returns the average of
            a list of integers.

            .. activecode::  list_writeAvgq
                :nocodelens:

                def gradeAverage(aList):
                    sum = 0
                    for num in aList:

                    average =
                    return average

                aList = [99, 100, 74, 63, 100, 100]
                print(gradeAverage(aList))

        .. tab:: Answer

            .. activecode:: list_writeAvgA
                :optional:

                After the for loop is initialized, add ``num`` to the ``sum``.
                Outside of the loop, calculate the average by dividing ``sum`` by the length of the list.
                ~~~~
                def gradeAverage(aList):
                    sum = 0
                    for num in aList:
                        sum = sum + num
                    average = sum/len(aList)
                    return average

                aList = [99, 100, 74, 63, 100, 100]
                print(gradeAverage(aList))

#.
    .. activecode:: list_write23q

        Assign the value of the item at index 3 of ``l`` to "200"
        ~~~~
        l = ["hi", "goodbye", "python", "106", "506"]

        =====

        from unittest.gui import TestCaseGui

        class myTests(TestCaseGui):

           def testOne(self):
              self.assertEqual(l[3], "200", "Testing that l[3] is 200")

        myTests().main()

#.
  .. tabbed:: list_writePlant

      .. tab:: Question

          Using indexing, retrieve the string ‘willow’ from the list and assign that to the variable plant.

          .. activecode:: list_writePlantq

              data = ['bagel', 'cream cheese', 'breakfast', 'grits', 'eggs', 'bacon', [34, 9, 73, []],
                     [['willow', 'birch', 'elm'], 'apple', 'peach', 'cherry']]


              =====

              from unittest.gui import TestCaseGui

              class myTests(TestCaseGui):

                 def testOne(self):
                    self.assertEqual(plant, "willow", "Testing that plant was assigned to the willow.")

              myTests().main()

      .. tab:: Answer

          .. activecode:: list_writePlanta
              :optional:

              Since ``willow`` is in the last element of ``data``, access that last element using [-1].
              Now ``willow`` is in the first element of ``dataLast``, use [0] to access the first element.
              Finally, ``willow`` is the first element in ``trees``. Access the first element [0] and
              assign to ``plant``.
              ~~~~
              data = ['bagel', 'cream cheese', 'breakfast', 'grits', 'eggs', 'bacon', [34, 9, 73, []],
                     [['willow', 'birch', 'elm'], 'apple', 'peach', 'cherry']]

              dataLast = data[-1]
              trees = dataLast[0]
              plant = trees[0]

#.
    .. activecode:: list_write5q

        Write a function called ``countWords`` that returns a count of how many words in the pased list, ``lst``, have length 5.
        ~~~~
        def countWords(lst):

        ====
        from unittest.gui import TestCaseGui

        class myTests(TestCaseGui):

            def testOne(self):
                self.assertEqual(countWords(["hello", "hi", "good morning", "three", "kitty"]),3,'Tested countWords on input ["hello", "hi", "good morning", "three", "kitty"]')
                self.assertEqual(countWords(["two", "three", "four", "five", "six", "seven"]),2,'Tested countWords on input ["two", "three", "four", "five", "six", "seven"]')
                self.assertEqual(countWords(["these", "those", "there"]),3,'Tested countWords on input ["these", "those", "there"]')
                self.assertEqual(countWords(["the", "an", "a"]),0,'Tested countWords on input ["the", "an", "a"]')


        myTests().main()

#.
  .. tabbed:: list_writeChop

      .. tab:: Question

          Write a function called ``chop`` that takes a list ``lst`` and modifies it, removing the first and last elements.

          .. activecode:: list_writeChopq

              def chop(lst):

              ====
              from unittest.gui import TestCaseGui

              class myTests(TestCaseGui):

                  def testOne(self):
                      self.assertEqual(chop([1,2,3,4,5]),[2,3,4],"Tested chop on input [1,2,3,4.5]")
                      self.assertEqual(chop([1,3,5,7,9,10]),[3,5,7,9],"Tested chop on input [1,3,5,7,9,10]")
                      self.assertEqual(chop([2,9]),[],"Tested chop on input [2,9]")

              myTests().main()

      .. tab:: Answer

          .. activecode:: list_writeChopa
              :optional:

              Use del to remove the first (0th) element and to remove the last (-1st) element.
              Then return the list.
              ~~~~
              def chop(lst):
                  del lst[0]
                  del lst[-1]
                  return(lst)

#.
    .. activecode:: list_writeMiddleq

        Write a function called ``middle`` that takes a list ``lst`` as its argument and
        returns a new list that contains all but the first and last elements.
        ~~~~
        def middle(lst):

        ====
        from unittest.gui import TestCaseGui

        class myTests(TestCaseGui):

            def testOne(self):
                self.assertEqual(middle([1,2,3,4,5]),[2,3,4],"Tested middle on input [1,2,3,4.5]")
                self.assertEqual(middle([1,3,5,7,9,10]),[3,5,7,9],"Tested middle on input [1,3,5,7,9,10]")
                self.assertEqual(middle([2,9]),[],"Tested middle on input [2,9]")

        myTests().main()

#.
  .. tabbed:: list_writeSum

        .. tab:: Question

            Sum all the elements in the list ``lst`` up to but not including the first even number.

            .. activecode:: list_writeSumq

                def sumUntilEven(lst):

                ====
                from unittest.gui import TestCaseGui

                class myTests(TestCaseGui):

                    def testOne(self):
                        self.assertEqual(sumUntilEven([1,2,3,4,5]),1,"Tested sumUntilEven on input [1,2,3,4.5]")
                        self.assertEqual(sumUntilEven([1,3,5,7,9]),25,"Tested sumUntilEven on input [1,3,5,7,9]")
                        self.assertEqual(sumUntilEven([2,4,6,7,9]),0,"Tested sumUntilEven on input [2,4,6,7,9]")

                myTests().main()


        .. tab:: Answer

            .. activecode:: list_writeSuma
                :optional:

                First, create a total variable to keep the sum, since sum is a built-in function and cannot be used as a variable name.
                Then, create a variable to iterate through elements. Use a while loop to filter the list, checking that
                the element is not beyond the list's capacity and that it is not even. If the element meets those conditions,
                increment the total and the iterator to move on to the next element. Finally, return the total.
                ~~~~
                def sumUntilEven(lst):
                    total = 0
                    element = 0
                    while element < len(lst) and lst[element] % 2 != 0:
                        total = total + lst[element]
                        element += 1
                    return total


#.
    .. activecode::  list_writeReverseq
        :nocodelens:

        Write a function called ``reverse`` that returns the reverse of a passed list.
        ~~~~
        ====
        from unittest.gui import TestCaseGui

        class myTests(TestCaseGui):

            def testOne(self):
                  self.assertEqual(reverse([1,2,3,4,5]),[5,4,3,2,1],"Tested reverse on input [1,2,3,4.5]")
                  self.assertEqual(reverse([1,3,5,7,9]),[9,7,5,3,1],"Tested reverse on input [1,3,5,7,9]")
                  self.assertEqual(reverse([2,4,6,7,9]),[9,7,6,4,2],"Tested reverse on input [2,4,6,7,9]")


        myTests().main()
