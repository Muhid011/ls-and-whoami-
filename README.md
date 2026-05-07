## 1. Problem Statement
The standard `ls` and `whoami` commands are too simple. `ls` does not show important file details by default, and `whoami` just prints out a name without any context.

## 2. Describe the Solution
I modified both `./ls` and `./whoami` and rebuilt them using the `./build_on_wsl.sh` script:
* **ls.c:** I changed the code so it always shows the "long list" (with sizes and dates) automatically.
* **whoami.c:** I changed the code to add a "You are: " message before the username.
* **Testing:** I ran `./ls` and `./whoami` in the `src` folder to confirm that the changes actually worked.

### Pros
* Easier to use because I didn't need to type extra flags.
* The ./ls output gives more useful information by default.
* The ./whoami output is easier to understand.

### Cons
* Some users may expect the normal Linux behavior.
* Some programs may expect the default output, which could make it behave differently.
* The long format output uses more screen space.

<img width="1099" height="615" alt="Screenshot 2026-05-07 010950" src="https://github.com/user-attachments/assets/58cd7dcc-0e3f-47f0-9b5f-8f02878e845d" />
<img width="1112" height="118" alt="Screenshot 2026-05-07 012437" src="https://github.com/user-attachments/assets/fa3934de-a26a-4807-8e2e-a785d9d75ed4" />
