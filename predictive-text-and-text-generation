import markovify
from IPython.display import display
import ipywidgets as widgets

# Create a text box for user input
text_input = widgets.Text(
    description="Enter text:"
)
display(text_input)

# Button to submit the input text
button = widgets.Button(
    description="Generate Sentences"
)
display(button)

output = widgets.Output()

# Function to generate sentences when the button is clicked
def generate_sentences(button):
    with output:
        output.clear_output()  # Clear previous output
        text = text_input.value
        if text:
            text_model = markovify.Text(text)
            for i in range(5):
                print(text_model.make_sentence())
        else:
            print("Please enter some text.")

button.on_click(generate_sentences)
display(output)
