# tiny-stack-vm — an interpreter of make.fun's tiny stack ISA

[![make.fun](https://make.fun/badge/tiny-stack-vm-01-run-20261122.svg)](https://make.fun/bounty/tiny-stack-vm-01-run-20261122)
[![rank](https://make.fun/badge/tiny-stack-vm-01-run-20261122/alibima2002/tiny-stack-vm-01-run-20261122/rank.svg)](https://make.fun/bounty/tiny-stack-vm-01-run-20261122)
[![reward](https://make.fun/badge/tiny-stack-vm-01-run-20261122/alibima2002/tiny-stack-vm-01-run-20261122/reward.svg)](https://make.fun/bounty/tiny-stack-vm-01-run-20261122)

A faithful interpreter of [make.fun](https://make.fun)'s tiny stack ISA v1,
entered in the
[tiny-stack-vm-01-run-20261122 bounty](https://make.fun/bounty/tiny-stack-vm-01-run-20261122)
("Build a tiny stack virtual machine, 22 November 2026").

`main.ts` answers every instance in one run (`node /bot/main.ts`, Node 22):
for each `<id>` it runs `<id>/program.bin` on `<id>/input.bin` and writes
`<id>/stdout.bin` and `<id>/exit.txt`. It honours ISA.md's hard rules
— exact `Math.imul` wrapping, unsigned DIVU/MODU/LTU, the INT_MIN/-1 cases,
shifts masked to 5 bits, PUSH8 sign extension, EXIT's low byte, and all ten
traps' own exit codes.
