# Evaluation-on-Few-Shot-formattingability-of-GPT-chat-creation

This folder contains three stages of experiments utilizing GPT family models, all of which employ the same dataset, MultiNLI. The primary objective across these stages is to evaluate the few-shot formatting ability of the models. Let's break down each stage and the conditions for experimentation:

**Stage 1:** In this stage, we focus on specific instructive labels while varying the conditions, such as the number of examples used and the model selected. The key conditions include:
- `num_example`: 0, 1, 3, 5, 10 examples
- `fewshot_label`: True label, space, opposite label
- `model`: gpt-4-0314, gpt-3.5-turbo, text-davinci-003, text-curie-001

**Stage 2:** In the second stage, we explore a broader range of experiments, examining the impact of different sequences of elements in the input, instruction, format instruction, and examples. The conditions for this stage include:
- `Input sequence`: General scenarios 1, 2, 3, 4
- `task_instruction`: Template0, Template1
- `format_instruction`: Format_instruction0, Format_instruction1
- `num_example`: 0, 1, 3 examples
- `model`: gpt-4-0314, gpt-3.5-turbo, text-davinci-003, text-curie-001

Here’s the definition of general scenarios 1, 2, 3, 4 are defined in document Stage3/mnli3%20research%20plan.docx.

**Stage 3:** In the third stage, our focus shifts to assessing whether GPT models can generate output in expected formats, including complex ones like providing answers for multiple data points and outputting them in a dictionary or list format. The conditions for this stage are:
- `Format`: Base string, list, dictionary, Mass string, list, dictionary
- `Input sequence`: General scenarios 1, 2, 3, 4
- `num_example` (for Base): 0, 1, 3 examples
- `num_example` (for Mass): 0, 3, 5 examples
- `model`: gpt-4-0314, gpt-3.5-turbo, text-davinci-003, text-curie-001

Now, let's clarify the list of result data that was collected and observed for each experiment:

1. **Accuracy:** This metric measures the percentage of experiments where the correct expected answer was generated and easily retrieved out of all the data tested.

2. **F1 Score:** The F1 score is a measure of accuracy that balances precision and recall, providing an overall performance evaluation.

3. **Correct Ratio:** It represents the percentage of experiments where the output, retrievable or convertible into the expected label format, yielded the correct answer out of all the data tested in one experiment.

4. **Unknown Rate:** This metric measures the percentage of experiments where the output was generated but couldn't be retrieved or converted into the expected label format.

5. **Wrong Rate:** It is complementary to the correct ratio and represents the percentage of experiments where the output, retrievable or convertible into the expected label format, yielded an incorrect answer. It can be calculated as 1 minus the correct ratio.

6. **RLR (Ratio of Lengths):** This ratio is the average expected output length divided by the average generated output length. It provides insights into the length of generated responses compared to expected responses.

In summary, these experiments aim to systematically evaluate the performance of GPT models under various conditions, with a focus on their ability to generate formatted output and provide accurate answers. The collected metrics help assess the models' capabilities and limitations in handling different scenarios and formatting requirements.
