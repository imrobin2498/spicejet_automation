from selenium import webdriver
from selenium.webdriver.common.keys import Keys
from selenium.webdriver.support.select import Select
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC
from selenium.webdriver.common.by import By
from time import sleep


def search():
    url = "https://www.spicejet.com/"
    browser = webdriver.Chrome('/home/robinsingh/Downloads/chromedriver_linux64/chromedriver')
    browser.get(url)
    browser.maximize_window()
    sleep(10)

    departure = browser.find_element_by_xpath('//*[@id="ctl00_mainContent_ddl_originStation1_CTXT"]')
    departure.click()
    departure.send_keys('Bengaluru')
    departure.send_keys(Keys.RETURN)
    sleep(2)

    arrival = browser.find_element_by_xpath('//*[@id="ctl00_mainContent_ddl_destinationStation1_CTXT"]')
    arrival.click()
    arrival.send_keys('Delhi')
    arrival.send_keys(Keys.RETURN)
    sleep(2)

    travel_date = browser.find_element_by_xpath(
        "//table[@class='ui-datepicker-calendar']//tr//a[contains(@class,'ui-state-default') and contains(.,'30')]")
    travel_date.click()

    sleep(1)

    search_btn = browser.find_element_by_id('ctl00_mainContent_btn_FindFlights')
    search_btn.click()
    sleep(10)

    browser.close()


if __name__ == '__main__':

    search()
