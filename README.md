def chatbot(user_input):
    # Convert user input to lowercase for case insensitivity
    user_input = user_input.lower()
    
    # Define predefined rules and responses
    rules = {
        "hi": "Hello!",
        "how are you?": "I'm good, thank you!",
        "what's your name?": "I'm a chatbot!",
        "bye": "Goodbye! Have a great day!"
    }
    
    # Check if user input matches any predefined rules
    for rule, response in rules.items():
        if rule in user_input:
            return response
    
    # If no match found, provide a generic response
    return "I'm sorry, I didn't understand that."

# Main loop to interact with the chatbot
while True:
    user_input = input("You: ")
    if user_input.lower() == 'exit':
        print("Chatbot: Goodbye!")
        break
    else:
        response = chatbot(user_input)
        print("Chatbot:", response)

