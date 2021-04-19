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
# <a name="changing-environment-variables"></a><span data-ttu-id="3dac7-103">Ändern von Umgebungsvariablen</span><span class="sxs-lookup"><span data-stu-id="3dac7-103">Changing Environment Variables</span></span>

<span data-ttu-id="3dac7-104">Jedem Prozess ist ein Umgebungsblock zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="3dac7-104">Each process has an environment block associated with it.</span></span> <span data-ttu-id="3dac7-105">Der Umgebungsblock besteht aus einem null-terminierten Block von null-terminierten Zeichen folgen (d. h., es gibt zwei NULL-Bytes am Ende des Blocks), wobei jede Zeichenfolge in folgendem Format vorliegt:</span><span class="sxs-lookup"><span data-stu-id="3dac7-105">The environment block consists of a null-terminated block of null-terminated strings (meaning there are two null bytes at the end of the block), where each string is in the form:</span></span>

<span data-ttu-id="3dac7-106">*Name* = *Wert*</span><span class="sxs-lookup"><span data-stu-id="3dac7-106">*name*=*value*</span></span>

<span data-ttu-id="3dac7-107">Alle Zeichen folgen im Umgebungsblock müssen alphabetisch nach Namen sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="3dac7-107">All strings in the environment block must be sorted alphabetically by name.</span></span> <span data-ttu-id="3dac7-108">Bei der Sortierung wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="3dac7-108">The sort is case-insensitive, Unicode order, without regard to locale.</span></span> <span data-ttu-id="3dac7-109">Da das Gleichheitszeichen ein Trennzeichen ist, darf es nicht im Namen einer Umgebungsvariablen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3dac7-109">Because the equal sign is a separator, it must not be used in the name of an environment variable.</span></span>

## <a name="example-1"></a><span data-ttu-id="3dac7-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3dac7-110">Example 1</span></span>

<span data-ttu-id="3dac7-111">Standardmäßig erbt ein untergeordneter Prozess eine Kopie des Umgebungs Blocks des übergeordneten Prozesses.</span><span class="sxs-lookup"><span data-stu-id="3dac7-111">By default, a child process inherits a copy of the environment block of the parent process.</span></span> <span data-ttu-id="3dac7-112">Im folgenden Beispiel wird veranschaulicht, wie ein neuer Umgebungsblock erstellt wird, der mithilfe von "- [**Prozess Prozess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)" an einen untergeordneten Prozess übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="3dac7-112">The following example demonstrates how to create a new environment block to pass to a child process using [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span></span>

<span data-ttu-id="3dac7-113">In diesem Beispiel wird der Code in Beispiel 3 als untergeordneter Prozess verwendet, Ex3.exe.</span><span class="sxs-lookup"><span data-stu-id="3dac7-113">This example uses the code in example three as the child process, Ex3.exe.</span></span>


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



## <a name="example-2"></a><span data-ttu-id="3dac7-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="3dac7-114">Example 2</span></span>

<span data-ttu-id="3dac7-115">Das Ändern der Umgebungsvariablen eines untergeordneten Prozesses während der Prozesserstellung ist die einzige Möglichkeit, dass ein Prozess die Umgebungsvariablen eines anderen Prozesses direkt ändern kann.</span><span class="sxs-lookup"><span data-stu-id="3dac7-115">Altering the environment variables of a child process during process creation is the only way one process can directly change the environment variables of another process.</span></span> <span data-ttu-id="3dac7-116">Ein Prozess kann die Umgebungsvariablen eines anderen Prozesses, der kein untergeordnetes Element dieses Prozesses ist, niemals direkt ändern.</span><span class="sxs-lookup"><span data-stu-id="3dac7-116">A process can never directly change the environment variables of another process that is not a child of that process.</span></span>

<span data-ttu-id="3dac7-117">Wenn der untergeordnete Prozess den größten Teil der Umgebung des übergeordneten Prozesses nur mit einigen wenigen Änderungen erben soll, rufen Sie die aktuellen Werte mithilfe von [**GetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-getenvironmentvariable)ab, speichern Sie diese Werte, erstellen Sie einen aktualisierten Block für den untergeordneten Prozess zum Erben, erstellen Sie den untergeordneten Prozess, und stellen Sie die gespeicherten Werte mithilfe von " [**ctenvironmentvariable**](/windows/desktop/api/WinBase/nf-winbase-setenvironmentvariable)" wieder her</span><span class="sxs-lookup"><span data-stu-id="3dac7-117">If you want the child process to inherit most of the parent's environment with only a few changes, retrieve the current values using [**GetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-getenvironmentvariable), save these values, create an updated block for the child process to inherit, create the child process, and then restore the saved values using [**SetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-setenvironmentvariable), as shown in the following example.</span></span>

<span data-ttu-id="3dac7-118">In diesem Beispiel wird der Code in Beispiel 3 als untergeordneter Prozess verwendet, Ex3.exe.</span><span class="sxs-lookup"><span data-stu-id="3dac7-118">This example uses the code in example three as the child process, Ex3.exe.</span></span>


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



## <a name="example-3"></a><span data-ttu-id="3dac7-119">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="3dac7-119">Example 3</span></span>

<span data-ttu-id="3dac7-120">Im folgenden Beispiel wird der Umgebungsblock des Prozesses mithilfe von [**getenvironmentstrings**](/windows/win32/api/processenv/nf-processenv-getenvironmentstrings) abgerufen und der Inhalt auf der Konsole ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="3dac7-120">The following example retrieves the process's environment block using [**GetEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-getenvironmentstrings) and prints the contents to the console.</span></span>


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



 

 
