## Target to write clean code (Java)

### 1. Variable/Method Names

Variable holds a piece of data value and using good variable names improves readability.

Bad variable/method names
```
Boolean isRequired = true;

public Boolean isRequired () {
    # logic goes here
	return isRequired;
}

int primAccntSortCd;
```

Good variable/method names
```
Boolean isAuthenticationRequired = true;

public Boolean isAuthenticationRequired () {
    # logic goes here
	return isAuthenticationRequired;
}

int primaryAccountSortCode;
```

The variable/method name here provides more readability and will more or less tells us the functionality in the method.

Use verbs for function names and nouns for classes and attributes
```
public int hikeProductPrice(int productPrice, int dollarsToAddToPrice) {
	return (dollarsToAddToPrice*1.5) + (productPrice*2.32);
}
```
### 2. Use one word per concept
Be consistent. For example, don’t use get and fetch to do the same thing in different classes for different method names.

### 3. Keep it simple
Keep the code as simple as you can. Instead of having multiple lines of code in a single file, move them to functions, so that the code can be reusable

* A function should only do one thing
* No nested control structure
* Less arguments are better
* No side effects - Functions should always do what the name suggests

Example
```
if(isSecurityCheckRequired) {
	// Logic goes here
}
```
Instead of writing logic inside if, call a method that processes the logic 
```
if(isSecurityCheckRequired) {
	doSecurityValidations();
}
```
This makes the code look more readable.

### 4. Include code comments wherever required

Code comments in any programming language helps in understanding the functionality of the method. Ideally, code should speak, but we will get a naive idea from the comments.

Method functionality has to be called out in the comments
```
// if we sort the array here the logic becomes simpler in calculatePayment() method
```
Warn of consequences in comments
```
// this script will take a very long time to run
```
Emphasise important points in comments
```
// the trim function is very important, in most cases the username has a trailing space
```
Noise comments are bad. For example:
```
/** The day of the month. */
int dayOfMonth;
```
##### Any comments other than the above should be avoided
##### Never leave code commented
### 5. Code Smells
Avoid the below code smells.
```
 * Dead code - The code that is not reachable
 * Speculative Generality - no need “what if?”
 * Large classes - Classes with more than 200+ lines of code
 * Multiple languages in one file - Plain java code move out of Storm class
 * Long if conditions - replace with appropriate functions 
 * Hard-coding - Avoid hard coding variables
```
### 6. Logging

Logging in simple words refers to the recording of an application activity and is used to store exceptions, information, and warnings as messages that occur during the execution of a program. Logging helps a programmer in the debugging process of a program.

```
LOGGER.info("Logger Name: ", LOGGER.getName());
LOGGER.warning("Can cause ArrayIndexOutOfBoundsException");

Aug 29, 2017 1:19:30 PM com.lbg.dre.cf.LoggerExample main INFO: Logger Name: com.lbg.dre.cf.LoggerExample
Aug 29, 2017 1:19:31 PM com.lbg.dre.cf.LoggerExample main WARNING: Can cause ArrayIndexOutOfBoundsException
```

### Sources
 * [Clean Code in Agile](http://ricardogeek.com/docs/clean_code.html)
 * [on Git](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-2-coding-style-guide.md)
 * [CodeSniffer](http://docs.joomla.org/Joomla_CodeSniffer)
 * [CodeGeeks](http://www.javacodegeeks.com/2013/02/my-favourite-programming-quotes.html)
