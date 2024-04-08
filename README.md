# Chatbot
import nltk
from nltk.chat.util import Chat, reflections


pairs = [
    [
        r"my name is (.*)",
        ["Hello %1, how can I help you today?",]
    ],
    [
        r"what is your name?",
        ["My name is ChatBot and I'm here to assist you.",]
    ],
    [
        r"how are you ?",
        ["I'm doing well, thank you!",]
    ],
    [
        r"what is the weather today?",
        ["Its rainy today in Mumbai.",]
    ],
    [
        r"sorry (.*)",
        ["No problem, please don't apologize.",]
    ],
    [
        r"(.*) (good|great|fine)",
        ["That's great to hear!",]
    ],
    [
        r"PM of India",
        ["Shri. Narendra Modi",]
    ],
    [
        r"Capital of India",
        ["Delhi",]
    ],
    [
        r"quit",
        ["Goodbye! Take care.", "Goodbye, hope to see you soon!"]
    ],
]


def chatbot():
    print("Hello! I'm ChatBot. How can I assist you today?")
    chatbot = Chat(pairs, reflections)
    chatbot.converse()

if __name__ == "__main__":
    nltk.download("punkt")  
    chatbot()
