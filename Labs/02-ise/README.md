# Lab 2: Xilinx ISE Design Suite

#### Table of contents

1. [Lab prerequisites](#Lab-prerequisites)
2. [Synchronize Git and create a new folder](#Synchronize-Git-and-create-a-new-folder)
3. [Digital circuits in VHDL language](#Digital-circuits-in-VHDL-language)
4. [Clean project and synchronize git](#Clean-project-and-synchronize-git)
5. [Ideas for other tasks](#Ideas-for-other-tasks)


## Lab prerequisites

1. *Digital* or *Binary comparator* compares the digital signals A, B presented at input terminal and produce an outputs depending upon the condition of those inputs. Complete a truth table for 1-bit *Identity comparator* (A=B), and two *Magnitude comparators* (A>B, A<B).

    | **B** | **A** | **A>B** | **A=B** | **A<B** |
    | :-: | :-: | :-: | :-: | :-: |
    | `0` | `0` | `0` | `1` | `0` |
    | `0` | `1` |  |   |   |
    | `1` | `0` |  |   |   |
    | `1` | `1` |  |   |   |

    For all outputs (i.e. A>B, A=B, A<B) create a canonical SoP (Sum of Product) and PoS (Product of Sum) forms.


## Synchronize Git and create a new folder

1. Open a Linux terminal, use `cd` commands to change path to your Digital-electronics-1 working directory, and [synchronize the contents](https://github.com/joshnh/Git-Commands) with GitHub.

    ```bash
    $ pwd
    /home/lab661
    $ cd Documents/your-name/Digital-electronics-1/
    $ pwd
    /home/lab661/Documents/your-name/Digital-electronics-1
    $ git pull
    ```

2. Create a new folder `Labs/02-ise`.

    ```bash
    $ cd Labs/
    $ mkdir 02-ise
    ```


## Digital circuits in VHDL language

1. Follow instructions from Wiki and [create a new project in ISE](https://github.com/tomas-fryza/Digital-electronics-1/wiki/How-to-create-a-new-project-in-ISE).

2. Using VHDL operators, define the architecture for digital comparator. Most common VHDL operators are shown in the table.

    | **Operator** | **Description** |
    | :-: | :-- |
    | `<=` | Value assignment |
    | `and` | Logical AND |
    | `nand` | Logical AND with negation |
    | `or` | Logical OR |
    | `nor` | Logical OR with negation |
    | `not` | Nagation |
    | `xor` | Exclusive OR |
    | `xnor` | Exclusive OR with negation |
    | `-- comment` | Comments |

3. Follow instructions from Wiki, create a test bench, and [simulate your design](https://github.com/tomas-fryza/Digital-electronics-1/wiki/How-to-Simulate-Your-Design-in-ISE) in ISim simulator.

4. Follow instructions from Wiki, create a constraints file, and [implement your design](XXXX) to CoolRunner-II CPLD starter board. See schematic of [CoolRunner-II CPLD starter board](../../Docs/coolrunner-ii_sch.pdf) and find out the connection of LD1, LD2, LD3, LD4 LEDs and BTN1, BTN2 push buttons. Modify the internal architecture of your design so that the pressed button represents log. 1 and LED is turn off for log. 0.


## Clean project and synchronize git

1. Clean up all generated files in menu **Project > Cleanup Project Files...** and close the project useing **File > Close Project**.

2. Use `cd ..` command in Linux terminal and change the working directory to `Digital-electronics-1`. Then use [git commands](https://github.com/joshnh/Git-Commands) to add, commit, and push all local changes to your remote repository. Check the repository at GitHub web page for changes.

    ```bash
    $ pwd
    /home/lab661/Documents/your-name/Digital-electronics-1/Labs/02-ise

    $ cd ..
    $ cd ..
    $ pwd
    /home/lab661/Documents/your-name/Digital-electronics-1

    $ git status
    $ git add <your-modified-files>
    $ git status
    $ git commit -m "[LAB] Adding 02-ise lab"
    $ git status
    $ git push
    $ git status
    ```


## Ideas for other tasks

1. Accordin to [Binary Decoders](https://www.electronics-tutorials.ws/combination/comb_5.html), create and simulate VHDL architecture of 2-to-4 binary decoder.