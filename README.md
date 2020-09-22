<div align="center">

## Asm in C\+\+


</div>

### Description

This code shows how to add asm to your c++ code
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[\_AuC\_](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/auc.md)
**Level**          |Beginner
**User Rating**    |3.0 (9 globes from 3 users)
**Compatibility**  |Microsoft Visual C\+\+
**Category**       |[Math](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/math__3-12.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/auc-asm-in-c__3-5057/archive/master.zip)

### API Declarations

```
#include <iostream.h>
```


### Source Code

```
#include <iostream.h>
//---------------------------------------
// This code will add number and number2
//---------------------------------------
int add(int number, int number2)
{
	int answer;
	//Start of asm code
	_asm{
		MOV	EAX, number;
		MOV EBX, number2;
		ADD EAX, EBX;
		MOV answer, EAX;
	}
	return answer;
}
//---------------------------------------
// Entry point of our program
//---------------------------------------
int main(int argc, char* argv[])
{
	int number;
	int number2;
	int answer;
	// Ask the user to enter a number
	cout << "Enter a number: ";
	cin >> number;
	// Ask the user to enter a second number
	cout << "\n\nEnter another number: ";
	cin >> number2;
	// Now add number and number 2
	answer = add(number, number2);
	// Show the answer on screen
	cout << "\n\n" << number << " and " << number2 << " is " << answer << endl;
	return 0;
}
```

