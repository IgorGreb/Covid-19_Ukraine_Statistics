from bs4 import BeautifulSoup
import requests
import lxml
import datetime

url = 'https://covid19.gov.ua/'
r = requests.get(url).text
soup= BeautifulSoup(r, 'lxml')


info = soup.find_all('div', class_="after-title")

x = datetime.datetime.now()
print('Станом на :')
print(x)

for res in info:
	ill = soup.find('div', class_='one-field light-box info-count flex-w-50').text
	new = soup.find('div', class_='one-field light-pink-box info-count flex-w-50').text
	recover = soup.find_all('div', class_='one-field light-box info-count flex-w-30')
	print('___________________________'+ill+'___________________________')
	print(new+'___________________________')
	for i in recover:
		print(i.text+'___________________________')


if __name__ == '__main__':
	pass

	
