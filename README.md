This code is for dec morning batch.
package pom1;

import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.support.FindBy;
import org.openqa.selenium.support.PageFactory;

public class SignUpPagePOM {
	
	//Declaration
	
	@FindBy(xpath="//input[@name='firstname']") private WebElement fName;
	@FindBy(xpath="//input[@name='lastname']") private WebElement lName;
	@FindBy(xpath="//input[@name='reg_email__']") private WebElement phone;
	@FindBy(xpath="//input[@name='reg_passwd__']") private WebElement pwd;
	@FindBy(xpath="//select[@name='birthday_day']") private WebElement date;
	@FindBy(xpath="//select[@name='birthday_month']") private WebElement month;
	@FindBy(xpath="//select[@name='birthday_year']") private WebElement year;
	@FindBy(xpath="(//input[@type='radio'])[1]") private WebElement female;
	@FindBy(xpath="(//input[@type='radio'])[2]") private WebElement male;
	@FindBy(xpath="//button[@name='websubmit']") private WebElement signupBtn;
	
	//Initialization
	
	SignUpPagePOM(WebDriver driver){
		PageFactory.initElements(driver, this);
	}
	
	//Usage
	
	public void enterFirstName(String name) {
		fName.sendKeys(name);
	}
	public void enterLastName(String lName1) {
		lName.sendKeys(lName1);
	}
	public void enterPhone(String ph) {
		phone.sendKeys(ph);
	}
	public void enterPassword(String pass) {
		pwd.sendKeys(pass);
	}
	public void selectDate(String date1) {
		date.sendKeys(date1);
	}
	public void selectMonth(String month1) {
		month.sendKeys(month1);
	}
	public void selectYear(String year1) {
		year.sendKeys(year1);
	}
	public void selectFemale() {
		female.click();
	}
	public void selectMale() {
		male.clear();
	}
	public void clickSigninBtn() {
		signupBtn.click();
	}
	
	

}
