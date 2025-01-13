from tkinter import Tk, Entry, Button,  Label, StringVar



igbo_dict = {"nnoo": "welcome",
             "udo": "peace",
             "nna": "father",
            "nne": "mother",
             "ezi": "good",
             "ulo": "house",
             "mmiri": "water",
             "akwukwo":"book",
             "anyanwu": "sun",
             "utitu oma": "good morning",
             "mgbede oma": "good evening",
             "enyi": "friend",
             "ezinulo": "family",
             "mba": "no",
             "iru": "face",
             "bia": "come",
             "isi": "head",
             "imi": "nose",
             "aka": "hand",
             "obo-aka": "palm"
             }


window =  Tk()
window.geometry('600x250')
window.title("igbo Dictionary")

entry_text = Entry(window, width=40)
entry_text.pack(pady=10)

result = StringVar()
result_label = Label(window, textvariable=result, font=("arial", 14))
result_label.pack(pady=10)

def search(word):
    if word in igbo_dict:
        result.set(igbo_dict[word])
    else:
        result.set("Not Found")

search_btn = Button(window, text="search", command=lambda:search(entry_text.get()))
search_btn.pack(pady=10)

window.mainloop()
