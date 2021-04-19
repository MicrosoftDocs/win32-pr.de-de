---
description: Jedem Prozess ist ein Umgebungsblock zugeordnet.
ms.assetid: b428688c-7b16-48c7-8d89-55d066496d1c
title: Ändern von Umgebungsvariablen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e13054afff996c4f8128fdc58f9d6dfadc35cc84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349854"
---
# <a name="changing-environment-variables"></a>Ändern von Umgebungsvariablen

Jedem Prozess ist ein Umgebungsblock zugeordnet. Der Umgebungsblock besteht aus einem null-terminierten Block von null-terminierten Zeichen folgen (d. h., es gibt zwei NULL-Bytes am Ende des Blocks), wobei jede Zeichenfolge in folgendem Format vorliegt:

*Name* = *Wert*

Alle Zeichen folgen im Umgebungsblock müssen alphabetisch nach Namen sortiert werden. Bei der Sortierung wird die Groß-/Kleinschreibung nicht beachtet. Da das Gleichheitszeichen ein Trennzeichen ist, darf es nicht im Namen einer Umgebungsvariablen verwendet werden.

## <a name="example-1"></a>Beispiel 1

Standardmäßig erbt ein untergeordneter Prozess eine Kopie des Umgebungs Blocks des übergeordneten Prozesses. Im folgenden Beispiel wird veranschaulicht, wie ein neuer Umgebungsblock erstellt wird, der mithilfe von "- [**Prozess Prozess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)" an einen untergeordneten Prozess übergeben wird.

In diesem Beispiel wird der Code in Beispiel 3 als untergeordneter Prozess verwendet, Ex3.exe.


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>
#include <strsafe.h>

#define BUFSIZE 4096

