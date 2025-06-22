# 🏥 CURA Healthcare Test Automation



Automated testing framework for CURA Healthcare Service's appointment scheduling system using Selenium WebDriver and Java.

## 🚀 Key Features
- **End-to-End Workflow Testing**: Appointment booking, facility selection, and medical history submission
- **Advanced POM Architecture**: Enhanced Page Object Model with reusable components
- **Dynamic Data Handling**: JSON/Excel test data integration
- **Cross-Browser Testing**: Chrome/Firefox/Edge support via WebDriverManager
- **Failure Analysis**: Automatic screenshot capture for test failures

## 🛠️ Tech Stack
- **Core**: Selenium WebDriver 4.x, Java 11+
- **Testing**: TestNG, Maven
- **Utilities**: WebDriverManager (auto-driver setup), ExtentReports (visual reporting)
- **CI/CD**: GitHub Actions integration

## 📦 Setup & Execution
```bash
git clone https://github.com/surajharogoppa/CURAHealthcareAutomation.git
cd CURAHealthcareAutomation
mvn clean test
🌟 Sample Test Case

@Test(dataProvider = "appointmentData")
public void bookAppointment(String facility, String visitDate, String comment) {
    LoginPage.login("username", "password");
    new AppointmentPage()
        .selectFacility(facility)
        .setVisitDate(visitDate)
        .addComment(comment)
        .confirmBooking();
}
📂 Project Structure

src/
├── main/java/
│   ├── pages/          # POM classes
│   │   ├── core/       # Base pages
│   │   └── components/ # UI widgets
│   └── utilities/      # Helpers
└── test/java/
    ├── testdata/       # JSON/Excel files
    ├── tests/          # Test classes
    └── listeners/      # TestNG listeners
