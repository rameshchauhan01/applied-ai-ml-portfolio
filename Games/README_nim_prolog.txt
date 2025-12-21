# Nim Prolog Rules & Interactive Advisor

Files:
- nim_rules.pl — SWI-Prolog rules for 3-pile Nim (remove 1..3) + interactive advisor.

## Run (SWI-Prolog)
swipl nim_rules.pl
?- play.

Then type states like:
5 5 5
3 5 5
3 4 5

The advisor will:
- Tell if the state is WINNING or LOSING (nim-sum test),
- Recommend a move (tries to reach nim-sum = 0),
- Show the next state.

## Notes
- If the ideal nim move requires removing >3, the advisor falls back: remove up to 3 from the largest pile.
- Rules cover: terminal detection, legal moves, state transition, nim-sum-based winning test,
  and best-move recommender.
