# Selenium

Purpose: To build a framework around the Selenium WebDriver to simplify the
basic capabilities that are most frequently used (in my experience anyway).

# Instructions
- Install Python version 3
- Install the selenium bindings for Python: `pip install selenium`
- Install the SeleniumFramework.py file into a location searchable by Python
    - i.e. site-packages or the folder containing your test scripts
- Sample test script:
```
import SeleniumFramework as SF

driver = SF.Driver()
driver.open('gc')   # Can be gc, ff, ie.
driver.goto('https://duckduckgo.com/')

element = driver.find('name=q') 
element.send_keys('SeleniumHQ')
element.submit()

assert driver.browser.title == 'SeleniumHQ at DuckDuckGo'
driver.close()
```
