# EntersektTeam
//To run this file use Selenium 3 and latest version of firefox.


package Entersekt;

import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.firefox.FirefoxDriver;
import org.openqa.selenium.By;


public class Entersektteam {

	public static void main(String[] args) throws InterruptedException {
		
		System.setProperty("webdriver.gecko.driver","C:\\Selenium\\geckodriver.exe");
		
		WebDriver driver = new FirefoxDriver();
		driver.manage().window().maximize();
		
		driver.get("https://www.entersekt.com/Company-The-team"); 
		Thread.sleep(1000); 

		String expected_String1 = "Schalk joined Entersekt as CEO";

		String actual_String1 = driver.findElement(By.xpath(".//*[@id='features']/div/div/div[2]/div[1]/p[3]")).getText();

		if(actual_String1.contains(expected_String1)){
		System.out.println("Schalk Nolte is the CEO of Entersekt.");}
		else{
        System.out.println("Schalk Nolte is not the CEO of Entersekt.");}	  
		  				
		WebElement element = driver.findElement(By.xpath(".//*[@id='features']/descendant::span[text()='Non-executive board members']"));
		element.click();
		System.out.println(element.getText());
			
		String expected_String2 = "RAMZI MANSOUR";
		String actual_String2 = driver.findElement(By.xpath(".//*[@id='features']/descendant::span[text()='Ramzi Mansour']")).getText();
		if(actual_String2.equals(expected_String2)){
		System.out.println("Ramzi Mansour is one of the Non-executive board members of Entersekt.");}
        else{
		System.out.println("Ramzi Mansour is not the Non-executive board members of Entersekt.");}
		
		String expected_String3 = "NATHAN MINTAH";
		String actual_String3 = driver.findElement(By.xpath(".//*[@id='features']/descendant::span[text()='Nathan Mintah']")).getText();
		if(actual_String3.equals(expected_String3)){
		System.out.println("Nathan Mintah is one of the Non-executive board members of Entersekt.");}
        else{
		System.out.println("Nathan Mintah is not the Non-executive board members of Entersekt.");}
		
		String expected_String4 = "WILLEM VAN BILJON";
		String actual_String4 = driver.findElement(By.xpath(".//*[@id='features']/descendant::span[text()='Willem van Biljon']")).getText();
		if(actual_String4.equals(expected_String4)){
		System.out.println("Willem van Biljon is one of the Non-executive board members of Entersekt.");}
        else{
		System.out.println("Willem van Biljon is not the Non-executive board members of Entersekt.");}
		
		String expected_String5 = "ANDREAS VON BLOTTNITZ";
		String actual_String5 = driver.findElement(By.xpath(".//*[@id='features']/descendant::span[text()='Andreas von Blottnitz']")).getText();
		if(actual_String5.equals(expected_String5)){
		System.out.println("Andreas von Blottnitz is one of the Non-executive board members of Entersekt.");}
        else{
		System.out.println("Andreas von Blottnitz is not the Non-executive board members of Entersekt.");}
		 	
	}

}
