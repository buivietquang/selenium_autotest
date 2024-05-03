# selenium_autotest



from selenium import webdriver
from selenium.webdriver.chrome.service import Service
from webdriver_manager.chrome import ChromeDriverManager
import time
from selenium.webdriver.common.by import By

# Khởi tạo trình duyệt Chrome
service = Service(ChromeDriverManager().install())
driver = webdriver.Chrome(service=service)

driver.get("https://canvas.phenikaa-uni.edu.vn/login/canvas")
time.sleep(1)

driver.find_element(By.ID, 'pseudonym_session_unique_id').send_keys("21010647@st.phenikaa-uni.edu.vn")
driver.find_element(By.ID, 'pseudonym_session_password').send_keys("@Neverdie1001")
time.sleep(1)

driver.find_element(By.XPATH, '/html/body/div[2]/div[2]/div/div/div[1]/div/div/div/div/div/div[2]/form[1]/div[3]/div[1]/input[2]').click()
time.sleep(1)

driver.find_element(By.XPATH, '/html/body/div[2]/div[2]/div/div/div[1]/div/div/div/div/div/div[2]/form[1]/div[3]/div[2]/button').click()
time.sleep(1)

driver.find_element(By.XPATH, '/html/body/div[2]/header/div[1]/ul/li[3]/button').click()
time.sleep(1)

driver.find_element(By.XPATH, '/html/body/div[3]/span/span/div/div/div/div/div/ul[2]/li[2]/a').click()
time.sleep(1)

driver.find_element(By.XPATH, '/html/body/div[2]/div[2]/div/div[2]/div[1]/div/table[1]/tbody/tr[1]/td[2]/a/span').click()
time.sleep(1)

driver.find_element(By.XPATH, '/html/body/div[2]/div[2]/div[2]/div[2]/nav/ul/li[2]/a').click()
time.sleep(2)

driver.find_element(By.XPATH, '/html/body/div[2]/div[2]/div[2]/div[2]/nav/ul/li[5]/a').click()
time.sleep(2)

driver.find_element(By.XPATH, '/html/body/div[2]/div[2]/div[2]/div[2]/nav/ul/li[3]/a').click()

time.sleep(5)
driver.implicitly_wait(5)

driver.quit()
