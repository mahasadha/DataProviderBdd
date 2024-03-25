#Data Provider with Cucumber BDD

Using Apache POI integrated with Cucumber / Selenium, Integrate a data provider for feeding the test data into the testing platform 
Feature: Login Functionality Test

Scenario Outline: Login with Different Credentials
  Given I am on the login page
  When I enter username "<username>" and password "<password>"
  Then I should <expected_result>

  Examples:
    | username           | password    | expected_result            |
    | "abc@gmail.com"    | "12345"     | "see an error message"     |
    | "abd@gmail.com"    | "9876"      | "see an error message"     |
    | "mahasadha201@gmail.com"  | "Ssvm#4036"    | "be logged in successfully"|
