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
# <a name="creating-processes"></a><span data-ttu-id="3f41a-104">Erstellen von Prozessen</span><span class="sxs-lookup"><span data-stu-id="3f41a-104">Creating Processes</span></span>

<span data-ttu-id="3f41a-105">Die [**Funktion "**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) Funktion erstellen" erstellt einen neuen Prozess, der unabhängig vom Erstellungs Prozess ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3f41a-105">The [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) function creates a new process, which runs independently of the creating process.</span></span> <span data-ttu-id="3f41a-106">Der Einfachheit halber wird die Beziehung jedoch als über-/Unterordnungsbeziehung bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="3f41a-106">However, for simplicity, the relationship is referred to as a parent-child relationship.</span></span>

<span data-ttu-id="3f41a-107">Der folgende Code veranschaulicht, wie ein Prozess erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="3f41a-107">The following code demonstrates how to create a process.</span></span>


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



<span data-ttu-id="3f41a-108">Wenn " [**forateprocess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) " erfolgreich ist, wird eine [**Prozess \_ Informations**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information) Struktur mit Handles und bezeichlern für den neuen Prozess und seinen primären Thread zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3f41a-108">If [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) succeeds, it returns a [**PROCESS\_INFORMATION**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information) structure containing handles and identifiers for the new process and its primary thread.</span></span> <span data-ttu-id="3f41a-109">Die Thread-und Prozess Handles werden mit vollständigen Zugriffsrechten erstellt, obwohl der Zugriff eingeschränkt werden kann, wenn Sie Sicherheits Deskriptoren angeben.</span><span class="sxs-lookup"><span data-stu-id="3f41a-109">The thread and process handles are created with full access rights, although access can be restricted if you specify security descriptors.</span></span> <span data-ttu-id="3f41a-110">Wenn diese Handles nicht mehr benötigt werden, schließen Sie Sie mithilfe der [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="3f41a-110">When you no longer need these handles, close them by using the [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function.</span></span>

<span data-ttu-id="3f41a-111">Sie können auch einen Prozess erstellen, indem Sie die Funktion " [**kreateprocessasuser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) " oder " [**kreateprocesswithlogonw**](/windows/desktop/api/WinBase/nf-winbase-createprocesswithlogonw) " verwenden.</span><span class="sxs-lookup"><span data-stu-id="3f41a-111">You can also create a process using the [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) or [**CreateProcessWithLogonW**](/windows/desktop/api/WinBase/nf-winbase-createprocesswithlogonw) function.</span></span> <span data-ttu-id="3f41a-112">Dies ermöglicht es Ihnen, den Sicherheitskontext des Benutzerkontos anzugeben, in dem der Prozess ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3f41a-112">This allows you to specify the security context of the user account in which the process will execute.</span></span>

 

 
