# TEMP_OIOIOI
## TL;DR
Repozytorium z testami oraz skryptami, ułatwi wam życie oraz szukanie błędów.

## bash
### Linux
Tutaj powinno wszyskto działać. Skrypty uruchamiane tak jak na zajęciach. Możliwy błąd końca lini.
Rozwiązanie problemu końca linii znalezione by Jakub Pisarek:
https://askubuntu.com/questions/304999/not-able-to-execute-a-sh-file-bin-bashm-bad-interpreter

### Windowsie
Póki problem nie zostanie rozwiązany polecam ustawienie sobie basha na działającego z konsoli
za pomocą tego tutorialu: https://hackernoon.com/how-to-install-bash-on-windows-10-lqb73yj3.
Następnie w uruchamiamy cmd, udajemy się do folderu z plikami i testami, a następnie skrypty 
(przykładowo skrypt "test_program.sh" dla pliku "solve.py" i folderu "tests")uruchamiamy za 
pomocą komendy:

**bash test_program.sh solve.py tests**

### bash na MacOS
Nie wiem :/

## test_program.sh
Prosty dwuargumentowy skrypt napisany w języku **bash**, który pozwoli na sprawdzenie
poprawności wyjścia dla napisanego przez nas programu oraz gotowych testów (tzn. takich,
które zawierają pliki o rozszerzeniach **in** oraz **out**).

Pierwszy argument: program o rozszerzeniu **exe** lub **py**.

Drugi argument: Katalog z gotowymi testami.

Sposób działania: Skrypt dla każdego pliku **x.in** znajdującego się w drugim katalogu
uruchomi program z wejściem takim samym jak w **x.in**, a następnie porówna wyjście
programu z plikiem o nazwie **x.out**. Jeżeli będą takie same, to wykona sprawdzenie dla
kolejnego pliku z katalogu, jeżeli pliki będą różne, przerwie sprawdzanie oraz poinformuje
nas, że wyjście programu oraz plik o nazwie **x.out** są różne, co pozwoli na prostym szukaniu
błędów
  
## make_output.sh
Prosty dwuagrumentowy skrypt napisany w języku **bash**, który pozwoli na wygenerowanie 
wyjścia dla napisanego przez nas programu

Pierwszy argument: program o rozszerzeniu **exe** lub **py**.

Drugi argument: Katalog z plikami o rozszerzeniu **in**.

Sposób działania: Skrypt dla każdego pliku **x.in** znajdującego się w drugim katalogu 
uruchomi program z wejściem takim samym jak w **x.in**, a następnie utworzy wyjście takie 
same jak program o nazwie **x.out**.
