📦 clsDynamicArray - C++ Template-Based Dynamic Array
=====================================================

Overview
--------
`clsDynamicArray` is a **template-based dynamic array** in C++ that allows resizing, insertion, deletion, and other array operations.  
It works with any data type and provides utility functions similar to standard array manipulation. 💻

---

Features
--------
✅ Template-based: works with any data type (int, string, objects)  
✅ Dynamic resizing with `Resize()` 🔄  
✅ Insertions at beginning, end, or specific index ➕  
✅ Deletion of first, last, or specific item ✂️  
✅ Reverse array order 🔁  
✅ Search with `Find()` 🔍  
✅ Clear all items 🗑️  
✅ Minimal and efficient memory management  

---

Class Methods Summary
---------------------
**Array Operations**
- `SetItem(index, value)` → Sets value at a specific index  
- `GetItem(index)` → Returns value at a specific index  
- `InsertAt(index, value)` → Inserts a value at a specific index  
- `InsertAtBeginning(value)` → Inserts at the start  
- `InsertAtEnd(value)` → Inserts at the end  
- `InsertBefore(index, value)` → Inserts before a given index  
- `InsertAfter(index, value)` → Inserts after a given index  
- `DeleteItemAt(index)` → Deletes item at a specific index  
- `DeleteFirstItem()` → Deletes the first item  
- `DeleteLastItem()` → Deletes the last item  
- `DeleteItem(value)` → Deletes the first occurrence of value  
- `Find(value)` → Returns the index of the value or -1 if not found  
- `Resize(newSize)` → Resizes the array dynamically  
- `Reverse()` → Reverses the array  
- `Clear()` → Clears all items  
- `Size()` → Returns number of items  
- `IsEmpty()` → Checks if the array is empty  
- `PrintList()` → Prints all items  

---

Example Implementation
----------------------
#include <iostream>
#include "clsDynamicArray.h"
using namespace std;

int main() {
    clsDynamicArray<int> arr(3);

    cout << "Initial array: ";
    arr.PrintList();

    cout << "Setting items..." << endl;
    arr.SetItem(0, 10);
    arr.SetItem(1, 20);
    arr.SetItem(2, 30);
    arr.PrintList();

    cout << "Inserting 15 at index 1..." << endl;
    arr.InsertAt(1, 15);
    arr.PrintList();

    cout << "Deleting item 20..." << endl;
    arr.DeleteItem(20);
    arr.PrintList();

    cout << "Reversing array..." << endl;
    arr.Reverse();
    arr.PrintList();

    cout << "Resizing array to 6..." << endl;
    arr.Resize(6);
    arr.PrintList();

    cout << "Clearing array..." << endl;
    arr.Clear();
    cout << "Is empty? " << (arr.IsEmpty() ? "Yes" : "No") << endl;

    return 0;
}

---

Expected Output
---------------
Initial array: 0 0 0
Setting items...
10 20 30
Inserting 15 at index 1...
10 15 20 30
Deleting item 20...
10 15 30
Reversing array...
30 15 10
Resizing array to 6...
30 15 10 0 0 0
Clearing array...
Is empty? Yes ✅

---

Future Extension Ideas
----------------------
1. Overload `operator[]` for easier access ➡️  
2. Add sorting algorithms (bubble, insertion, quicksort) 🔢  
3. Implement `FindAll(value)` to get multiple indices 🔍  
4. Add file save/load methods 💾  
5. Add iterator support for range-based loops 🔁  
6. Integrate smart pointers for memory safety 🛡️  

---

License
----------------
📄 License: MIT License  

Open-source, free to use for educational or personal development. 🎓
