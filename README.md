# semaphore.md
WIP
This will hold templates for Semaphore...

# Preps: You need to create a user "ghost/IT account", that will handle the instructions as an Admin.

# Step 1: Adding keystore
<img width="1032" height="837" alt="image" src="https://github.com/user-attachments/assets/c7e23e74-35ad-4b70-8140-9e6ea6d92ffb" /></br>

# Step 2: Variable Groups
For some reason, I don't quite know, they said it's a must </br>
just make sure that the content has the curly brackets `{}`</br>
<img width="1319" height="881" alt="image" src="https://github.com/user-attachments/assets/f9b5529d-423b-497a-8ad1-87a085215439" /></br>

@ Step 3: Inventory (add the user credentials)
<img width="1047" height="683" alt="image" src="https://github.com/user-attachments/assets/cae74a28-a9bc-42ea-be6e-d2442dc80834" /></br>
you can also do in this fashion so you can see the actual name of the machines
```
[ubuntu]
dockerbox ansible_host=10.10.9.1
n8nbox ansible_host=10.10.10.9.2
monitorbox ansible_host=10.10.10.3
```

# Step 4: Repository
create a GitHub / point to a GitHub </br>
Copy the git location from GitHub:</br>
<img width="443" height="369" alt="image" src="https://github.com/user-attachments/assets/a76c5afe-b6e6-4ac8-bed0-e1c284ba9b10" /></br>
The branch it will most likely be `main`</br>
<img width="1043" height="439" alt="image" src="https://github.com/user-attachments/assets/2ed0b5d0-b3e4-47a0-b588-96afc0929c31" /></br>

# Task Templates
New Template, select `Ansible`</br>
example, notice this is selecting `Task`, this is also unknown to me, why is it not `Deploy`</br>
<img width="1418" height="841" alt="image" src="https://github.com/user-attachments/assets/96adfe58-3619-4801-a4ba-764bfdac827b" /></br>
Now you can hit play and hit `Dry Run` if you just want to make sure the commands will be delivered, but if your ready then do not check anything</br>
<img width="399" height="237" alt="image" src="https://github.com/user-attachments/assets/945518bf-78ef-4f20-8e43-cf1b4d65af6e" /></br>
sample of a success:</br>
<img width="1000" height="681" alt="image" src="https://github.com/user-attachments/assets/eafa3999-76bc-463a-a957-578573decfed" /></br>
