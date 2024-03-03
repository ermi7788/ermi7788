import requests
from bs4 import BeautifulSoup

url = "https://freefire-battlegrounds.fandom.com/wiki/News"
response = requests.get(url)
soup = BeautifulSoup(response.text, "html.parser")

headlines = soup.find_all("div", class_="pi-item pi-border-color--light")
for headline in headlines:
    print(headline.h3.text.strip())
import pyautogui

# Move the mouse to the coordinates (100, 100)
pyautogui.moveTo(100, 100)
import pandas as pd

# Read a CSV file into a DataFrame
df = pd.read_csv("free_fire_data.csv")

# Perform some data analysis
average_damage = df["damage"].mean()
print(f"Average damage: {average_damage}")
