
Components

The key components of Jasmine Syntax - Suites, Specs, Expectations and Matchers

Suites

To test the code or checking project steps using jasmine.

Create a jasmine with the syntax

"describe"

It begins with a call to the global Jasmine function which describe the two parameters:

"string" and "function"

The string is a name or title for a spec suite it is a wording that what is being tested.

The function is a block of code that implements the suite or testing the code.

Specs

It is defined by calling the global Jasmine function "it".

The Syntax will be like this

//////////////////////////////////////////////////////

describe("About the main process", function(){

   it("about the function", function(){
   
       a = true;
       
       expect(a).toBe(true);
       
   });
   
});

//////////////////////////////////////////////////////

Expectations

Expectations is described as "expect" inside the function which takes a value, called the actual value as "toBe". An expectation in Jasmine is an assertion that is either true or false. 

Matchers

It is a comparison between the actual value and the expected value either if the expectation is "true" or "false".


import { TestBed, ComponentFixture, inject, async } from '@angular/core/testing';

import { LoginComponent, User } from './login.component';


``````ruby
describe('Component: Login', () => {

    let component: LoginComponent;
    
    let fixture: ComponentFixture<LoginComponent>;

     beforeEach(() => {

        // refine the test module by declaring the test component
        
        TestBed.configureTestingModule({
        
            declarations: [LoginComponent]
            
        });


        // create component and test fixture
        
        fixture = TestBed.createComponent(LoginComponent);
        
        // get test component from the fixture
        
        component = fixture.componentInstance;
        
         it('Entering valid email and password gets user loggedIn ', () => {
         
        let user: User;
        
        login.value = "xyz@campusrack.net";
        
        password.value = "123456";
        
        expect(user.valid.email).toBe(true,'xyz@campusrack.net');
     
        expect(user.valid.password).toBe(true, '123456');
        
        };
        
      it('Entering Invalid email or password , () => {
         
        let user: User;
        
        login.value = "xyz@campusrack.org";
        
        password.value = "12456";
        
        expect(user.invalid.email).toBe(false, 'xyz@campusrack.net');
     
        expect(user.invaild.password).toBe(false, '123456');  
        
        };
        
         it('Entering Invalid email or password user gets error message, () => {
         
        let user: User;
        
        login.message = "Invalid email or password;
        
        password.message = "Invalid email or password;
        
        expect(user.invalid.email).toBe("Invalid email or password;);
     
        expect(user.invaild.password).toBe("Invalid email or password;);  
        
        };
``````        
        
      