int _tmain()
{
    TCHAR chNewEnv[BUFSIZE];
    LPTSTR lpszCurrentVariable; 
    DWORD dwFlags=0;
    TCHAR szAppName[]=TEXT("ex3.exe");
    STARTUPINFO si;
    PROCESS_INFORMATION pi;
    BOOL fSuccess; 
 
    // Copy environment strings into an environment block. 
 
    lpszCurrentVariable = (LPTSTR) chNewEnv;
    if (FAILED(StringCchCopy(lpszCurrentVariable, BUFSIZE, TEXT("MySetting=A"))))
    {
        printf("String copy failed\n"); 
        return FALSE;
    }

    lpszCurrentVariable += lstrlen(lpszCurrentVariable) + 1; 
    if (FAILED(StringCchCopy(lpszCurrentVariable, BUFSIZE, TEXT("MyVersion=2")))) 
    {
        printf("String copy failed\n"); 
        return FALSE;
    }
 
    // Terminate the block with a NULL byte. 
 
    lpszCurrentVariable += lstrlen(lpszCurrentVariable) + 1; 
    *lpszCurrentVariable = (TCHAR)0; 

    // Create the child process, specifying a new environment block. 
 
    SecureZeroMemory(&si, sizeof(STARTUPINFO));
    si.cb = sizeof(STARTUPINFO);

#ifdef UNICODE
    dwFlags = CREATE_UNICODE_ENVIRONMENT;
#endif

    fSuccess = CreateProcess(szAppName, NULL, NULL, NULL, TRUE, dwFlags,
        (LPVOID) chNewEnv,   // new environment block
        NULL, &si, &pi); 
 
    if (! fSuccess) 
    {
        printf("CreateProcess failed (%d)\n", GetLastError());
        return FALSE;
    }
    WaitForSingleObject(pi.hProcess, INFINITE);
    return TRUE;
}
```



## <a name="example-2"></a>Beispiel 2

Das Ändern der Umgebungsvariablen eines untergeordneten Prozesses während der Prozesserstellung ist die einzige Möglichkeit, dass ein Prozess die Umgebungsvariablen eines anderen Prozesses direkt ändern kann. Ein Prozess kann die Umgebungsvariablen eines anderen Prozesses, der kein untergeordnetes Element dieses Prozesses ist, niemals direkt ändern.

Wenn der untergeordnete Prozess den größten Teil der Umgebung des übergeordneten Prozesses nur mit einigen wenigen Änderungen erben soll, rufen Sie die aktuellen Werte mithilfe von [**GetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-getenvironmentvariable)ab, speichern Sie diese Werte, erstellen Sie einen aktualisierten Block für den untergeordneten Prozess zum Erben, erstellen Sie den untergeordneten Prozess, und stellen Sie die gespeicherten Werte mithilfe von " [**ctenvironmentvariable**](/windows/desktop/api/WinBase/nf-winbase-setenvironmentvariable)" wieder her

In diesem Beispiel wird der Code in Beispiel 3 als untergeordneter Prozess verwendet, Ex3.exe.


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

#define BUFSIZE 4096
#define VARNAME TEXT("MyVariable")

int _tmain()
{
    DWORD dwRet, dwErr;
    LPTSTR pszOldVal; 
    TCHAR szAppName[]=TEXT("ex3.exe");
    DWORD dwFlags=0;
    STARTUPINFO si;
    PROCESS_INFORMATION pi;
    BOOL fExist, fSuccess; 
 
    // Retrieves the current value of the variable if it exists.
    // Sets the variable to a new value, creates a child process,
    // then uses SetEnvironmentVariable to restore the original
    // value or delete it if it did not exist previously. 
 
    pszOldVal = (LPTSTR) malloc(BUFSIZE*sizeof(TCHAR));
    if(NULL == pszOldVal)
    {
        printf("Out of memory\n");
        return FALSE;
    }

    dwRet = GetEnvironmentVariable(VARNAME, pszOldVal, BUFSIZE);

    if(0 == dwRet)
    {
        dwErr = GetLastError();
        if( ERROR_ENVVAR_NOT_FOUND == dwErr )
        {
            printf("Environment variable does not exist.\n");
            fExist=FALSE;
        }
    }
    else if(BUFSIZE < dwRet)
    {
        pszOldVal = (LPTSTR) realloc(pszOldVal, dwRet*sizeof(TCHAR));   
        if(NULL == pszOldVal)
        {
            printf("Out of memory\n");
            return FALSE;
        }
        dwRet = GetEnvironmentVariable(VARNAME, pszOldVal, dwRet);
        if(!dwRet)
        {
            printf("GetEnvironmentVariable failed (%d)\n", GetLastError());
            return FALSE;
        }
        else fExist=TRUE;
    }
    else fExist=TRUE;

    // Set a value for the child process to inherit. 
 
    if (! SetEnvironmentVariable(VARNAME, TEXT("Test"))) 
    {
        printf("SetEnvironmentVariable failed (%d)\n", GetLastError()); 
        return FALSE;
    }
 
    // Create a child process. 

    SecureZeroMemory(&si, sizeof(STARTUPINFO));
    si.cb = sizeof(STARTUPINFO);
 
#ifdef UNICODE
    dwFlags = CREATE_UNICODE_ENVIRONMENT;
#endif

    fSuccess = CreateProcess(szAppName, NULL, NULL, NULL, TRUE, dwFlags, 
        NULL,     // inherit parent's environment 
        NULL, &si, &pi); 
    if (! fSuccess) 
    {
        printf("CreateProcess failed (%d)\n", GetLastError()); 
    }
    WaitForSingleObject(pi.hProcess, INFINITE);

    // Restore the original environment variable. 
 
    if(fExist)
    {
        if (! SetEnvironmentVariable(VARNAME, pszOldVal)) 
        {
            printf("SetEnvironmentVariable failed (%d)\n", GetLastError()); 
            return FALSE;
        }
    }
    else SetEnvironmentVariable(VARNAME, NULL);

    free(pszOldVal);
    
    return fSuccess;
}
```



## <a name="example-3"></a>Beispiel 3

Im folgenden Beispiel wird der Umgebungsblock des Prozesses mithilfe von [**getenvironmentstrings**](/windows/win32/api/processenv/nf-processenv-getenvironmentstrings) abgerufen und der Inhalt auf der Konsole ausgegeben.


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

int _tmain()
{
    LPTSTR lpszVariable; 
    LPTCH lpvEnv; 
 
    // Get a pointer to the environment block. 
 
    lpvEnv = GetEnvironmentStrings();

    // If the returned pointer is NULL, exit.
    if (lpvEnv == NULL)
    {
        printf("GetEnvironmentStrings failed (%d)\n", GetLastError()); 
        return 0;
    }
 
    // Variable strings are separated by NULL byte, and the block is 
    // terminated by a NULL byte. 

    lpszVariable = (LPTSTR) lpvEnv;

    while (*lpszVariable)
    {
        _tprintf(TEXT("%s\n"), lpszVariable);
        lpszVariable += lstrlen(lpszVariable) + 1;
    }
    FreeEnvironmentStrings(lpvEnv);
    return 1;
}
```



 

 
