# Bezpieczeństwo 2018

---

## Zastrzeżenie

To nie jest przewodnik totalny. Jedynie tłumaczy niektóre slajdy, które wydawaly mi się zawikłane i musiałem googlować, lub pamiętałem, że sprawiały miproblemy kiedyś.

Poprawki do ortografi i merytoryki walimy pull requestami: [gitrepo](github.com/TheMesoria/non-total-guide)

---

## Użytkownicy w systemie UNIX

Linux jest systemem: 

- wielozadaniowym,
- wielo-użytkownikowym

---

## UID w systemie UNIX

**UID** -> ID użytkownika który **STWORZYŁ** ten proces. Może być zmienione, tylko kiedy  proces ma EUID=0.
**EUID** -> [*effective*] używane do ewaluacji zezwoleń procesu. (Tego używasz do stwierdzenia czy proces coś może czy nie.)
**GID** -> ID grupy użytkowników.

[source](https://stackoverflow.com/questions/205070/whats-the-deal-with-all-the-different-uids-a-process-can-have)

---

## Ważne miejsca na `/`

```terminal
/etc/shadow
/etc/passwd
/etc/group
```

---

