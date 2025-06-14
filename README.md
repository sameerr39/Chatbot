import re

def chatbot_response(user_input):
    # Rule 1: Greeting
    if re.match(r"hello|hi", user_input, re.IGNORECASE):
        return "Hello! How can I assist you today?"

    # Rule 2: Name
    elif re.match(r"what is your name", user_input, re.IGNORECASE):
        return "My name is AssistantBot, nice to meet you!"

    # Rule 3: Capabilities
    elif re.match(r"what can you do", user_input, re.IGNORECASE):
        return "I can provide information on a wide range of topics, from science and history to entertainment and culture."

    # Rule 4: Goodbye
    elif re.match(r"goodbye|bye", user_input, re.IGNORECASE):
        return "Goodbye! It was nice chatting with you."

    # Rule 5: How are you
    elif re.match(r"how are you", user_input, re.IGNORECASE):
        return "I'm doing well, thanks for asking! I'm a large language model, so I don't have feelings like humans do, but I'm always happy to chat with you."

    # Rule 6: What time is it
    elif re.match(r"what time is it", user_input, re.IGNORECASE):
        return "I'm a large language model, I don't have access to real-time information, but I can suggest ways for you to find out the current time."

    # Rule 7: What is the weather like
    elif re.match(r"what is the weather like", user_input, re.IGNORECASE):
        return "I'm a large language model, I don't have access to real-time weather information, but I can suggest ways for you to find out the current weather."

    # Rule 8: Tell me a joke
    elif re.match(r"can you tell me a joke", user_input, re.IGNORECASE):
        return "Here's one: Why couldn't the bicycle stand up by itself? Because it was two-tired!"

    # Rule 9: Default response
    else:
        return "I didn't understand that. Can you please rephrase or ask a different question?"

# Test the chatbot
while True:
    user_input = input("You: ")
    response = chatbot_response(user_input)
    print("AssistantBot:", response)
