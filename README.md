import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
 
import io.github.bonigarcia.wdm.WebDriverManager;
 
public class UsageOfSleep {
 
	public static void main(String[] args) {
 
		// Setting up browser executable using WebDriverManager
	WebDriverManager.chromedriver().setup();
		// Opening a browser and maximizing
		WebDriver driver = new ChromeDriver();
		driver.manage().window().maximize();
		// Loading a URL
		driver.get("https://www.redbus.in/");
		// Locating and typing in From text box.
		WebElement fromTextBox = driver.findElement(By.id("src"));
		fromTextBox.sendKeys("Ban");
		// Clicking on first search result
		driver.findElement(By.xpath("//li[@select-id='results[0]']")).click();
		// Closing browser
		driver.quit();
	}
}
