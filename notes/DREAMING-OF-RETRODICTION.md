# Dream-RSI read alongside historical retrodiction

Notes kept in this fork. They do not concern the engineering claims of Dream-RSI, which are
left untouched. They concern the concept of history the system runs on, read against the
methodological debate about prediction of the past in the discipline of history.

Companion text: Gill, Trachtenberg, Gill, Tetlock, Robb, Varnum, Hutcherson, Grossmann and
Trodd, "Predicting the Past: Testing Expert Historical Judgement", *The American Historical Review*
130:4 (2025), 1615-1630. https://doi.org/10.1093/ahr/rhaf590

---

## 1. What history means here

History in Dream-RSI is a log: the tree of exploration decisions an agent already made,
each node carrying the measured outcome of a code execution. It is the record of a search,
not an account of a past.

Its decisive property is completeness. Nothing is predicted and nothing is missing, so the
tree is an exact simulator over the space that was realised, because it is that space. The
limit follows immediately: a policy can be replayed only where history actually went.

## 2. Four working parallels

### 2.1 The retrodiction tournament is a replay simulator

The fourth method proposed in the AHR article is structurally identical to the Dream-RSI
loop. Organisers hold declassified documents; participants, who have not seen them, are
asked what the documents show; answers are scored against the record. No archive is opened
again. The expensive run was paid for by someone earlier, which is exactly why evaluating a
new judgement now costs nothing.

### 2.2 Making the implicit layer explicit is the precondition for improving it

Dream-RSI's move is to take the exploration strategy, until then hand-written and frozen,
and make it explicit and programmable. The AHR argument is the same move on historical
inference: retrodiction is performed constantly but implicitly, sometimes unknowingly, and
only stating it explicitly makes it testable.

### 2.3 The improvement is to the method, not to the content

Retrodiction, the authors insist, does not alter the logic of a historical argument; it
makes it clearer and more testable. Tetlock's result across decades of tournaments is that
how an expert thinks matters more than what they think. Dream-RSI improves the policy, never
the hypothesis. Same level of intervention in both.

### 2.4 Strong priors suppress exploration

Tetlock's hedgehogs, committed to one large idea, fail to beat chance; foxes show modest
foresight. Dream-RSI reports a matching negative result: compressing past runs into
high-level directional insight and injecting it into the prompt consistently underperforms
the unguided baseline, because strong semantic priors over-constrain the search. Two
independent findings, one conclusion.

## 3. The inversion

Both projects say history; they stand on opposite sides of the gap.

The AHR article opens on absence: loss, destruction, redaction, silence, embargo. Retrodiction
exists in order to reason about what was never recorded.

Dream-RSI has no absences by construction, and that is the source of its precision. Nothing
outside the record can be asked about at all.

The agent dreams only inside the recorded. The historian retrodicts only outside it. One
word, inverse operations.

A consequence worth keeping in view: Dream-RSI's exactness rests on a cheap non-interpretive
evaluator returning a number. A declassified document is not a measurement; it is new
evidence that itself requires interpretation. The authors of the AHR article know where this
bites, and name it: a poorly specified retrodiction is easy to defend post hoc. A node in a
historical tree does not arrive with a score attached.

## 4. Open problem, and where the humanities are ahead

Dream-RSI's loop is path dependent. History selects the policy, the policy produces the next
world, the world enters history. What locks in is coverage: regions the early policy
systematically pruned never entered the record, and a policy tuned on that record reproduces
the same coverage. Nothing rejected them; they were simply never measured, so they cannot be
reconsidered. The paper concedes the boundary but does not test it. Every reported run starts
from the same hand-written parallel-refine policy, and no comparison across independent
initialisations is offered.[^1]

The AHR article carries a toolkit developed against precisely this failure, none of it
designed for machines:

- pre-registration reports, fixing predictions and confidence before the archive is opened,
  against post-hoc accommodation
- dialectical bootstrapping: make the prediction, then work deliberately on why it may be
  wrong, under competing assumptions
- adversarial collaboration: opponents agree in advance which retrodictions count and on what
  terms
- aggregation of independent estimates rather than one trajectory, so that individual errors
  cancel

Dream-RSI uses none of them, although they are cheaper for it than for historians: running
several independent initial policies and comparing their trajectories is a question of
compute, not of scholarly consensus.

The transfer runs from historians to engineers here, not the other way.

[^1]: Checked against `papers/Dream-RSI.pdf` as published in this repository. The paper
    reports no ablation over initial policies and no random seeds; its appendices cover task
    descriptions, prompts and discovered programs. The absence is in the paper itself, not an
    inference from the website.

---

## Sources

- Dream-RSI: https://www.dream-rsi.com and https://github.com/zhengkid/Dream-RSI
  (sections Idea, Insight, Analysis)
- Gill et al., "Predicting the Past", AHR 130:4 (2025): the four approaches to retrodiction;
  foxes and hedgehogs; Hobsbawm on the opened Soviet archives
- Isaiah Berlin, "The Hedgehog and the Fox"; Philip Tetlock, *Expert Political Judgement*
