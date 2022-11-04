describe('Scenarijus', () => {
  it('Atidaryti BasicCalculator', () => {
  cy.visit('https://testsheepnz.github.io/BasicCalculator') 
})
it('Pasirinkti Prototipa', () => {
  cy.get('#selectBuild').select('Prototype')
}) 
  it('Skaiciai Substract', () => {
  cy.get('#number1Field').type('2')
  cy.get('#number2Field').type('3') 
  cy.get('#selectOperationDropdown').select('Subtract')
  cy.get('#calculateButton').click()
  cy.get('#numberAnswerField').should('have.value','-1')
  cy.contains('Answer')
  cy.get('.col-sm-7 > span').click()
  cy.get('#clearButton').click() 
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input
})   
it('Po kablelio Substract', () => {
  cy.get('#number1Field').type('0.1')
  cy.get('#number2Field').type('0.3') 
  cy.get('#selectOperationDropdown').select('Subtract')
  cy.get('#calculateButton').click()
  cy.get('#numberAnswerField').should('have.value','-0.19999999999999998')
  cy.contains('Answer')
  cy.get('#clearButton').click() 
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input
})   
it('0 Substract', () => {
  cy.get('#number1Field').type('0')
  cy.get('#number2Field').type('0') 
  cy.get('#selectOperationDropdown').select('Subtract')
  cy.get('#calculateButton').click()
  cy.get('#numberAnswerField').should('have.value','0')
  cy.contains('Answer')
  cy.get('.col-sm-7 > span').click()
  cy.get('#clearButton').click() 
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input
})   
it('Raide Substract', () => {
  cy.get('#number1Field').type('a')
  cy.get('#number2Field').type('1') 
  cy.get('#selectOperationDropdown').select('Subtract')
  cy.get('#calculateButton').click()
  cy.get('#errorMsgField').should('be.visible')
  cy.contains('Answer')
  cy.get('.col-sm-7 > span').click()
  cy.get('#clearButton').click() 
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input
})   
it('Element Substract', () => {
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input
  cy.get('#number1Field').should('be.visible')
  cy.get('#number2Field').should('be.visible')
  cy.get('#number1Field').type('3')
  cy.get('#number2Field').type('2')
  cy.get('#selectOperationDropdown').select('Subtract')
  cy.get('#calculateButton').click().should('be.visible') 
  cy.get('#numberAnswerField').should('have.value','1')
  cy.contains('Answer')
  cy.get('.col-sm-7 > span').click()
  cy.get('#clearButton').click() 
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input 
  })
  it('Skaiciai Multiply', () => {
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input
  cy.get('#number1Field').type('3')
  cy.get('#number2Field').type('2') 
  cy.get('#selectOperationDropdown').select('Multiply')
  cy.get('#calculateButton').click()
  cy.get('#numberAnswerField').should('have.value','6')
  cy.contains('Answer')
  cy.get('.col-sm-7 > span').click()
  cy.get('#clearButton').click() 
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input 
  })
  it('Po kablelio Multiply', () => {
    cy.get('#number1Field').type('0.1')
    cy.get('#number2Field').type('0.3') 
    cy.get('#selectOperationDropdown').select('Multiply')
    cy.get('#calculateButton').click()
    cy.get('#numberAnswerField').should('have.value','0.03')
    cy.contains('Answer')
    cy.get('#clearButton').click() 
    cy.get('#number1Field').clear() // Clear text input
    cy.get('#number2Field').clear() // Clear text input
  })   
  it('0 Multiply', () => {
    cy.get('#number1Field').type('0')
    cy.get('#number2Field').type('0') 
    cy.get('#selectOperationDropdown').select('Multiply')
    cy.get('#calculateButton').click()
    cy.get('#numberAnswerField').should('have.value','0')
    cy.contains('Answer')
    cy.get('.col-sm-7 > span').click()
    cy.get('#clearButton').click() 
    cy.get('#number1Field').clear() // Clear text input
    cy.get('#number2Field').clear() // Clear text input
  })   
  it('Raide Multiply', () => {
    cy.get('#number1Field').type('a')
    cy.get('#number2Field').type('1') 
    cy.get('#selectOperationDropdown').select('Multiply')
    cy.get('#calculateButton').click()
    cy.get('#errorMsgField').should('be.visible')
    cy.contains('Answer')
    cy.get('.col-sm-7 > span').click()
    cy.get('#clearButton').click() 
    cy.get('#number1Field').clear() // Clear text input
    cy.get('#number2Field').clear() // Clear text input
  })   
  it('Element Multiply', () => {
    cy.get('#number1Field').clear() // Clear text input
    cy.get('#number2Field').clear() // Clear text input
    cy.get('#number1Field').should('be.visible')
    cy.get('#number2Field').should('be.visible')
    cy.get('#number1Field').type('3')
    cy.get('#number2Field').type('2')
    cy.get('#selectOperationDropdown').select('Multiply')
    cy.get('#calculateButton').click().should('be.visible') 
    cy.get('#numberAnswerField').should('have.value','6')
    cy.contains('Answer')
    cy.get('.col-sm-7 > span').click()
    cy.get('#clearButton').click() 
    cy.get('#number1Field').clear() // Clear text input
    cy.get('#number2Field').clear() // Clear text input 
    })
it('Skaiciai Add', () => {
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input
  cy.get('#number1Field').type('1')
  cy.get('#number2Field').type('3') 
  cy.get('#selectOperationDropdown').select('Add')
  cy.get('#calculateButton').click()
  cy.get('#numberAnswerField').should('have.value','4')
  cy.contains('Answer')
  cy.get('.col-sm-7 > span').click()
  cy.get('#clearButton').click() 
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input 
  })
  it('Po kablelio Add ', () => {
    cy.get('#number1Field').type('0.1')
    cy.get('#number2Field').type('0.3') 
    cy.get('#selectOperationDropdown').select('Add')
    cy.get('#calculateButton').click()
    cy.get('#numberAnswerField').should('have.value','0.4')
    cy.contains('Answer')
    cy.get('#clearButton').click() 
    cy.get('#number1Field').clear() // Clear text input
    cy.get('#number2Field').clear() // Clear text input
  })   
  it('0 Add', () => {
    cy.get('#number1Field').type('0')
    cy.get('#number2Field').type('0') 
    cy.get('#selectOperationDropdown').select('Add')
    cy.get('#calculateButton').click()
    cy.get('#numberAnswerField').should('have.value','0')
    cy.contains('Answer')
    cy.get('.col-sm-7 > span').click()
    cy.get('#clearButton').click() 
    cy.get('#number1Field').clear() // Clear text input
    cy.get('#number2Field').clear() // Clear text input
  })   
  it('Raide Add', () => {
    cy.get('#number1Field').type('a')
    cy.get('#number2Field').type('1') 
    cy.get('#selectOperationDropdown').select('Add')
    cy.get('#calculateButton').click()
    cy.get('#errorMsgField').should('be.visible')
    cy.contains('Answer')
    cy.get('.col-sm-7 > span').click()
    cy.get('#clearButton').click() 
    cy.get('#number1Field').clear() // Clear text input
    cy.get('#number2Field').clear() // Clear text input
  })   
  it('Element Add', () => {
    cy.get('#number1Field').clear() // Clear text input
    cy.get('#number2Field').clear() // Clear text input
    cy.get('#number1Field').should('be.visible')
    cy.get('#number2Field').should('be.visible')
    cy.get('#number1Field').type('3')
    cy.get('#number2Field').type('2')
    cy.get('#selectOperationDropdown').select('Add')
    cy.get('#calculateButton').click().should('be.visible') 
    cy.get('#numberAnswerField').should('have.value','5')
    cy.contains('Answer')
    cy.get('.col-sm-7 > span').click()
    cy.get('#clearButton').click() 
    cy.get('#number1Field').clear() // Clear text input
    cy.get('#number2Field').clear() // Clear text input 
    })  
it('Skaiciai Concatenate', () => {
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input
  cy.get('#number1Field').type('4')
  cy.get('#number2Field').type('2') 
  cy.get('#selectOperationDropdown').select('Concatenate')
  cy.get('#calculateButton').click()
  cy.get('#numberAnswerField').should('have.value','42')
  cy.contains('Answer')
  cy.get('#clearButton').click() 
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input 
  })
  it('Raide Concatenate', () => {
    cy.get('#number1Field').type('a')
    cy.get('#number2Field').type('1') 
    cy.get('#selectOperationDropdown').select('Concatenate')
    cy.get('#calculateButton').click()
    cy.get('#numberAnswerField').should('have.value','a1')
    cy.contains('Answer')
    cy.get('#clearButton').click() 
    cy.get('#number1Field').clear() // Clear text input
    cy.get('#number2Field').clear() // Clear text input
  })   
  it('Po kablelio Concatenate', () => {
    cy.get('#number1Field').type('0.1')
    cy.get('#number2Field').type('0.3') 
    cy.get('#selectOperationDropdown').select('Concatenate')
    cy.get('#calculateButton').click()
    cy.get('#numberAnswerField').should('have.value','0.10.3')
    cy.contains('Answer')
    cy.get('#clearButton').click() 
    cy.get('#number1Field').clear() // Clear text input
    cy.get('#number2Field').clear() // Clear text input
  })   
  it('0 Concatenate', () => {
    cy.get('#number1Field').type('0')
    cy.get('#number2Field').type('0') 
    cy.get('#selectOperationDropdown').select('Concatenate')
    cy.get('#calculateButton').click()
    cy.get('#numberAnswerField').should('have.value','00')
    cy.contains('Answer')
    cy.get('#clearButton').click() 
    cy.get('#number1Field').clear() // Clear text input
    cy.get('#number2Field').clear() // Clear text input
  })   
  it('Element Concatenate', () => {
    cy.get('#number1Field').clear() // Clear text input
    cy.get('#number2Field').clear() // Clear text input
    cy.get('#number1Field').should('be.visible')
    cy.get('#number2Field').should('be.visible')
    cy.get('#number1Field').type('3')
    cy.get('#number2Field').type('2')
    cy.get('#selectOperationDropdown').select('Concatenate')
    cy.get('#calculateButton').click().should('be.visible') 
    cy.get('#numberAnswerField').should('have.value','32')
    cy.contains('Answer')
    cy.get('#clearButton').click() 
    cy.get('#number1Field').clear() // Clear text input
    cy.get('#number2Field').clear() // Clear text input 
    })  
  it('Skaiciai Divide', () => {
    cy.get('#number1Field').clear() // Clear text input
    cy.get('#number2Field').clear() // Clear text input
    cy.get('#number1Field').type('6')
    cy.get('#number2Field').type('2') 
    cy.get('#selectOperationDropdown').select('Divide')
    cy.get('#calculateButton').click()
    cy.get('#numberAnswerField').should('have.value','3')
    cy.contains('Answer')
    cy.get('.col-sm-7 > span').click()
    cy.get('#clearButton').click() 
    cy.get('#number1Field').clear() // Clear text input
    cy.get('#number2Field').clear() // Clear text input 
    })
  it('Po kablelio Divide', () => {
    cy.get('#number1Field').type('0.1')
    cy.get('#number2Field').type('0.3') 
    cy.get('#selectOperationDropdown').select('Divide')
    cy.get('#calculateButton').click()
    cy.get('#numberAnswerField').should('have.value','0.33333333333333337')
    cy.contains('Answer')
    cy.get('#clearButton').click() 
    cy.get('#number1Field').clear() // Clear text input
    cy.get('#number2Field').clear() // Clear text input
    })   
  it('0 Divide', () => {
    cy.get('#number1Field').type('0')
    cy.get('#number2Field').type('1') 
    cy.get('#selectOperationDropdown').select('Divide')
    cy.get('#calculateButton').click()
    cy.get('#numberAnswerField').should('have.value','0')
    cy.contains('Answer')
    cy.get('.col-sm-7 > span').click()
    cy.get('#clearButton').click() 
    cy.get('#number1Field').clear() // Clear text input
    cy.get('#number2Field').clear() // Clear text input
    })   
    it('Divide 0', () => {
      cy.get('#number1Field').type('8')
      cy.get('#number2Field').type('0') 
      cy.get('#selectOperationDropdown').select('Divide')
      cy.get('#calculateButton').click()
      cy.get('#errorMsgField').should('be.visible')
      cy.get('#number1Field').clear() // Clear text input
      cy.get('#number2Field').clear() // Clear text input
      })   
  it('Raide Divide', () => {
    cy.get('#number1Field').type('a')
    cy.get('#number2Field').type('1') 
    cy.get('#selectOperationDropdown').select('Divide')
    cy.get('#calculateButton').click({force:true})
    cy.get('#errorMsgField').should('be.visible')
    cy.contains('Answer')
    cy.get('.col-sm-7 > span').click({force:true})
    cy.get('#clearButton').click({force:true}) 
    cy.get('#number1Field').clear({force:true}) // Clear text input
    cy.get('#number2Field').clear({force:true}) // Clear text input
  })     
  it('Element Divide', () => {
    cy.get('#number1Field').clear() // Clear text input
    cy.get('#number2Field').clear() // Clear text input
    cy.get('#number1Field').should('be.visible')
    cy.get('#number2Field').should('be.visible')
    cy.get('#number1Field').type('4')
    cy.get('#number2Field').type('2')
    cy.get('#selectOperationDropdown').select('Divide')
    cy.get('#calculateButton').click({force:true}).should('be.visible') 
    cy.get('#numberAnswerField').should('have.value','')
    cy.contains('Answer')
    cy.get('#number1Field').clear() // Clear text input
    cy.get('#number2Field').clear() // Clear text input 
    })  
it('Pasirinkti', () => {
  cy.get('#selectBuild').select('1')
}) 
 
it('Build 1 Add Apvalinimas', () => {
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input
  cy.get('#number1Field').type('0.77744444')
  cy.get('#number2Field').type('0.10000000') 
  cy.get('#selectOperationDropdown').select('Add')
  cy.get('#calculateButton').click()
  cy.get('#numberAnswerField').should('have.value','1')
  cy.contains('Answer')
  cy.get('.col-sm-7 > span').click()
  cy.get('#clearButton').click() 
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input 
  })
it('Raide Add', () => {
  cy.get('#number1Field').type('a')
  cy.get('#number2Field').type('1') 
  cy.get('#selectOperationDropdown').select('Add')
  cy.get('#calculateButton').click()
  cy.get('#errorMsgField').should('be.visible')
  cy.contains('Answer')
  cy.get('.col-sm-7 > span').click()
  cy.get('#clearButton').click() 
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input
  })     
it('Build 1 Concatenate', () => {
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input
  cy.get('#number1Field').type('4')
  cy.get('#number2Field').type('2') 
  cy.get('#selectOperationDropdown').select('Concatenate')
  cy.get('#calculateButton').click()
  cy.get('#numberAnswerField').should('have.value','42')
  cy.contains('Answer')
  cy.get('#clearButton').click() 
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input 
  })

it('Pasirinkti', () => {
  cy.get('#selectBuild').select('2')
}) 
  it('Build 2 Substract', () => {
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input
  cy.get('#number1Field').type('2')
  cy.get('#number2Field').type('3') 
  cy.get('#selectOperationDropdown').select('Subtract')
  cy.get('#calculateButton').click()
  cy.get('#numberAnswerField').should('have.value','-1')
  cy.contains('Answer')
  cy.get('.col-sm-7 > span').click()
  cy.get('#clearButton').click() 
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input
})   
  it('Build 2 Multiply', () => {
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input
  cy.get('#number1Field').type('3')
  cy.get('#number2Field').type('2') 
  cy.get('#selectOperationDropdown').select('Multiply')
  cy.get('#calculateButton').click()
  cy.get('#numberAnswerField').should('have.value','6')
  cy.contains('Answer')
  cy.get('.col-sm-7 > span').click()
  cy.get('#clearButton').click() 
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input 
  })
it('Build 2 Add', () => {
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input
  cy.get('#number1Field').type('1')
  cy.get('#number2Field').type('2') 
  cy.get('#selectOperationDropdown').select('Add')
  cy.get('#calculateButton').click()
  cy.get('#numberAnswerField').should('have.value','3')
  cy.contains('Answer')
  cy.get('.col-sm-7 > span').click()
  cy.get('#clearButton').click() 
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input 
  })
    
it('Build 2 Concatenate', () => {
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input 
  cy.get('#number1Field').type('4')
  cy.get('#number2Field').type('2') 
  cy.get('#selectOperationDropdown').select('Concatenate')
  cy.get('#calculateButton').click()
  cy.get('#numberAnswerField').should('have.value','42')
  cy.contains('Answer')
  cy.get('#clearButton').click() 
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input 
  })

it('Pasirinkti', () => {
  cy.get('#selectBuild').select('3')
}) 
  it('Build 3 Substract', () => {
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input
  cy.get('#number1Field').type('2')
  cy.get('#number2Field').type('3') 
  cy.get('#selectOperationDropdown').select('Subtract')
  cy.get('#calculateButton').click()
  cy.get('#numberAnswerField').should('have.value','-1')
  cy.contains('Answer')
  cy.get('.col-sm-7 > span').click()
  cy.get('#clearButton').click() 
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input
})   
  it('Build 3 Multiply', () => {
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input
  cy.get('#number1Field').type('3')
  cy.get('#number2Field').type('2') 
  cy.get('#selectOperationDropdown').select('Multiply')
  cy.get('#calculateButton').click()
  cy.get('#numberAnswerField').should('have.value','6')
  cy.contains('Answer')
  cy.get('.col-sm-7 > span').click()
  cy.get('#clearButton').click() 
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input 
  })
it('Build 3 Add', () => {
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input
  cy.get('#number1Field').type('0.1')
  cy.get('#number2Field').type('0.2') 
  cy.get('#selectOperationDropdown').select('Add')
  cy.get('#calculateButton').click()
  cy.get('#numberAnswerField').should('have.value','0.30000000000000004')
  cy.contains('Answer')
  cy.get('#clearButton').click() 
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input 
  })

  it('Build 3 raide Concatenate', () => {
    cy.get('#number1Field').type('a')
    cy.get('#number2Field').type('1') 
    cy.get('#selectOperationDropdown').select('Concatenate')
    cy.get('#calculateButton').click()
    cy.get('#numberAnswerField').should('have.value','a1')
    cy.contains('Answer')
    cy.get('#clearButton').click() 
    cy.get('#number1Field').clear() // Clear text input
    cy.get('#number2Field').clear() // Clear text input
  })   
it('Pasirinkti', () => {
  cy.get('#selectBuild').select('4')
}) 
  it('Build 4 Substract', () => {
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input
  cy.get('#number1Field').type('2')
  cy.get('#number2Field').type('3') 
  cy.get('#selectOperationDropdown').select('Subtract')
  cy.get('#calculateButton').click()
  cy.get('#numberAnswerField').should('have.value','-1')
  cy.contains('Answer')
  cy.get('.col-sm-7 > span').click()
  cy.get('#clearButton').click() 
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input
})   
  it('Build 4 Multiply', () => {
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input
  cy.get('#number1Field').type('3')
  cy.get('#number2Field').type('2') 
  cy.get('#selectOperationDropdown').select('Multiply')
  cy.get('#calculateButton').click()
  cy.get('#numberAnswerField').should('have.value','6')
  cy.contains('Answer')
  cy.get('.col-sm-7 > span').click()
  cy.get('#clearButton').click() 
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input 
  })
it('Build 4 Add', () => {
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input
  cy.get('#number1Field').type('1')
  cy.get('#number2Field').type('2') 
  cy.get('#selectOperationDropdown').select('Add')
  cy.get('#calculateButton').click()
  cy.get('#numberAnswerField').should('have.value','3')
  cy.contains('Answer')
  cy.get('.col-sm-7 > span').check()
  cy.get('#clearButton').click() 
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input 
  })
    
it('Build 4 Concatenate', () => {
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input
  cy.get('#number1Field').type('a')
  cy.get('#number2Field').type('2') 
  cy.get('#selectOperationDropdown').select('Concatenate')
  cy.get('#calculateButton').click()
  cy.get('#numberAnswerField').should('not.have.value')
  cy.contains('Answer')
  cy.get('#clearButton').click() 
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input 
  })

it('Pasirinkti', () => {
  cy.get('#selectBuild').select('5')
}) 
  it('Build 5 Substract', () => {
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input
  cy.get('#number1Field').type('2')
  cy.get('#number2Field').type('3') 
  cy.get('#selectOperationDropdown').select('Subtract')
  cy.get('#calculateButton').click()
  cy.get('#numberAnswerField').should('have.value','-1')
  cy.contains('Answer')
  cy.get('.col-sm-7 > span').click()
  cy.get('#clearButton').check() 
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input
})   
  it('Build 5 Multiply', () => {
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input
  cy.get('#number1Field').type('3')
  cy.get('#number2Field').type('2') 
  cy.get('#selectOperationDropdown').select('Multiply')
  cy.get('#calculateButton').click()
  cy.get('#numberAnswerField').should('have.value','6')
  cy.contains('Answer')
  cy.get('.col-sm-7 > span').click()
  cy.get('#clearButton').click() 
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input 
  })
it('Build 5 Add', () => {
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input
  cy.get('#number1Field').type('1')
  cy.get('#number2Field').type('2') 
  cy.get('#selectOperationDropdown').select('Add')
  cy.get('#calculateButton').click()
  cy.get('#numberAnswerField').should('have.value','3')
  cy.contains('Answer')
  cy.get('.col-sm-7 > span').click()
  cy.get('#clearButton').click() 
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input 
  })
    
it('Build 5 Concatenate', () => {
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input
  cy.get('#number1Field').type('4')
  cy.get('#number2Field').type('2') 
  cy.get('#selectOperationDropdown').select('Concatenate')
  cy.get('#calculateButton').click()
  cy.get('#numberAnswerField').should('have.value','42')
  cy.contains('Answer')
  cy.get('#clearButton').click() 
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input 
  })

it('Pasirinkti', () => {
  cy.get('#selectBuild').select('6')
}) 
it('Buils 6 Divide', () => {
  cy.get('#number1Field').type('8')
  cy.get('#number2Field').type('0') 
  cy.get('#selectOperationDropdown').select('Divide')
  cy.get('#calculateButton').click()
  cy.get('#errorMsgField').should('be.visible')
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input
  })     
  it('Build 6 Substract', () => {
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input
  cy.get('#number1Field').type('2')
  cy.get('#number2Field').type('3') 
  cy.get('#selectOperationDropdown').select('Subtract')
  cy.get('#calculateButton').click()
  cy.get('#numberAnswerField').should('have.value','-1')
  cy.contains('Answer')
  cy.get('.col-sm-7 > span').click()
  cy.get('#clearButton').click() 
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input
})   
  it('Build 6 Multiply', () => {
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input
  cy.get('#number1Field').type('3')
  cy.get('#number2Field').type('2') 
  cy.get('#selectOperationDropdown').select('Multiply')
  cy.get('#calculateButton').click()
  cy.get('#numberAnswerField').should('have.value','6')
  cy.contains('Answer')
  cy.get('.col-sm-7 > span').click()
  cy.get('#clearButton').click() 
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input 
  })
it('Build 6 Add', () => {
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input
  cy.get('#number1Field').type('2')
  cy.get('#number2Field').type('2') 
  cy.get('#selectOperationDropdown').select('Add')
  cy.get('#calculateButton').click()
  cy.get('#numberAnswerField').should('have.value','4')
  cy.contains('Answer')
  cy.get('.col-sm-7 > span').click()
  cy.get('#clearButton').click() 
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input 
  })
it('Build 6 Concatenate', () => {
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input
  cy.get('#number1Field').type('4')
  cy.get('#number2Field').type('2') 
  cy.get('#selectOperationDropdown').select('Concatenate')
  cy.get('#calculateButton').click()
  cy.get('#numberAnswerField').should('have.value','42')
  cy.contains('Answer')
  cy.get('#clearButton').click() 
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input 
  })

it('Pasirinkti prototipa', () => {
  cy.get('#selectBuild').select('7')
}) 
  it('Build 7 Multiply', () => {
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input
  cy.get('#number1Field').type('3')
  cy.get('#number2Field').type('2') 
  cy.get('#selectOperationDropdown').select('Multiply')
  cy.get('#calculateButton').click()
  cy.get('#numberAnswerField').should('have.value','6')
  cy.contains('Answer')
  cy.get('.col-sm-7 > span').click()
  cy.get('#clearButton').click() 
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input 
  })
it('Build 7 Add', () => {
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input 
  cy.get('#number1Field').type('1')
  cy.get('#number2Field').type('2') 
  cy.get('#selectOperationDropdown').select('Add')
  cy.get('#calculateButton').click()
  cy.get('#numberAnswerField').should('have.value','3')
  cy.contains('Answer')
  cy.get('.col-sm-7 > span').click()
  cy.get('#clearButton').click() 
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input 
  })
    
it('Build 7 Concatenate', () => {
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input
  cy.get('#number1Field').type('4')
  cy.get('#number2Field').type('2') 
  cy.get('#selectOperationDropdown').select('Concatenate')
  cy.get('#calculateButton').click()
  cy.get('#numberAnswerField').should('have.value','42')
  cy.contains('Answer')
  cy.get('#clearButton').click() 
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input 
  })

it('Pasirinkti', () => {
  cy.get('#selectBuild').select('8')
}) 
  it('Build 8 Substract', () => {
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input
  cy.get('#number1Field').type('2')
  cy.get('#number2Field').type('3') 
  cy.get('#selectOperationDropdown').select('Subtract')
  cy.get('#calculateButton').click()
  cy.get('#numberAnswerField').should('have.value','-1')
  cy.contains('Answer')
  cy.get('.col-sm-7 > span').click()
  cy.get('#clearButton').click() 
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input
})   
it('Build 8 Concatenate', () => {
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input
  cy.get('#number1Field').type('4')
  cy.get('#number2Field').type('2') 
  cy.get('#selectOperationDropdown').select('Concatenate')
  cy.get('#calculateButton').click()
  cy.get('#numberAnswerField').should('have.value','42')
  cy.contains('Answer')
  cy.get('#clearButton').click() 
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input 
 })

  it('Pasirinkti', () => {
  cy.get('#selectBuild').select('9')
}) 
  it('Build 9 Multiply', () => {
  cy.get('#number1Field').should('be.visible')
  cy.get('#number2Field').should('be.visible')
  cy.get('#number1Field').type('3')
  cy.get('#number2Field').type('2')
  cy.get('#selectOperationDropdown').select('Multiply')
  cy.get('#calculateButton').click().should('be.visible') 
  cy.get('#numberAnswerField').should('have.value','6')
  cy.contains('Answer')
  cy.get('.col-sm-7 > span').click()
  cy.get('#clearButton').click() 
  cy.get('#number1Field').clear() // Clear text input
  cy.get('#number2Field').clear() // Clear text input 
  })

})
