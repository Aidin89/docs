---
layout: relation
title:  'neg'
shortdef : 'negation modifier'
---

In Finnish, negation is marked using the verb *ei*, which is used as an auxiliary and assigned the dependency relation `neg`. The most commonly negated elements are verbs and verb phrases, but occasional exceptions in verbless constructions are allowed.

If a conjunction or adverb has been merged together with *ei*, as in for instance *ettei* (*että+ei* "that+not") or *miksei* (*miksi+ei* "why+not"), then the word is marked as a conjunction or an adverb rather than a negation verb. However, *eikä* "and+not", when it appears alone and not coordinating another clause or phrase, is still marked as `neg`.

<!-- fname:neg.pdf -->
~~~ sdparse
Hän ei sanonut mitään . \n He didn't say anything .
nsubj(sanonut-3, Hän-1)
neg(sanonut-3, ei-2)
dobj(sanonut-3, mitään-4)
punct(sanonut-3, .-5)
~~~

### Diffs

FinnTreeBank (FI_FTB) is tokenized differently:
it treats *ettei* the same as *että ei* ("that not"),
*miksei* as *miksi ei* ("why not") and so on,
as if they were two separate words.
Consequently, *ei* (“not”) represents a normal negation verb
in these combinations and gets annotated `neg`.
On the other hand, *eikä* (“and+not”) is treated as a single
token with a clitic particle (and also marked as `neg`).
<!-- Interlanguage links updated Út zář 29 20:43:21 CEST 2020 -->
