!pip install requests beautifulsoup4
import requests
from bs4 import BeautifulSoup
url='https://www.milligazete.com.tr/arsiv/2025-03-22'
r = requests.get(url)
soup = BeautifulSoup(r.content, 'html.parser')
list= soup.find_all("div", {"class": "f-cat f-item"})
for i in list:
  print('==============================================================')
  for b in i.findAll("ul", {"class": "list underline"}):
    for link in b.find_all('a'):
      my_link =link.get('href') + "\n"
      print(my_link)
      newLink="www.milligazete.com.tr{}" .format(my_link)
      print(newLink)
      with open('beyzisko.txt' , "a", encoding="utf-8") as file:
        file.write(newLink)
        listem = [
          "https://www.milligazete.com.tr/arsiv/2025-03-21",
          "https://www.milligazete.com.tr/arsiv/2025-03-22",
          "https://www.milligazete.com.tr/arsiv/2025-03-23",
          "https://www.milligazete.com.tr/arsiv/2025-03-24",
          "https://www.milligazete.com.tr/arsiv/2025-03-25",
]

def abc(sayfa_url):
    r = requests.get(sayfa_url)
    soup = BeautifulSoup(r.content, 'html.parser')
    list= soup.find_all("div", {"class": "f-cat f-item"})
    for i in list:
        print('==============================================================')
        for b in i.findAll("ul", {"class": "list underline"}):
            for link in b.find_all('a'):
                my_link =link.get('href') + "\n"
                print(my_link)
                newLink="www.milligazete.com.tr{}" .format(my_link)
                print(newLink)
                with open('beyzisko.txt' , "a", encoding="utf-8") as file:
                    file.write(newLink)

for i in listem:
    sayfa_url = i
    abc(sayfa_url)
r = requests.get(url)
soup = BeautifulSoup(r.content, 'html.parser')
list= soup.find_all("div", {"class": "f-cat f-item"})
for i in list:
  print('==============================================================')
  for b in i.findAll("ul", {"class": "list underline"}):
    for link in b.findALL('a'):
      my_link =link.get('href') + "\n"
      print(my_link)
      newLink="www.milligazete.com.tr{}" .format(my_link)
      print(newlink)
      with open('beyzisko.txt' , "a", encoding="utf-8") as file:
        file.write(newlink)
        listem = [
          "https://www.milligazete.com.tr/arsiv/2025-03-21",
          "https://www.milligazete.com.tr/arsiv/2025-03-22",
          "https://www.milligazete.com.tr/arsiv/2025-03-23",
          "https://www.milligazete.com.tr/arsiv/2025-03-24",
          "https://www.milligazete.com.tr/arsiv/2025-03-25",
]

for i in listem:
    sayfa_url = i
    abc(sayfa_url)
