# Mini Shell - FSO
A program that simulates a shell with very basic features. Accept 
the path of a program with a required argument and print
the output of the program entered by the user without a terminal. Example:

    /bin/apt-get moo

The output will be:

                    (__) 
                    (oo) 
              /------\/ 
             / |    ||   
            *  /\---/\ 
               ~~   ~~   
    ..."Have you mooed today?"...
    > Demorou 0.0 segundos, retornou 0

For more information on the problem statement, see the 
[PDF](https://moj.naquadah.com.br/contests/bcr-FSO-2021_1-trabalho-001/fso-timedshell.pdf), the 
[page](https://moj.naquadah.com.br/contests/bcr-FSO-2021_1-trabalho-001/fso-timedshell.html)
ou o [video](https://www.youtube.com/watch?v=cHcr1EZdFao) with a breef demonstration (starts on 14:27).


## Playing with mini-shell
Open the terminal and run:

    gcc mini_shell.c -O2 -static -lm

Igonore the warning and start the program:

    ./mini_shell.out

In another terminal try with redirect:

    ./mini_shell.out < red.txt

Try with some commands:

    /usr/bin/ls .
    /usr/bin/ls /
    /usr/bin/ls --color

    /bin/apt-get moo
    /bin/false 111

Do <kbd>Ctrl</kbd>+<kbd>D</kbd> to exit the program.


## Functions learned from the project:
[Docs](https://pubs.opengroup.org/onlinepubs/9699919799/functions/exec.html) of
function family `exec`.

- `execl`
- `execve`
- `gettimeofday`
- `execv`: seems much more convenient than `execl` because the call
function remains the same regardless of the number of arguments
of the command.
- `strerror`


## Measure time
[8 ways to measure time](https://levelup.gitconnected.com/8-ways-to-measure-execution-time-in-c-c-48634458d0f9).

[clock_t no stackoverflow](https://stackoverflow.com/questions/3557221/how-do-i-measure-time-in-c)


## Continuation/Evolution of the mini shell
[More funcionalities](https://web2.clarkson.edu/class/cs444/assignments/shell/)
from another universities.

[More inspiration](https://brennan.io/2015/01/16/write-a-shell-in-c/)
if need some help.
