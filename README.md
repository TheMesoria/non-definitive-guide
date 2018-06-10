<!-- $theme: gaia -->

# Bezpieczeństwo 2018

---

## Zastrzeżenie

To nie jest przewodnik totalny. Jedynie tłumaczy niektóre slajdy, które wydawaly mi się zawikłane i musiałem googlować, lub pamiętałem, że sprawiały miproblemy kiedyś.

Poprawki do ortografi i merytoryki walimy pull requestami: [gitrepo](github.com/TheMesoria/non-total-guide)
Slajdy: [2015](http://dream.ict.pwr.wroc.pl/ssn/bus-www.pdf)

---

## Użytkownicy w systemie UNIX

Linux jest systemem: 

- wielozadaniowym,
- wielo-użytkownikowym

---

## UID w systemie UNIX

**UID** -> ID użytkownika który **STWORZYŁ** ten proces. Może być zmienione, tylko kiedy  proces ma EUID=0.
**EUID** -> [*effective*] używane do ewaluacji zezwoleń procesu. (Tego używasz do stwierdzenia czy proces coś może czy nie.)
**SUID** -> [*Saved UID*] Daje użytkownikowi prawo do wystartowania aplikacji, nie jako on, ale osoba zapisana.
**GID** -> ID grupy użytkowników.

[source1](https://stackoverflow.com/questions/205070/whats-the-deal-with-all-the-different-uids-a-process-can-have)
[source2](https://www.linux.com/blog/what-suid-and-how-set-suid-linuxunix)

---

## Ważne miejsca na `/`

```bash
# Ten plik ogranicza dostęp do hashy haseł,
# dla wszystkich, z wyjątkiem najbardziej uprawnionych.
/etc/shadow
# Tekstowa baza danych przechowująca dane logowania
# oraz informacje kto może się zalogować.
/etc/passwd
# Plik tekstowy definiujący przynależność do grup.
/etc/group
```

---

## /etc/passwd

![wiki](images/passwd.png)

[source](https://en.wikipedia.org/wiki/Passwd#Password_file)

---

## Fundamentalne cechy wszytskich systemów UNIX

- Rozróżnienie na **administratora** oraz **użytkownika**
- 