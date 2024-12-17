---
aliases: [skilled]
---

One can be skilled in an [[Profession]], [[Talent]] or [[Weapontalent]].
Being skilled in something lowers the DC to succeed with a diceroll to 8, instead of the usual 13.

3d (skilled) = avg 1.95 Successes
3d (unskilled) = avg 1.20 Successes

function: evaluate ROLL:s {
 SUCCESSES: ROLL >= 8
 if SUCCESSES > 0 { result: SUCCESSES}
 result: 0
}

loop DICE over {1..6} {
 output [evaluate DICE d20] named "[DICE]d"
}