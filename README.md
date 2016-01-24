# harmonix
Coding challenge

1.) Write a Django view for user registration that doesn’t rely on contrib.auth. It should have a simple model that holds a username, email, and password. Presume the registration is coming from a JSON POST; no form or display logic is necessary. Instead write a set of unit tests to test your code.

2.) Write a set of two Django views that aggregate user stats across all users in a wildly successful game. One view receives a JSON POST event each time one of the following things happens in game: sword swung, spell cast, item picked up. Another view returns the number of times each of those events has been triggered, in JSON. Assuming a heavy load and a small amount of acceptable lag on reads, show or discuss how you would handle maintaining speed for reads and writes while handling a large volume of traffic.

3.) If you were asked to write a function to remove duplicates from an list of integers, what questions would you ask before you started coding? Describe in general terms the solutions you would give depending on the answers to those questions, and analyze the performance characteristics of your solutions in time and memory.

1) How long is the list? 
If the list is short, I can solve the problem by putting each unique integer into a hash and checking future intergers against the keys to that hash. 
If the list is large, I would try to make sure that my hash is implemented efficiently, and make choices about how my data is stored to minimize the size of the hash.

2) Does my output need to preserve the order of the original list? 
If yes, I would store each new unique number in a new list instead of in a hash. 


