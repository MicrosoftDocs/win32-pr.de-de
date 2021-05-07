---
title: Aufzählen aller Prozesse
description: Im folgenden Beispielcode wird die EnumProcesses-Funktion verwendet, um die aktuellen Prozesse im System zu aufzählen.
ms.assetid: 0ed81548-4936-40e9-bfc8-baa71492310e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf03fd9ad06bfb15924f3f5ec92d8f8858fbff60
ms.sourcegitcommit: 07ba02719c9779e082b108ae74f9699fb0236c34
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/06/2021
ms.locfileid: "108644112"
---
# <a name="enumerating-all-processes"></a><span data-ttu-id="9b1d4-103">Aufzählen aller Prozesse</span><span class="sxs-lookup"><span data-stu-id="9b1d4-103">Enumerating All Processes</span></span>

<span data-ttu-id="9b1d4-104">Im folgenden Beispielcode wird die [**EnumProcesses-Funktion**](/windows/win32/api/Psapi/nf-psapi-enumprocesses) verwendet, um den Prozessbezeichner für jedes Prozessobjekt im System abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9b1d4-104">The following sample code uses the [**EnumProcesses**](/windows/win32/api/Psapi/nf-psapi-enumprocesses) function to retrieve the process identifier for each process object in the system.</span></span> <span data-ttu-id="9b1d4-105">[EnumProcessModules wird](/windows/win32/api/psapi/nf-psapi-enumprocessmodules) dann aufgerufen, um jeden Prozessnamen zu erhalten und ausgedruckt.</span><span class="sxs-lookup"><span data-stu-id="9b1d4-105">[EnumProcessModules](/windows/win32/api/psapi/nf-psapi-enumprocessmodules) is then called to get each process name and print it.</span></span>

>[!NOTE]
> <span data-ttu-id="9b1d4-106">Verwenden Sie für 64-Bit-Prozesse die [EnumProcessModulesEx-Funktion.](/windows/win32/api/psapi/nf-psapi-enumprocessmodulesex)</span><span class="sxs-lookup"><span data-stu-id="9b1d4-106">For 64 bit processes, use the [EnumProcessModulesEx](/windows/win32/api/psapi/nf-psapi-enumprocessmodulesex) function.</span></span>

```C++
#include <windows.h>
#include <stdio.h>
#include <tchar.h>
#include <psapi.h>

// To ensure correct resolution of symbols, add Psapi.lib to TARGETLIBS
// and compile with -DPSAPI_VERSION=1

void PrintProcessNameAndID( DWORD processID )
{
    TCHAR szProcessName[MAX_PATH] = TEXT("<unknown>");

    // Get a handle to the process.

    HANDLE hProcess = OpenProcess( PROCESS_QUERY_INFORMATION |
                                   PROCESS_VM_READ,
                                   FALSE, processID );

    // Get the process name.

    if (NULL != hProcess )
    {
        HMODULE hMod;
        DWORD cbNeeded;

        if ( EnumProcessModules( hProcess, &hMod, sizeof(hMod), 
             &cbNeeded) )
        {
            GetModuleBaseName( hProcess, hMod, szProcessName, 
                               sizeof(szProcessName)/sizeof(TCHAR) );
        }
    }

    // Print the process name and identifier.

    _tprintf( TEXT("%s  (PID: %u)\n"), szProcessName, processID );

    // Release the handle to the process.

    CloseHandle( hProcess );
}

int main( void )
{
    // Get the list of process identifiers.

    DWORD aProcesses[1024], cbNeeded, cProcesses;
    unsigned int i;

    if ( !EnumProcesses( aProcesses, sizeof(aProcesses), &cbNeeded ) )
    {
        return 1;
    }


    // Calculate how many process identifiers were returned.

    cProcesses = cbNeeded / sizeof(DWORD);

    // Print the name and process identifier for each process.

    for ( i = 0; i < cProcesses; i++ )
    {
        if( aProcesses[i] != 0 )
        {
            PrintProcessNameAndID( aProcesses[i] );
        }
    }

    return 0;
}
```



<span data-ttu-id="9b1d4-107">Die main-Funktion erhält mithilfe der [**EnumProcesses-Funktion**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) eine Liste von Prozessen.</span><span class="sxs-lookup"><span data-stu-id="9b1d4-107">The main function obtains a list of processes by using the [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) function.</span></span> <span data-ttu-id="9b1d4-108">Für jeden Prozess ruft main die **PrintProcessNameAndID-Funktion** auf und über gibt den Prozessbezeichner an sie weiter.</span><span class="sxs-lookup"><span data-stu-id="9b1d4-108">For each process, main calls the **PrintProcessNameAndID** function, passing it the process identifier.</span></span> <span data-ttu-id="9b1d4-109">**PrintProcessNameAndID** ruft wiederum die [**OpenProcess-Funktion**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) auf, um das Prozesshandle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9b1d4-109">**PrintProcessNameAndID** in turn calls the [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) function to obtain the process handle.</span></span> <span data-ttu-id="9b1d4-110">Wenn **OpenProcess fehlschlägt,** zeigt die Ausgabe den Prozessnamen als <unknown> an.</span><span class="sxs-lookup"><span data-stu-id="9b1d4-110">If **OpenProcess** fails, the output shows the process name as <unknown>.</span></span> <span data-ttu-id="9b1d4-111">Beispielsweise schlägt **OpenProcess für die Leerlauf-** und CSRSS-Prozesse fehl, da ihre Zugriffseinschränkungen verhindern, dass Code auf Benutzerebene sie öffnet.</span><span class="sxs-lookup"><span data-stu-id="9b1d4-111">For example, **OpenProcess** fails for the Idle and CSRSS processes because their access restrictions prevent user-level code from opening them.</span></span> <span data-ttu-id="9b1d4-112">Als Nächstes **ruft PrintProcessNameAndID** die [**EnumProcessModules-Funktion**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) auf, um die Modulhandles zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9b1d4-112">Next, **PrintProcessNameAndID** calls the [**EnumProcessModules**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) function to obtain the module handles.</span></span> <span data-ttu-id="9b1d4-113">Schließlich ruft **PrintProcessNameAndID** die [**GetModuleBaseName-Funktion**](/windows/desktop/api/Psapi/nf-psapi-getmodulebasenamea) auf, um den Namen der ausführbaren Datei zu erhalten, und zeigt den Namen zusammen mit dem Prozessbezeichner an.</span><span class="sxs-lookup"><span data-stu-id="9b1d4-113">Finally, **PrintProcessNameAndID** calls the [**GetModuleBaseName**](/windows/desktop/api/Psapi/nf-psapi-getmodulebasenamea) function to obtain the name of the executable file and displays the name along with the process identifier.</span></span>

 

 
