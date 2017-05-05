LOAD Value behavior:
All loading are expected to be called when the read head is pointing at or before the $ sign.
After LOAD is called, the read head will be pointing at the "destination" Register character, 
NOT it's content, NOR the Assembly Code Sector
(e.g. #LAV will make the read head point at 'a' after it's done)

As of 5/4/2017: 
there is no implementation to throw an error (or something) when there is an overflow. 
When the register is full, it will simply point back to the Register character.

Test Run instruction:
feel free to use Reg_Tester.jff to test the LOAD jffs. 
testRun.txt provided my previous test cases for your convenient.
(some inner Register, i.e. CR, DR, is more than 10 character long in some of my test cases. 
those are for overflow testing purposes)
