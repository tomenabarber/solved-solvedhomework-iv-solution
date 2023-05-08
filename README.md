Download Link: https://assignmentchef.com/product/solved-solvedhomework-iv-solution
<br>
PROBLEM DESCRIPTIONNot all programs running on a system at any given time have the same behavior. There may be one or two that are directly interacting with a human being, while others are downloading information from a network. Some larger systems would also be occasionally saving data onto long­term secondary storage in the background. Simulating process scheduling for such a varied set of processes would be much simplified if they could all be represented in a uniform and simple way. Similarly, there are many different ways for an operating system to choose which of these several processes to run. If we wish a simulation to adequately compare these various policies to each other, it would be much simplified if all the scheduling policies could be represented in a uniform way. Object­oriented programming with inheritance is a very useful programming technique, because it allows an interface to interact with a base class, while the details of the operations are implemented in derived classes. INHERITANCE DEFINED FOR THIS ASSIGNMENT Ŝ and Ŝ A new object type appearing this week is the &#x7;, that represents any peripheral device that a process may choose to interact with. For this assignment, there will be the disk, the network, and the console (keyboard and screen). For simplicity, all of these devices will appear to have the same behavior from the point of view of the process ­­ something that takes time to respond. The keyboard and the screen are folded into one object modeling the possibility that a user types at the keyboard in response to seeing something on the screen. One additional ‘cpu’ object is declared in this category only for simplifying an interface elsewhere. The method &#x7;śś accomplishes the same thing as &#x15; in the previous assignment. It is simply generalized to apply to work for any of the derived classes. Ŝ and Ŝ Three different sorts of processes are defined for this exercise. A &#x6; represents a program that uses relatively large bursts of CPU, occasionally separated by some access to a disk, either for data or virtual memory. A &#x7; process represents a program that fetches data from a network and stored it onto the disk. And one process type is defined to simply  with a user at the console. The simulation will work with a mixture of these types of processes. Ŝ The Scheduler object is now used as the basis for four different scheduling policies ­­ two which had been seen before, and two more, which will be discussed in more detail below. ASSIGNMENT DETAILS Most of the work for this assignment will be simply adapting the previous assignment to the new objectoriented environment. 1) The array of Processes has been changed to be an array of pointers to Processes, to allow the use of the derived classes for Process. The function prototypes for &#xb;, śśś&#x16; and &#x7;śś have been changed for you, but the use of these variables will require some minor editing. In most cases, it will be nothing more than replacing Ŝ with Şʴ to follow the pointer before accessing an object member. 2) When a process is done executing, instead of returning a character representing its next state, it will return a pointer to a Device object. If it wishes to access a peripheral, it will indicate which one. If it still has more work to do with the CPU, it will return a pointer to that object. If it is done, it may return a NULL pointer. The &#x16;śś&#x16; code will then need to properly handle this change. 3) The only “new” code will be the completion of the two new objects defined in Ŝ, which will use a binary search tree implemented in Ŝ. Priority scheduling will simply use the process identifier (
) for its choice, choosing the process with the largest value to be the highest priority. We will provide this ordering with a binary search tree, which has the ability to add any value, and remove the largest. Preemptive priority scheduling will also choose the process that has the highest process identifier. It only differs from priority scheduling in that the highest priority process will be allowed to run as soon as it arrives. This can be effectively simulated simply by changing the behavior of the  method. The credit for this new code will depend in part on the clarity and simplicity of the solution, as well as its correctness. HINT: The implementation is very much simplified in both cases by using a recursive function with a reference parameter for any tree node that needs to be changed. those that are currently ready to run.