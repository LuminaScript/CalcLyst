# MathLyst: Mathematical Modeling Program Design Proposal

## Motivation

This program is designed to provide a user-friendly interface for mathematical modeling, leveraging the robustness of functional programming with OCaml. The declarative, strongly and statically typed nature of OCaml, along with static scoping and strict evaluation, offers a reliable and precise environment for computational tasks. Incorporating higher-order functions and partial application, the system ensures adaptability and concise, maintainable code. This language is particularly suitable for tasks requiring clear logical structure, crucial for mathematical modeling and graph-based computations.

## Paradigms and Features

The language supports the functional programming paradigm, emphasizing functions as the core of the language. The key features include:

- **Declarative Syntax**: For intuitive mathematical model definitions.
- **Strong, Static Typing**: To prevent type errors and ensure consistency.
- **Static Scoping**: For error avoidance and predictable side effects.
- **Strict Evaluation**: To maintain order and predictability in operations.
- **Higher-Order Functions**: For code pattern abstraction and reusability.
- **Partial Application**: Enabling functions to be versatile with the number of arguments.
- **Mathematical and Graph Operation Library**: A comprehensive standard library equipped for advanced mathematical and graph functions.

## "Hello World" Program

```ocaml
(* Define a simple function to output a greeting *)
let greet_world = 
  let greeting = "Hello" in
  let entity = "World" in
  print_endline (greeting ^ " " ^ entity);;

(* Invoke the function *)
greet_world;;
```
## Language in One-Slide Program
```ocaml
(* Demonstrate core language constructs: variables, functions, and basic I/O *)

(* Function to calculate the area of a circle *)
let area_of_circle radius =
  let pi = 3.14159 in
  pi *. radius *. radius;;

(* Function to partially apply and create a custom print function *)
let custom_print preface message =
  print_endline (preface ^ ": " ^ message);;

let print_area = custom_print "The area of the circle is";;

(* Main function to tie it all together *)
let main () =
  let radius = 5.0 in
  let area = area_of_circle radius in
  print_area (string_of_float area);;

(* Execute the main function *)
main ();;
```
