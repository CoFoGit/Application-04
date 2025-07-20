# Application-04
Abarrass 5346980 RTS summer 2025
Q1: Binary semaphores can store a value like a mutex and in binary case hold the value 0 or 1 and will retain that value until the button is otherwise released, this keeps new values from affecting the semaphore meaning only one instance of the button "exists" at a time, counting semaphores increment with each press which can stock up presses for instances of multiple inputs being needed but are subject to overflow with lagging and rapid presses.

Q2: Rapidly adjusting the potentiometer across the threshold would create a large amount of LED and console tasks to execute which is helped by the counting semaphore as it is more prepared to handle multiple instances of task execution so that no missed threshold crosses are missed, a binary semaphore would have to activate all of these tasks simultaneously and can miss out on rapid threshold passes which could leave out critical information of operation along with operation tasks.

Q3: If we remove mutexes for the purposes of output, we can get corrupted and interleaved prints that do not convey clear messages. Mutexes are important because it allows resources to be shared in order to avoid issues of corruption. When information needs to be logged accurately, ensuring that interleaving and corruptions don't occur clears up misunderstandings and incorrect information being collected.

Q4: Task priorities depending on individual CPU usage can affect the responsiveness of our program, like if a long printing task is given higher priority than a routine led flickering, then the led could suffer if the print task takes up too much CPU uptime. In my code, the button manual intervention task pre-empts my uptime led that blinks every second which sometimes shifts the timing which fortunately did not affect my results. 

Q5: vTaskDelay introduces small amounts of drift which can be improved upon with the implementation of vTaskDelayUntil because we can more accurately configure the delay involved with tasks.

Q6: Synchronization is a priority because in a highly radioactive and toxic environment, prolonged and excessive exposure to containments could impact the life and well-being of any exposed individuals caught in the containment facility during a failure to contain the radiation within safe levels. Having any missing alerts, especially with our sensor's ability to accurately detect radiation exposure levels. For this system, blocking of all other tasks when the button is pressed will allow for human intuition to alert anyone within the contaminated zone.
