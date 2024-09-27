# ANSIBLE

# TASK 1 - Importance of Configuration Management
- Write a brief summary discussing the significance of configuration management in maintaining infrastructure.
- Explore the benefits of configuration management for ensuring consistency, reliability, scalability, and reproducibility.

Configuration management is like having a set of rules and tools to make sure all the computers and software in a company work the same way and stay up-to-date.
Here’s why it’s important and how it helps:

Consistency: Imagine if every computer in an office had different software and settings. It would be confusing and hard to manage. 
Configuration management ensures that all computers and systems have the same setup, making everything run smoothly and predictably.

Reliability: When changes or updates are made manually, there’s a higher chance of mistakes. Configuration management uses automated tools to apply changes, reducing human error. This makes the system more reliable and less likely to have issues.

Scalability: As a business grows, it needs more computers and systems. Manually setting up each new system can be time-consuming and prone to errors. 
Configuration management makes it easy to add new systems quickly and correctly, helping the business expand efficiently.

Reproducibility: If something goes wrong, like a system crash, it’s important to be able to recreate the same setup quickly to get things running again. Configuration management keeps track of all settings and changes, allowing you to recreate environments exactly as they were, which is crucial for recovery and testing.

In short, configuration management keeps everything organized and running smoothly, ensuring that the company’s technology is reliable, scalable, and easy to manage.


# TASK 2 - Exploring Configuration Management Tools
- Compare various configuration management tools.
- Justify why Ansible is chosen over other tools, emphasising its simplicity, agentless nature, idempotency, and large community support.

Imagine you have to manage and keep several machines (like office computers) running smoothly. You need tools to help you ensure they all have the same software and settings. 

Here’s a look at four popular tools: Ansible, Puppet, Chef, and SaltStack, and why Ansible is often the top choice.

Ansible
Easy to Use: Ansible is like following a simple recipe. It's easy to read and understand, even if you're not a tech expert.
No Extra Software Needed: Ansible doesn’t need any extra programs installed on the computers it manages. It works with what’s already there.
Consistency: When Ansible makes a change, it checks to make sure it only changes what’s necessary and leaves everything else as it should be.
Big Community Support: Ansible has lots of people using and helping improve it, so there’s plenty of advice and ready-made solutions available.

Puppet
More Complex: Puppet is like following a more complicated recipe with its own special language, which can be harder to learn.
Needs Extra Software: Puppet requires you to install additional programs on each computer it manages.
Consistency: Puppet also ensures changes are made correctly and consistently.
Good Community: Puppet has a supportive community, but it’s not as big as Ansible’s.

Chef
More Complex: Chef uses a different, more complex language (like a more advanced cooking method) that can be harder to learn.
Needs Extra Software: Chef also needs extra programs installed on each computer it manages.
Consistency: Chef makes sure changes are applied consistently, just like Ansible and Puppet.
Good Community: Chef has a helpful community, but it's smaller compared to Ansible’s.

SaltStack
Flexible but Can Be Complex: SaltStack can work with or without extra programs on the computers it manages, which offers flexibility but can also add complexity.
Consistency: SaltStack ensures changes are made correctly and consistently.
Good Community: SaltStack has a good community, but it's smaller compared to Ansible and Puppet.

Why Choose Ansible
Easy to Use: Ansible is like following a simple, straightforward recipe. Even if you're not a tech expert, you can understand and use it without much hassle.
No Extra Software Needed: Ansible works with what’s already on your computers, so you don’t need to install any extra programs. This makes it easier to set up and maintain.
Consistency: Ansible checks to ensure that each change is necessary and correct, avoiding unnecessary work and keeping your systems stable.
Big Community Support: With lots of people using Ansible, you can find plenty of help, advice, and ready-made solutions for your needs.

In summary, Ansible is often chosen because it’s easy to use, doesn’t require extra software, ensures consistent changes, and has a large community for support. This makes it a reliable and efficient tool for managing company computers and software.



# Task 3: Understanding Ansible and Its Architecture
- Dive into Ansible's architecture, explaining its control node, managed nodes, and communication process.
- Explore Ansible components, including playbooks, roles, and inventory, and discuss their roles in configuration management.

Imagine you are the manager of a team, and you have to tell each team member what to do. Ansible works in a similar way, with a "control node" (the manager) and "managed nodes" (the team members).

Control Node (Manager)
This is the main computer where Ansible runs.
It sends instructions to other computers (managed nodes).

Managed Nodes (Team Members)
These are the computers that Ansible manages.
They follow the instructions sent by the control node.

Communication Process
The control node communicates with managed nodes using a common method called SSH (like sending emails).
No extra software is needed on the managed nodes to receive instructions, making it simple to set up.

Ansible Components

Playbooks (Instruction Manuals)
Playbooks are like detailed instruction manuals.
They are written in a simple language (YAML) and tell the managed nodes what tasks to perform.
Example: A playbook can tell a managed node to install a specific software.

Roles (Pre-Packaged Instructions)
Roles are like pre-packaged sets of instructions.
They bundle related tasks together to make them reusable and organized.
Example: A role might include all the steps needed to set up a web server, like installing the software and configuring settings.

Inventory (Team Roster)
The inventory is like a team roster.
It lists all the managed nodes (computers) and organizes them into groups.
Example: The inventory can have a list of all web servers, database servers, etc.

Putting It All Together
The control node (manager) uses the inventory (team roster) to know which computers (team members) to manage.
It sends instructions written in playbooks (instruction manuals) to the managed nodes.
Roles (pre-packaged instructions) help make the playbooks more organized and reusable.

In simple terms, Ansible's architecture helps you manage multiple computers efficiently by organizing instructions and communicating them clearly, making sure everything runs smoothly and consistently.

[ Ruben’s repo for anisble documentation
https://github.com/Rubben007/ansible-project/blob/master/project ]

# Task 4: Writing Ansible Playbooks

In this task, you will perform hands-on exercises to create Ansible playbooks for common configuration management tasks, specifically installing LAMP stack (Linux, Apache, MySQL, PHP) and LEMP stack (Linux, Nginx, MySQL, PHP) on two target node servers - one running Linux and the other running Windows. The control node for managing these servers will be a Linux server.
