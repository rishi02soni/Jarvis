# Jarvis
I have started working on making a AI self talking bot named Jarvis..
Just for recognising and speaking the output for JARVIS....
{#With all the particular packages and modules}


import speech_recognition as sr
import os

def say(text):
    os.system(f"say{text}")

def takeCommand():
    r = sr.Recognizer()
    with sr.Microphone() as source:
        r.pause_threshold = 1
        audio = r.listen(source)
        query = r.recognize_google(audio, language='en-in')
        print(f"User said: {query}")
        return query

if __name__ == '__main__':
    print('PyCharm')
    say("Hello  i am jarvis")
    print("Listening....")
    text = takeCommand()
    say(text)
