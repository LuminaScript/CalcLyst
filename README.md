# Language Proposal

## Motivation

The proposed language aims to serve as a bridge between mathematical modeling and functional programming, harnessing the power of OCaml to deliver a robust platform for computational mathematics. By combining a declarative style with strong, static typing and scoping, our language ensures that models are not only written in a form that closely mirrors mathematical notation but also benefit from the safety and predictability of functional programming. The inclusion of higher-order functions and partial application allows for a flexible and expressive syntax that can adapt to complex modeling scenarios. This language is particularly suited for users who require accurate and intricate mathematical models and visual graph representations, such as researchers, data scientists, and engineers in fields like finance, physics, and systems biology.

## Paradigms and Features

- **Functional Paradigm**: Embraces OCaml's efficient compilation mechanisms.
- **Declarative Programming**: Allows users to articulate computation logic without explicit control flow for enhanced readability and maintainability.
- **Strong, Static Typing and Scoping**: Aims to eliminate runtime errors and accidental variable shadowing.
- **Strict Evaluation**: Guarantees consistent performance outcomes.
- **Higher-Order Functions & Partial Application**: Offers potent tools for abstracting and composing complex functions.
- **Mathematical API-Style Interface**: Facilitates a user-friendly environment, mirroring mathematical conventions.
- **Caching Mechanism**: Optimizes performance for variables that are accessed frequently.
- **Efficient Compilation Process**: Leverages OCaml to translate high-level constructs, with a lexer and parser that transform tokens into machine code efficiently.
- **Embedded DSL for Graph Operations**: Enables intuitive model visualization, comparable to GraphCL.

## "Hello World" Program

```ocaml
let greet_world () =
  print_endline "Hello, World!"
  
let () = greet_world ()
```
This simple program demonstrates the OCaml-inspired syntax, with a function declaration that prints a greeting to the world. It showcases the use of higher-order functions and the language's approach to IO operations.

## Language in one-slide Program
```ocaml
(* Define a function to calculate the factorial *)
let rec factorial n = match n with
  | 0 -> 1
  | _ -> n * factorial (n - 1)

(* Partially apply to create a function for computing permutations *)
let permutations n r = factorial n / factorial (n - r)

(* Visualize a simple graph *)
let graph = Graph.create ()
let () = 
  Graph.add_nodes graph ["A"; "B"; "C"];
  Graph.add_edges graph [("A", "B"); ("B", "C")];
  Graph.draw graph

(* Main entry point *)
let () =
  let perm = permutations 5 3 in
  Printf.printf "Permutations of 5 taken 3 at a time: %d\n" perm;
  graph
```
This program encapsulates the language's core functional features, including recursive functions, pattern matching, and partial application. It also introduces the graph DSL, allowing users to create and manipulate graph structures visually.
