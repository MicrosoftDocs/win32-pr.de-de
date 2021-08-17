---
description: Die CreateProcess-Funktion erstellt einen neuen Prozess, der unabhängig vom Erstellungsprozess ausgeführt wird. Der Einfachheit halber wird die Beziehung jedoch als über- und untergeordnete Beziehung bezeichnet.
ms.assetid: 4c3f76a3-e9f5-4d73-b5ef-eabfa9d6e4d4
title: Erstellen von Prozessen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be8e5e4340f5c956e964b74ab134a7618a4c4bf0fa44eee1989a0457741d7bc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143103"
---
# <a name="creating-processes"></a>Erstellen von Prozessen

Die [**CreateProcess-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) erstellt einen neuen Prozess, der unabhängig vom Erstellungsprozess ausgeführt wird. Der Einfachheit halber wird die Beziehung jedoch als über- und untergeordnete Beziehung bezeichnet.

Der folgende Code veranschaulicht das Erstellen eines Prozesses.


```C++
#include <windows.h>
#include <stdio.h>
#include <tchar.h>

void _tmain( int argc, TCHAR *argv[] )
{
    STARTUPINFO si;
    PROCESS_INFORMATION pi;

    ZeroMemory( &si, sizeof(si) );
    si.cb = sizeof(si);
    ZeroMemory( &pi, sizeof(pi) );

    if( argc != 2 )
    {
        printf("Usage: %s [cmdline]\n", argv[0]);
        return;
    }

    // Start the child process. 
    if( !CreateProcess( NULL,   // No module name (use command line)
        argv[1],        // Command line
        NULL,           // Process handle not inheritable
        NULL,           // Thread handle not inheritable
        FALSE,          // Set handle inheritance to FALSE
        0,              // No creation flags
        NULL,           // Use parent's environment block
        NULL,           // Use parent's starting directory 
        &si,            // Pointer to STARTUPINFO structure
        &pi )           // Pointer to PROCESS_INFORMATION structure
    ) 
    {
        printf( "CreateProcess failed (%d).\n", GetLastError() );
        return;
    }

    // Wait until child process exits.
    WaitForSingleObject( pi.hProcess, INFINITE );

    // Close process and thread handles. 
    CloseHandle( pi.hProcess );
    CloseHandle( pi.hThread );
}
```



Wenn [**CreateProcess erfolgreich**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) ist, wird eine [**PROCESS \_ INFORMATION-Struktur**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information) zurückgegeben, die Handles und Bezeichner für den neuen Prozess und seinen primären Thread enthält. Der Thread und die Prozesshandles werden mit Vollzugriffsrechten erstellt, obwohl der Zugriff eingeschränkt werden kann, wenn Sie Sicherheitsdeskriptoren angeben. Wenn Sie diese Handles nicht mehr benötigen, schließen Sie sie mithilfe der [**CloseHandle-Funktion.**](/windows/desktop/api/handleapi/nf-handleapi-closehandle)

Sie können einen Prozess auch mithilfe der [**Funktion CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) oder [**CreateProcessWithLogonW**](/windows/desktop/api/WinBase/nf-winbase-createprocesswithlogonw) erstellen. Dadurch können Sie den Sicherheitskontext des Benutzerkontos angeben, in dem der Prozess ausgeführt wird.

 

 
