<h1>ExpNo 1 :Developing AI Agent with PEAS Description</h1>
<h3>Name: Revathi.D </h3>
<h3>Register Number: 212221240045</h3>

AIM:
 To find the PEAS description for the given AI problem and develop an AI agent.
 
Theory: 
Performance Measure: minimize energy consumption, maximize dirt pick up. Making this precise: one point for each clean square over lifetime of 1000 steps.

Environment: two squares, dirt distribution unknown, assume accions are deterministic and environment is static (clean squares stay clean).

Actuators: Left, Right, Suck, NoOp.

Sensors: agent can perceive its location and whether location is dirty.

PEAS DESCRIPTION:


DESIGN STEPS
STEP 1:
Identifying the input:

STEP 2:
Identifying the output:

STEP 3:
Developing the PEAS description:

STEP 4:
Implementing the AI agent

STEP 5:
Measure the performance parameters

PROGRAM:
class VacuumCleanerAgent: def init(self): # Initialize the agent's state (location and dirt status) self.location = "A" # Initial location (can be "A" or "B") self.dirt_status = {"A": False, "B": False} # Initial dirt status (False means no dirt)
``
def move_left(self):
    # Move the agent to the left if possible
    if self.location == "B":
        self.location = "A"

def move_right(self):
    # Move the agent to the right if possible
    if self.location == "A":
        self.location = "B"

def suck_dirt(self):
    # Suck dirt in the current location if there is dirt
    if self.dirt_status[self.location]:
        self.dirt_status[self.location] = False
        print(f"Sucked dirt in location {self.location}")

def do_nothing(self):
    # Do nothing
    pass

def perform_action(self, action):
    # Perform the specified action
    if action == "left":
        self.move_left()
    elif action == "right":
        self.move_right()
    elif action == "suck":
        self.suck_dirt()
    elif action == "nothing":
        self.do_nothing()
    else:
        print("Invalid action")

def print_status(self):
    # Print the current status of the agent
    print(f"Location: {self.location}, Dirt Status: {self.dirt_status}") 
~~
Example usage:
agent = VacuumCleanerAgent()

Move the agent, suck dirt, and do nothing
agent.perform_action("left") agent.print_status() agent.perform_action("suck") agent.print_status() agent.perform_action("nothing") agent.print_status()


### OUTPUT:
![image](https://github.com/Revathi-Dayalan/19AI405ExpNo1/assets/96000574/1ed1db02-eab7-4dd8-90f6-d9032b4effcd)

Result:
Thus, an AI agent is developed.


