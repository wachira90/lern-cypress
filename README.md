# lern-cypress
lerning cypress Automate Test software

## test login and cap

```javascript
describe('Login', () => {
  it('Logs in and captures a screenshot', () => {
    // Visit the login page
    cy.visit('/login')

    // Fill in the username and password fields
    cy.get('#username').type('myusername')
    cy.get('#password').type('mypassword')

    // Click the login button
    cy.get('#login-button').click()

    // Verify that we are logged in by checking for a welcome message
    cy.contains('Welcome, myusername!')

    // Capture a screenshot of the logged in page
    cy.screenshot('logged-in-page')
  })
})
```
