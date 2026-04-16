from selenium import webdriver
from selenium.webdriver.common.by import By

# Start Chrome browser
driver = webdriver.Chrome()

# Open Google homepage
driver.get("https://www.google.com/")

# Inspect and locate search box element
search_box = driver.find_element(By.NAME, "q")

# Print confirmation
print("Search box element found:", search_box)

# Keep browser open until user input
input("Press Enter to close...")

# Close browser
driver.quit()
face book
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC

# Start Chrome browser
driver = webdriver.Chrome()

# Open Facebook
driver.get("https://www.facebook.com/")

# Wait until email box is visible (max 10 seconds)
wait = WebDriverWait(driver, 10)
email_box = wait.until(EC.presence_of_element_located((By.ID, "email")))

print("Email box found:", email_box)

input("Press Enter to close...")
driver.quit()
