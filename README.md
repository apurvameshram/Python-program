# Python-program to count frequency of words in a file showing in the bar graph!
import numpy as np
import matplotlib.pyplot as plt
def print_words(filename):
    f = open(filename,'r')
    full_list = (f.read()).lower()
    print full_list
    list_content = full_list.split()
    countwords= {}
    for word in list_content:
        countwords[word] = 0
    for word in list_content:
        countwords[word] += 1
    print countwords.items()
    values=[]
    data=[]
    for i in countwords.items():
      x=countwords[i]
      values.append(x)
    for word in counterwords:
      y=counterwords[word]
      data.append(word)
    pos=np.arange(len(data))
    width=0.5
    plt.bar(pos,values,width)
    plt.yticks(pos,data)
    plt.show()
