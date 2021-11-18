from bs4 import BeautifulSoup
from selenium import webdriver
from time import sleep

music_names=[]
sayac=0
driver = webdriver.Chrome()
driver.get("https://www.youtube.com/watch?v=tQ0yjYUFKAE&list=PLw-VjHDlEOgvtnnnqWlTqByAtC7tXBg6D")
sleep(4)
soup = BeautifulSoup(driver.page_source,"html.parser")
table=soup.find("div",{"class":"playlist-items style-scope ytd-playlist-panel-renderer"})
contents =table.findAll("h4")
for content in contents:
    span = content.find("span").text.strip()
    music_names.append(span)
    #print(span)
#driver.close()
sleep(4)

for i in range(0,len(music_names)):
    try:
        driver.get("https://www.topupmp3.com/?q="+music_names[sayac]+"")
        sleep(5)
        mp3button=driver.find_element_by_xpath('//*[@id="results"]/div[1]/div/div/div[2]/div[1]/button[1]').click()
        sleep(5)
        mp3downloadbutton=driver.find_element_by_xpath('//*[@id="btnDownload"]').click()
        sayac+=1
        #soup = BeautifulSoup(google_search.text,"html.parser")
    except:
        pass


