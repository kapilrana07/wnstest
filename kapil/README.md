
# Project Title

Project is for currency conversion base on Base currency and Target currency after that we need to put the amount in Amount to be convert field which you want to convert.


## Acknowledgements

 - [Awesome Readme Templates](https://awesomeopensource.com/project/elangosundar/awesome-README-templates)
 - [Awesome README](https://github.com/matiassingers/awesome-readme)
 - [How to write a Good readme](https://bulldogjob.com/news/449-how-to-write-a-good-readme-for-your-github-project)


## API Reference

#### Get all items

```http
  GET /api/items
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `api_key` | `string` | **Required**. Your API key |

#### Get item

```http
  GET /api/items/${id}
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `id`      | `string` | **Required**. Id of item to fetch |

#### add(num1, num2)

Takes two numbers and returns the sum.


## Appendix

User should be accessing the form as per the given access in the data base. So here I need to perform stability testing, database testing and functionality testing for displays them correctly to the user so it is basically the approach to check this form.
Tester manually verifies if the currency is displayed with the details in the front end. We will manually verify that the product details have changed.
We will check functionalities of software application its working as per specifications by checking screens and controls like menus, buttons, icons. 
So basically, here we will Build the model, Determine Inputs for this form, Calculate the expected output for the model, Run the tests, Compare the actual output with the expected output and a decision on further action on the form.



## Points:
We will perform here usability testing for a particular functionality, we need to perform date base testing also for Add, Delete, and Edit the data. Operational acceptance testing this testing technique performed to verify the operational readiness (pre-release) of a product or application under test as part of Software test life cycle. 
This testing technique mainly focusses on operational readiness of the system.
We will perform the update operation and value should be updated as per the updation value. If we have the delete operation then we perform delete operation and form to be updated after deletion. We will also perform Partition Testing that divides the input data of a software unit into partitions of equivalent data from which test cases can be derived. then test cases are designed to cover each partition at least once. Here we will also use Operational Acceptance Testing to analyse the Operational Documentation, analyse the code, End-to-End Test Environment Operational Testing, Load & Performance Test Operation and Backup and Restore Testing.
## Authors

- [@katherinepeterson](https://www.github.com/octokatherine)


## Badges

Add badges from somewhere like: [shields.io](https://shields.io/)

[![MIT License](https://img.shields.io/apm/l/atomic-design-ui.svg?)](https://github.com/tterb/atomic-design-ui/blob/master/LICENSEs)
[![GPLv3 License](https://img.shields.io/badge/License-GPL%20v3-yellow.svg)](https://opensource.org/licenses/)
[![AGPL License](https://img.shields.io/badge/license-AGPL-blue.svg)](http://www.gnu.org/licenses/agpl-3.0)

## Color Reference

| Color             | Hex                                                                |
| ----------------- | ------------------------------------------------------------------ |
| Example Color | ![#0a192f](https://via.placeholder.com/10/0a192f?text=+) #0a192f |
| Example Color | ![#f8f8f8](https://via.placeholder.com/10/f8f8f8?text=+) #f8f8f8 |
| Example Color | ![#00b48a](https://via.placeholder.com/10/00b48a?text=+) #00b48a |
| Example Color | ![#00d1a0](https://via.placeholder.com/10/00b48a?text=+) #00d1a0 |

we can also change the convert button Color as per the visibility.
•	When we click on maintenance button then maintain currencies and maintain commission rate should be on next page separately not on same because in this condition header is not visible in proper way.
## Contributing

our testing approach is to globalised this application as internationally and As we know this is the currency conversion application and this application would convert the currencies across the countries and we have already covered most of the scenarios on above answers but still we can perform/validate the conversion for the multiple countries. As per the internationalization testing, we can also check language, culture and region, date, Content localization, Feature-based, User Interface, Rendering, File transformation and Database.
•	When we click on maintenance button then maintain currencies and maintain commission rate should be on next page separately not on same because in this condition header is not visible in proper way.
Test cases are categorized into two parts, reusable test cases which can be used in further regression cycles and obsolete test cases which cannot be used in succeeding cycles. 


## Demo

Insert gif or link to demo


## Deployment

package kapil;

import java.awt.Component;
import java.awt.Dimension;
import java.awt.List;

import org.openqa.selenium.By;
import org.openqa.selenium.JavascriptExecutor;
import org.openqa.selenium.Keys;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.chrome.ChromeOptions;

public class Test {

	public static void main(String[] args) {

		// Launch the Browser
		System.setProperty("webdriver.chrome.driver", "D:\\chromedriver_win32/chromedriver.exe");

		// Disable Notifications
		ChromeOptions options = new ChromeOptions();
		options.addArguments("--disable-notifications");

		WebDriver driver = new ChromeDriver(options);

		// Window maximize
		driver.manage().window().maximize();

		// Open URL
		driver.get("https://www.moneycorp.com/en-gb/");

		// Accept cookies
		//driver.findElement(By.cssSelector("button#onetrust-accept-btn-handler")).click();

		// Change Language and region
		WebElement languageList = driver.findElement(By.id("language-dropdown-flag"));
		languageList.click();
		driver.findElement(By.xpath("//*[@id=\"nav-languages-overlay\"]/div/ul/li[9]/a")).click();

		// Validate Foreign exchange solutions
		WebElement foreignExchangeSolutions = driver
				.findElement(By.xpath("/html/body/section/div[4]/div[3]/div/div/div[1]/div/a"));
		JavascriptExecutor jse = (JavascriptExecutor) driver;
		jse.executeScript("arguments[0].click()", foreignExchangeSolutions);
		String foreignExchangeSolutionsURL = "https://www.moneycorp.com/en-us/business/foreign-exchange-solutions/";
		if (!driver.getCurrentUrl().equalsIgnoreCase(foreignExchangeSolutionsURL)) {
			driver.close();
		}
		driver.findElement(By.xpath("/html/body/section/div[1]/header/div[2]/div/div[3]/button[1]")).click();

		// International payments searching
		WebElement navSearch = driver.findElement(By.id("nav_search"));
		navSearch.sendKeys("international payments");
		navSearch.sendKeys(Keys.ENTER);

		String internationalPaymentsURL = "https://www.moneycorp.com/en-us/search/?q=international+payments";

		if (!driver.getCurrentUrl().equalsIgnoreCase(internationalPaymentsURL)) {
			driver.close();
		}
		// Validate the Links
		System.out.println(driver.findElements(By.tagName("a")).size());
	}
}



## Documentation
1.	Open the following URL: https://www.moneycorp.com/en-gb/ 
// Launch the Browser
		System.setProperty("webdriver.chrome.driver", "D:\\chromedriver_win32/chromedriver.exe");
        WebDriver driver = new ChromeDriver(options);
2.	Change the language and region from the top right corner to USA (English). 
WebElement languageList = driver.findElement(By.id("language-dropdown-flag"));
		languageList.click();
		driver.findElement(By.xpath("//*[@id=\"nav-languages-overlay\"]/div/ul/li[9]/a")).click();

3.	Click Find out more for “Foreign exchange solutions” Validate if you have arrived on the page
 Validate Foreign exchange solutions
		WebElement foreignExchangeSolutions = driver
				.findElement(By.xpath("/html/body/section/div[4]/div[3]/div/div/div[1]/div/a"));
		JavascriptExecutor jse = (JavascriptExecutor) driver;
		jse.executeScript("arguments[0].click()", foreignExchangeSolutions);
		String foreignExchangeSolutionsURL = "https://www.moneycorp.com/en-us/business/foreign-exchange-solutions/";
		if (!driver.getCurrentUrl().equalsIgnoreCase(foreignExchangeSolutionsURL)) {
			driver.close();
		}
		driver.findElement(By.xpath("/html/body/section/div[1]/header/div[2]/div/div[3]/button[1]")).click();

5.	Search for the word “international payments” using the search box
WebElement navSearch = driver.findElement(By.id("nav_search"));
		navSearch.sendKeys("international payments");
		navSearch.sendKeys(Keys.ENTER);

		String internationalPaymentsURL = "https://www.moneycorp.com/en-us/search/?q=international+payments";

		if (!driver.getCurrentUrl().equalsIgnoreCase(internationalPaymentsURL)) {
			driver.close();
6.	Validate if you have arrived on the result page
System.out.println(driver.findElements(By.tagName("a")).size());
## Features

We can convert the currency Base currency and Target currency after that we need to put the amount in Amount to be convert field which you want to convert. 


## Feedback

If you have any feedback, please reach out to us at fake@fake.com


## New Comment:
•	When we click on maintenance button then maintain currencies and maintain commission rate should be on next page separately not on same because in this condition header is not visible in proper way.
•	while we are converting any amount then amount to be target currency field should be enabled.
•	Convert button is not in right colour. It should be in proper colour.
•	Convert button should be clickable/enterable and currency should be converted as per calculation logic and displayed in the amount in target currency field after click/enter conversion button. 
•	Colour alignment should be in proper way for all fields, check box, and button.
further we can also do these kind of changes in this project.
