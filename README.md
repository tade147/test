# test

from name_function import get_formatted_name
print("Enter 'q'at any time to quit.")
while True:
    first = input("\nPlease give me a first name: ")
    if first == 'q':
        break
    last = input("Please give me a last name: ")
    if last == 'q':
        break

    formatted_name = get_formatted_name(first, last)
    print("\tNearly formatted name: " + formatted_name + " .")



import unittest
from name_function import get_formatted_name

class NameTestCase(unittest.TestCase):
    """test name_function"""

    def test_first_last_name(self):
        """Can deal with name like Janis Joplin?"""
        formatted_name = get_formatted_name('janis', 'joplin')
        self.assertEqual(formatted_name, 'Janis Joplin')

unittest.main()
