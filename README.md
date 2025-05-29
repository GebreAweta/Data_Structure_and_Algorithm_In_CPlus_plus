 📕        Brief explanation for each implementation in Our doubly linked list assignment:


🎁 1. struct Node

         Defines the structure of each node in the doubly linked list.
         
         data: holds the actual value.
         
         prev: points to the previous node.
         
         next: points to the next node.
         

🎁 2. Node* head = NULL;

     Global pointer that always points to the first node in the list.
     
     If it's NULL, the list is empty.

🎁 3. insertAtPosition(int data, int position)

      Inserts a node with the given data at a specified position (1-based index).
      
   Handles:
   
         Inserting at the beginning (position 1).
         
         Inserting between nodes.
         
        Displays an error if the position is invalid.

✅ 4. insertAtBeginning(int data)

     Calls insertAtPosition(data, 1) to insert a node at the very beginning of the list.

✅ 5. insertAtEnd(int data)

         Traverses the list to the end and inserts the node as the last element.
         Handles empty list as a special case.

✅ 6. deleteAtPosition(int position)

        Deletes the node at the given position.
    Handles:
    
      Deleting the first node (updates head).
      
      Deleting a middle or last node (relinks pointers).
      
      Invalid positions (prints error).

      
✅ 7. deleteFirstNode()

        Deletes the first node in the list by calling deleteAtPosition(1).
        
✅ 8. deleteLastNode()

      Deletes the last node in the list.
      
      Traverses to the last node.
      
      Adjusts the prev node’s next pointer to NULL.
      

✅ 9. getValueAtPosition(int position)

        Retrieves and prints the value at the given position.
        
        Traverses the list to that index.
        
      If invalid, shows an error.
      

✅ 10. displayList()

      Traverses from head to the end and prints all node values.
      
      Shows the list in forward order.
      
✅ 11. displayReverse()

        Traverses to the last node, then prints values by going backward using prev pointers.
        
        Displays the list in reverse order.
        

✅ 12. searchValue(int value)

       Searches the list for a given value.
       
       If found, prints the position.
       
      If not found, displays a message.
      
✅ 13. showMenu()

       Prints a menu of available operations.
       
       Used inside main() to provide user interaction.
       

✅ 14. main() Function

       Acts as the main user interface for testing the list:
        
       Displays welcome message and group info.

      Loops and takes user input to call the appropriate function.
     
      Exits on choice 11.

    The out put looks


![image](https://github.com/user-attachments/assets/0ff1d275-cf48-4baf-b8ed-80155c028414)   ![image](https://github.com/user-attachments/assets/908c84ec-8971-45d5-b3a8-ee86a1c963aa)










         📕       Here’s a brief explanation for each implementation in  circular doubly linked list program:

🎯 1. struct CNode

        Defines a node in the circular doubly linked list.
        
       int data: Stores the actual data.
       
       CNode* prev: Pointer to the previous node.
       
       CNode* next: Pointer to the next node.
       

🎯  2. CNode* createNode(int value)

      Creates and returns a new node with the given value.
      
      Allocates memory dynamically.
      
      Initializes next and prev to NULL.

      

🎯  3. void insertAtBeginning(int data)

       Inserts a node at the start of the list.
       
       If list is empty, creates a self-referencing node.
       
       Otherwise, links the new node before the current head and updates pointers to maintain the circular structure.
       
🎯  4. void insertAtEnd(int data)

        Inserts a node at the end of the list.
        
        If the list is empty, delegates to insertAtBeginning().
        
        Otherwise, adds the new node after the last node (tail) and connects it to head.
        

🎯 5. void insertAtPosition(int pos, int data)

         Inserts a node at a specific position (1-based index).
         
         If position is 1, inserts at beginning.
         
         Traverses to the pos-1 node and inserts the new node after it.
         
        Validates bounds to avoid inserting in invalid positions.
        

🎯 6. void deleteFromBeginning()

        Deletes the first node from the list.
        
        If the list is empty or has only one node, handles edge cases.
        
        Otherwise, removes the head node and updates head and tail pointers.
        

🎯 7. void deleteFromEnd()

        Deletes the last node in the list.
        
        Handles empty list and single-node list cases.
        
        Otherwise, updates the second-last node to become the new tail and connects it back to the head.
        

🎯 8. void deleteFromPosition(int pos)

       Deletes a node at a specific position.
       
       If position is 1, deletes from beginning.
       
       Otherwise, traverses to the node at pos, and updates adjacent pointers to remove it.
       

🎯 9. void display()

        Displays the entire list in a circular format.
        
        Starts from head and loops through until it comes back to head.
        
        Outputs the values with a "↔" style to show two-way links.
        

🎯 10. void showMenu()

        Displays the user menu options for operations:
        
        Insert, delete, display, and exit options.

🎯 11. main()

          The entry point of the program.
          
          Shows university and group info.
          
          Continuously shows the menu and takes user input to perform operations on the circular doubly linked list using a switch-case.
          
The out put Looks



![image](https://github.com/user-attachments/assets/5d46bb78-5115-4692-903e-0c39af17be79)





📚Here’s a brief explanation of each part of queue implementation using a singly linked list in C++:

✅ 1. struct Node

         Defines a node of the linked list used to implement the queue.

        
         int data: Stores the value.
         
         Node* next: Points to the next node in the queue.

         
✅ 2. Global Pointers

        Node* front = NULL;
        
        Node* rear = NULL;
        
        These maintain the start and end of the queue:
        
        front: Points to the first node (next to be dequeued).
        
        rear: Points to the last node (where new data is enqueued).
        

✅ 3. bool isEmpty()

        Checks if the queue is empty:
        
        return front == NULL;

        
✅ 4. void enqueue(int value)

         Adds a new value at the rear of the queue.
         
         Creates a new node.
         
         If the queue is empty, both front and rear point to the new node.
         
         Otherwise, the current rear’s next points to the new node, and rear is updated.
         

✅ Outputs the enqueued value.


📙 5. void dequeue()

         Removes the value at the front of the queue.
         
         Checks if the queue is empty (underflow).
         
         Otherwise, removes the node pointed to by front and moves front to the next node.
         
         If the queue becomes empty after deletion, sets rear to NULL.
         

✅ Outputs the dequeued value.

📙 6. void peek()

         Displays the front element of the queue without removing it.
         
         If empty, shows a message.
         
         Otherwise, shows front->data.
         

📙 7. void display()

        Displays all elements of the queue from front to rear.
        
        Traverses the queue from front to NULL, printing each data.
        

📚 8. main()

       The main function:
       
             Displays your university and group member info.
             
             Shows a menu with 5 options:
             
             Enqueue
             
             Dequeue
             
             Peek
             
             Display
             
             Exit

📚 Summary of Operations:
            Operation	Function	Description
            
            Enqueue	enqueue()	Add element at rear of queue
            
            Dequeue	dequeue()	Remove element from front
            
            Peek	peek()	View front element without removing
            
            Display	display()	Print all elements in the queue
            
            Exit	return 0;	End the program

![image](https://github.com/user-attachments/assets/5d34948e-2d5e-4c01-8a1f-3dcff398b2f1)

 
