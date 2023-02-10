---
marp: true
theme: uncover
paginate: true
size: 16:9
class: invert
---

# Restore Router Password in Cisco Packet Tracer 💻

A Guide to Resetting Your Router Password

---

## Step 1: Open Cisco Packet Tracer

![bg right:50% 100%](https://content.instructables.com/F3Z/VCEB/J6QQP7AD/F3ZVCEBJ6QQP7AD.png?auto=webp)

- Load the simulation that contains the router.

---

## Step 2: Console Access

- Right-click on the router and select "Console."
- In the console window, enter the command `enable` and press enter.

---

## Step 3: Configure Terminal

Enter the command:

```bash
configure terminal
```

and press enter.

---

## Step 4: Set New Password

- Enter the following command to set a new username and password:

```bash
username admin privilege 15 password cisco
```

---

## Step 5: Save Changes

- Enter the command `exit` and press enter to save the changes.

---

## Step 6: User Management

- Close the console window and right-click on the router again.
- Select "Device Management" and then "User Management."
- Enter your new username and password and click "Apply."

---

## Step 7: Test New Login Credentials

- Close the user management window and test your new login credentials by right-clicking on the router and selecting "Console" again.

---

Your router password should now be successfully restored in Cisco Packet Tracer.

---

# <!--fit-->Thanks for reading!
