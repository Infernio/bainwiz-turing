# Turing Machine Emulator as a BAIN Wizard

## 1. What?
This is a BAIN wizard for [Wrye Bash](https://github.com/wrye-bash/wrye-bash/) that emulates a Turing machine, thereby
proving my conjecture that the BAIN wizard minilang is Turing-complete.

## 2. Why?
Three reasons:
 - An exercise for me to become more familiar with the BAIN wizard minilang, since I'm working on its interpreter.
 - Curiosity - after looking through the implementation of its interpreter, I was fairly sure the language was Turing-complete.
   But I obviously can't know without building a Turing machine emulator (or formally proving it).
 - To stress test the parser and interpreter. This wizard uses almost every feature of BAIN wizards *except* the ones that
   are commonly used. Really, the only uncommon feature that is unused here is `Exec` - and I did try to find a way to
   squeeze it in.

## 3. Usage
Have a look at the `examples` folder and its README. The basic gist is:
 - Create a Wrye Bash package.
 - Drop the `wizard.txt` file in.
 - Follow the instructions in the `wizard.txt` file, creating some subpackages with peculiar names.
   - These names encode the state configurations for the Turing machine.
   - One special subpackages begins with `I`, this subpackage describes the initial tape.
 - In Wrye Bash, right click on the package and click `Wizard Installer... > Manual Wizard` or
   `Wizard Installer... > Auto Wizard` if the startup message annoys you.

## 4. License
Licensed under MIT, see [LICENSE](LICENSE). No idea why you would want to use this, but feel free.
