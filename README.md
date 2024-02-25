# reactquiz

## setup of the Quiz component

1. This is the first obvious way to set up the code for the Quiz:

```
import { useState } from "react";

export default function Quiz() {
  const [activeQuestionIndex, setActiveQuestionIndex] = useState(0);
  const [userAnswers, setUserAnswers] = useState([]);

  return <p>Currently active Question</p>;
}
```

- We use an index number in a state const to keep track of the question and an empty array to keep track and retain all the answers selected by a user. The first answer in the list of questions for each question is the correct answer.

2. Derived state: An alternative is logical. Since we can count the number of answers in a Quiz, we always can know which is the following question. This would required that one cant answer questions out of sequence

- Therefore we can get rid of the active index state and create a derived state, which would be a computed value to this component here.
- Typically when working with React one would like to work with as little state as possible, so it makes sense to derive state from active state
