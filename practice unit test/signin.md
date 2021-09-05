# Glossary of terms

## Components

The key components of Jasmine Syntax - Suites, Specs, Expectations and Matchers

* ### Suites

  To test the code or checking project steps using jasmine.

  Create a jasmine with the syntax

  "describe"

  It begins with a call to the global Jasmine function which describe the two parameters:

  "string" and "function"

  The string is a name or title for a spec suite what is being tested.

  The function is a block of code that implements the suite or testing the code.

* ### Specs

  It is defined by calling the global Jasmine function "it".

  The Syntax will be like this

```ruby
describe("About the main process", function(){

 it("about the function", function(){
   
     a = true;
       
     expect(a).toBe(true);
       
  });
   
});
```
* ### Expectations

  Expectations is described as "expect" inside the function which takes a value, called  as "toBe". An expectation is an assertion that is either true or false. 

* ### Matchers

  It is a comparison between the actual value and the expected value either if the expectation is "true" or "false".

* ### Use Cases

  * A Signin component case is below:

  * User gets logged in filling credentials.

* ### User Behaviour

  * Enter email and password Details
   
  * Click on login Button


```ruby
import { TestBed, ComponentFixture, inject, async } from '@angular/core/testing';

import { Loginmethod, User } from './signin.component';

describe('Component: signin', () => {

    let component: signinComponent;

    let fixture: ComponentFixture<signinComponent>;

     beforeEach(() => {
```

> refine the test module by declaring the test component
```ruby       
        TestBed.configureTestingModule({
        
            declarations: [signinComponent]
            
        });

```
> create component and test fixture

```ruby    
        fixture = TestBed.createComponent(signinComponent);
 ```       
> get test component from the fixture


```ruby        
        component = fixture.componentInstance;
        
```     

```ruby
       it('Entering valid email and valid password gets user loggedIn ', () => {
         
            let user: User;
        
            signin.email.value = "xyz@campustrack.net";
        
            sigin.password.value = "123456";
           
            user.clickSignIn();
        
            expect(user.valid.email).toBe(true,'xyz@campustrack.net');
     
            expect(user.valid.password).toBe(true, '123456');
        
        };
        
       it('Entering Invalid email or password or both user gets error message, () => {
         
            let user: User;
     
            signin.email.value = " ";
        
            signin.password.value = " ";
        
            user.clickSignIn();
         
            expect(login.getErrorMessage()).toEqual(
        
           'Invalid email or password.'
      );
        
     });
     
     });
        
```


