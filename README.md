# Mike
Witam
question_prompts = [
    "What color are apples?\n(a) green/red\n(b) yellow\n(c) teal\n",
    "What color are bananas?\n(a) orange\n(b) pink\n(c) yellow\n",
    "What color are strawberries?\n(a) red\n(b) pink\n(c) black\n",
]

class Question:
    def __init__(self, question_prompt, answer):
        self.question_prompt = question_prompt
        self.answer = answer

questions = [
    Question(question_prompts[0], answer="a"),
    Question(question_prompts[1], answer="c"),
    Question(question_prompts[2], answer="a"),
]

def run(questions):
    score = 0
    for question in questions:
        user_answer = input(question.question_prompt).strip().lower()
        if user_answer == question.answer:
            score += 1
    print(f"Score: {score}/{len(questions)}")

run(questions)
