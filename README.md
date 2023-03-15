# 202001003_Lab5

 Lab-5
SOFTWARE-ENGINEERING



Git Repository-(StackOverFlow--Clone-master)
Tool used-Pylint

Errors in manage.py
![result_manage_py](https://user-images.githubusercontent.com/85830046/225287881-c9c9fea1-9a8b-4899-a59b-b03838fef9a2.PNG)
     

Error in the Line 11:8.
![mange_py_error](https://user-images.githubusercontent.com/85830046/225287941-9075f155-ca4a-4391-801b-16c06b552ed3.png)

Error:”Import outside Top-level”
->The 11th line should be present before def main(),So technically the 11th line should be at 6th position.Because the top level here is def main().
Error is valid.

(2)Errors in views.py:
Result of Pylint analysis
![result_vies_py](https://user-images.githubusercontent.com/85830046/225287972-88321b2a-2e2a-4578-8968-b667ae30b170.png)




Views.py code
![vies_py_error](https://user-images.githubusercontent.com/85830046/225288172-d3538c58-f93f-4ed7-a7c6-ee2bdd5f5fb4.png)



Error Type 1:  views.py:1:0: C0114: Missing module docstring (missing-module-docstring)
->The docstring is a general statement written before a module(typically put in inverted commas) regarding what the module is all about.
It's not necessary everywhere.Error is optional.

Error Type 2:  views.py:6:0: C0103: Function name "read_All_Notifications" doesn't conform to snake_case naming style (invalid-name)
->Here the code def read_All_Priv_Notifications(request):
Every letter after underscore should be a small letter with respect to snake_case naming convention.But we have capital letters, so the error is valid.


Error Type 3 : views.py:3:0: W0611: Unused HttpResponseRedirect imported from django.http (unused-import)
->Here the line 3 code:from django.http import JsonResponse, HttpResponseRedirect, HttpResponse,might not be correct here as in the line 25 and 15 we are returning a json response and json response Http must be imported here for this ,
So it's optional to keep the line 3.

Error type 4:  views.py:8:15: E1101: Class 'Notification' has no 'objects' member (no-member)
->As in the code screenshot we can't see  any member declaration in the ‘notification’ class.
So the error is valid.

Error type 5:  views.py:26:0: C0305: Trailing newlines (trailing-newlines)
->This error has occurred because there is one more line after line 26 ,i,e line 27.Its an empty line, it's not required here.
So this error is more of a kind of warning and amending it is optional.
