# TestCafe-Example

selectbox-spec.js
describe('Select box', () => {
  it('should pick an option from select box', () => {
    cy.visit('https://devexpress.github.io/testcafe/example/')
    cy.get('#preferred-interface').select('JavaScript API')      
    cy.get('#preferred-interface').should('have.value', 'JavaScript API')
  })
})

-------

slider.spec.js
describe('Slider', () => {
  it('should pick a value on slider', () => {                     
      cy.visit('https://devexpress.github.io/testcafe/example/')
      cy.get('#tried-test-cafe').click()                          
      cy.contains('5').click()                                    
  })
})

-------

submit.spec.js
describe('Submit form', () => {
  it('should fill and submit developer name', () => {
    cy.visit('https://devexpress.github.io/testcafe/example/')    
    cy.get('#developer-name').type('mike')                        
    cy.get('#tried-test-cafe').click()                            
    cy.get('#submit-button').click()                              
    cy.get('#article-header').contains('Thank you')
  })
})


