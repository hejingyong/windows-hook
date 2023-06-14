# windows-hook

```
#include <iostream>
#include <Windows.h>
using namespace std;
HMODULE hDllLib = NULL;
int main()
{
	hDllLib = ::LoadLibrary(L"F:\\code\\hook_MessageBox\\hook_dll\\Debug\\hook_dll.dll");

	if (hDllLib == NULL)
	{
		MessageBox(NULL, L"加载失败！", L"加载", MB_OK);
	}

	MessageBoxW(NULL, L"hello world", L"flagby", NULL);
	::FreeLibrary(hDllLib);
	MessageBoxW(NULL, L"hello world", L"flagby", NULL);
	MessageBoxW(NULL, L"hello world", L"flagby", NULL);


	
}
```
