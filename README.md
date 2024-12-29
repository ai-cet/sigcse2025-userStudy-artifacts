# Feasibility Study of Augmenting Teaching Assistants with AI for CS1 Programming Feedback

Artifacts of a SIGCSE 2025 user-study paper on semi-automatically assisting CS1 students during live programming assignments.
For detailed insights and methodologies, you can access our paper through the following link: [Feasibility Study of Augmenting Teaching Assistants with AI for CS1 Programming Feedback](https://www.comp.nus.edu.sg/~bleong/publications/sigcse25-AI-augmented%20TAs.pdf).

## Citing Our Work

If you find our research or dataset useful, please consider citing it using the BibTeX entry below:

```
@inproceedings{ahmed2025feasibility,
  author={Ahmed, Umair Z and Sahai, Shubham and Leong, Ben and Karkare, Amey},
  title={Feasibility Study of Augmenting Teaching Assistants with AI for CS1 Programming Feedback},
  booktitle={Proceedings of the 56th ACM Technical Symposium on Computer Science Education V. 1 (SIGCSE TS 2025)},
  year={2025},
  location={Pittsburgh, PA, USA},
  publisher={ACM},
  address={New York, NY, USA},
  pages={7},
  url={https://doi.org/10.1145/3641554.3701972}
}
```

## Jupyter Notebook

`main.ipynb` contains the analysis and visualizations of our user study, exploring the impact of AI on CS1 student and TA performance.

## Dataset

We conducted a randomized intervention trial with `185` undergraduate students enrolled in a CS1 C programming course at a large public University. LLMs were used to service a total of `115` "Get Help" requests and depending on the question, the feedback was sent either directly to the student or indirectly after validation by a human TA. Our human TAs manually handled `17` help requests without any AI assistance.

Below is a detailed explanation of each CSV, along with the meanings of their respective column names.

---

### 1. Experimental Groups

- `assignment_id`: The unique identifier for each assignment given to the students.
- `user_id`: A unique identifier assigned to each student.
- `question_num`: Denotes the specific question number in an assignment that the student is addressing.
- `toolName`: The name of the tool or method assigned to the student for assistance. A majority of the students didn't request for any help
- `numEvaluation`: The number of testcase evaluations or attempts made by the student for a specific question.
- `timeTaken`: The total time, in minutes, that a student spent working on a particular question.
- `score`: The grade given to the student's solution for a question, based on the percentage of test-cases passed.

### 2. Requests

- `code_id`: A unique identifier for each individual code submission or help request made by a student.
- `assignment_id`: The unique identifier for each assignment, linking the request to a specific task assigned to students.
- `user_id`: A unique identifier assigned to each student, used to track submissions and requests by individual users.
- `question_num`: Denotes the specific question number within an assignment that the request pertains to.
- `toolName`: The name of the tool or method assigned to the student for assistance.
- `query`: The description of the help sought by student.
- `TA Service Time`: The duration of time, in minutes, that the AI/human spent addressing the help request.
- `content`: The student code state
- `testcases`: The test cases evaluation result on student code

### 3. Feedbacks

- `code_id`: A unique identifier for each individual code submission or help request made by a student.
- `question_num`: Denotes the specific question number within an assignment that the feedback pertains to.
- `toolName`: The name of the tool or method that generated or was used to generate the feedback.
- `feedbackIndex`: An index number identifying the specific feedback given for a code submission.
- `lineNum`: The line number(s) in the code to which the feedback relates.
- `feedback`: The actual feedback text provided to the student.

### 4. Feedback Ratings

- `code_id`: A unique identifier for each individual code submission or help request made by a student.
- `question_num`: Denotes the specific question number within an assignment that the feedback rating pertains to.
- `toolName`: The name of the tool or method used to generate the feedback.
- `key`: Represents the category of the rating. It can be one of the following:
  - `accurate`: Indicates the accuracy of the feedback.
  - `helpful`: Denotes how helpful the feedback was to the student.
  - `speed`: Relates to the timeliness of the feedback provided.
  - `line`: Refers to line-level rating
- `feedbackIndex`: An index number identifying the specific feedback for a code submission. Present only for line-level rating.
- `value`: The rating value for the respective key. `1` indicates a positive rating, while `0` indicates a negative rating.

---

For any clarifications on the dataset, please contact the authors over email. Your feedback would be much appreciated.
