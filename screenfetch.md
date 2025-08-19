```yml
---
- name: Run screenfetch and get output
  hosts: all
  gather_facts: yes
  become: yes  # This enables privilege escalation for the entire play
  tasks:
    - name: Ensure screenfetch is installed on Debian-based systems
      ansible.builtin.apt:
        name: screenfetch
        state: present
        update_cache: yes  # Optional: update package cache
      when: ansible_os_family == "Debian"

    - name: Ensure screenfetch is installed on RedHat-based systems
      ansible.builtin.yum:
        name: screenfetch
        state: present
      when: ansible_os_family == "RedHat"

    - name: Run screenfetch on the remote machine
      ansible.builtin.shell: "screenfetch -N"
      register: screenfetch_output
      changed_when: false
      become: no  # Don't need root privileges for this task

    - name: Print the screenfetch output for each host
      ansible.builtin.debug:
        msg: |
          --------- Output from {{ inventory_hostname }} ---------
          {{ screenfetch_output.stdout }}
      become: no  # Don't need root privileges for this task
```
