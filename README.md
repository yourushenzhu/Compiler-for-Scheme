# Compiler-for-Scheme [for 64-bit x86_64 architecture]
The compiler for subset of scheme developed as part of P523

The checked-in code passes all the expected test cases. The testing summary is as follows:

Compiler Language Information
-----------------------------
Source Langauge : Subset of Scheme  
Target Language : x86-64 (AMD64) assembly   
Host   Language : Scheme  

Compilers used:
---------------
Chez Scheme Version 8.4 - used for producing the assembly code (.s)  
GCC - used for compiling Framework/Runtime.c and executing the assembly codes  

Compiler Passes:
----------------
1] Compiler/parse-scheme.ss  
2] Compiler/convert-complex-datum.ss  
3] Compiler/uncover-assigned.ss  
4] Compiler/purify-letrec.ss  
5] Compiler/convert-assignments.ss  
6] Compiler/optimize-direct-call.ss  
7] Compiler/remove-anonymous-lambda.ss  
8] Compiler/sanitize-binding-forms.ss  
9] Compiler/uncover-free.ss  
10] Compiler/convert-closures.ss  
11] Compiler/optimize-known-call.ss  
12] Compiler/uncover-well-known.ss  
13] Compiler/optimize-free.ss  
14] Compiler/optimize-self-reference.ss  
15] Compiler/introduce-procedure-primitives.ss  
16] Compiler/optimize-source.ss  
17] Compiler/lift-letrec.ss  
18] Compiler/normalize-context.ss  
19] Compiler/specify-representation.ss  
20] Compiler/uncover-locals.ss  
21] Compiler/remove-let.ss  
22] Compiler/verify-uil.ss  
23] Compiler/remove-complex-opera*.ss  
24] Compiler/flatten-set!.ss  
25] Compiler/impose-calling-conventions.ss  
26] Compiler/expose-allocation-pointer.ss  
27] Compiler/uncover-frame-conflict.ss  
28] Compiler/pre-assign-frame.ss  
29] Compiler/assign-new-frame.ss  
30] Compiler/select-instructions.ss  
31] Compiler/uncover-register-conflict.ss  
32] Compiler/assign-registers.ss  
33] Compiler/everybody-home.ss  
34] Compiler/assign-frame.ss  
35] Compiler/finalize-frame-locations.ss  
36] Compiler/discard-call-live.ss  
37] Compiler/finalize-locations.ss  
38] Compiler/expose-frame-var.ss  
39] Compiler/expose-memory-operands.ss  
40] Compiler/expose-basic-blocks.ss  
41] Compiler/optimize-jumps.ss  
42] Compiler/flatten-program.ss  
43] Compiler/generate-x86-64.ss  

Note:
-----

The code is move-bias enabled  
The code is optimize-source enabled

