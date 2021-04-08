---
description: Die Funktion "Funktion erstellen" erstellt einen neuen Prozess, der unabhängig vom Erstellungs Prozess ausgeführt wird. Der Einfachheit halber wird die Beziehung jedoch als über-/Unterordnungsbeziehung bezeichnet.
ms.assetid: 4c3f76a3-e9f5-4d73-b5ef-eabfa9d6e4d4
title: Erstellen von Prozessen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75606a3006bf63359b3e52cf2172b8bc2d77ed56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959730"
---
# <a name="creating-processes"></a>Erstellen von Prozessen

Die [**Funktion "**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) Funktion erstellen" erstellt einen neuen Prozess, der unabhängig vom Erstellungs Prozess ausgeführt wird. Der Einfachheit halber wird die Beziehung jedoch als über-/Unterordnungsbeziehung bezeichnet.

Der folgende Code veranschaulicht, wie ein Prozess erstellt wird.


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



Wenn " [**forateprocess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) " erfolgreich ist, wird eine [**Prozess \_ Informations**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information) Struktur mit Handles und bezeichlern für den neuen Prozess und seinen primären Thread zurückgegeben. Die Thread-und Prozess Handles werden mit vollständigen Zugriffsrechten erstellt, obwohl der Zugriff eingeschränkt werden kann, wenn Sie Sicherheits Deskriptoren angeben. Wenn diese Handles nicht mehr benötigt werden, schließen Sie Sie mithilfe der [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) -Funktion.

Sie können auch einen Prozess erstellen, indem Sie die Funktion " [**kreateprocessasuser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) " oder " [**kreateprocesswithlogonw**](/windows/desktop/api/WinBase/nf-winbase-createprocesswithlogonw) " verwenden. Dies ermöglicht es Ihnen, den Sicherheitskontext des Benutzerkontos anzugeben, in dem der Prozess ausgeführt wird.

 

 
