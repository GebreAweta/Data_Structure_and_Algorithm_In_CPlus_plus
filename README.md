 Brief explanation for each implementation in Our doubly linked list assignment:


🔷 1. struct Node
Defines the structure of each node in the doubly linked list.

data: holds the actual value.

prev: points to the previous node.

next: points to the next node.

🔷 2. Node* head = NULL;
Global pointer that always points to the first node in the list.
If it's NULL, the list is empty.

🔷 3. insertAtPosition(int data, int position)
Inserts a node with the given data at a specified position (1-based index).
Handles:

Inserting at the beginning (position 1).

Inserting between nodes.

Displays an error if the position is invalid.

🔷 4. insertAtBeginning(int data)
Calls insertAtPosition(data, 1) to insert a node at the very beginning of the list.

🔷 5. insertAtEnd(int data)
Traverses the list to the end and inserts the node as the last element.
Handles empty list as a special case.

🔷 6. deleteAtPosition(int position)
Deletes the node at the given position.
Handles:

Deleting the first node (updates head).

Deleting a middle or last node (relinks pointers).

Invalid positions (prints error).

🔷 7. deleteFirstNode()
Deletes the first node in the list by calling deleteAtPosition(1).

🔷 8. deleteLastNode()
Deletes the last node in the list.

Traverses to the last node.

Adjusts the prev node’s next pointer to NULL.

🔷 9. getValueAtPosition(int position)
Retrieves and prints the value at the given position.

Traverses the list to that index.

If invalid, shows an error.

🔷 10. displayList()
Traverses from head to the end and prints all node values.
Shows the list in forward order.

🔷 11. displayReverse()
Traverses to the last node, then prints values by going backward using prev pointers.
Displays the list in reverse order.

🔷 12. searchValue(int value)
Searches the list for a given value.

If found, prints the position.

If not found, displays a message.

🔷 13. showMenu()
Prints a menu of available operations.
Used inside main() to provide user interaction.

🔷 14. main() Function
Acts as the main user interface for testing the list:

Displays welcome message and group info.

Loops and takes user input to call the appropriate function.

Exits on choice 11.

The out put looks
![image](https://github.com/user-attachments/assets/0ff1d275-cf48-4baf-b8ed-80155c028414)
![image](https://github.com/user-attachments/assets/908c84ec-8971-45d5-b3a8-ee86a1c963aa)

