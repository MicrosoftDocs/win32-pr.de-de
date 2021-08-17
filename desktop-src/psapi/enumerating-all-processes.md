---
title: Aufzählen aller Prozesse
description: Im folgenden Beispielcode wird die EnumProcesses-Funktion verwendet, um die aktuellen Prozesse im System aufzuzählen.
ms.assetid: 0ed81548-4936-40e9-bfc8-baa71492310e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89798ed3d2d7e44f014d95833302edb5d5be078daf557eed32d3496c863539e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117681007"
---
# <a name="enumerating-all-processes"></a>Aufzählen aller Prozesse

Im folgenden Beispielcode wird die [**EnumProcesses-Funktion**](/windows/win32/api/Psapi/nf-psapi-enumprocesses) verwendet, um den Prozessbezeichner für jedes Prozessobjekt im System abzurufen. [EnumProcessModules](/windows/win32/api/psapi/nf-psapi-enumprocessmodules) wird dann aufgerufen, um jeden Prozessnamen abzurufen und zu drucken.

>[!NOTE]
> Verwenden Sie für 64-Bit-Prozesse die [EnumProcessModulesEx-Funktion.](/windows/win32/api/psapi/nf-psapi-enumprocessmodulesex)

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



Die main-Funktion ruft mithilfe der [**EnumProcesses-Funktion**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) eine Liste von Prozessen ab. Für jeden Prozess ruft main die **PrintProcessNameAndID-Funktion** auf und übergibt ihr den Prozessbezeichner. **PrintProcessNameAndID** ruft wiederum die [**OpenProcess-Funktion**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) auf, um das Prozesshandle abzurufen. Wenn **OpenProcess** fehlschlägt, wird der Prozessname in der Ausgabe als <unknown> angezeigt. Beispielsweise schlägt **OpenProcess** für die Prozesse Idle und CSRSS fehl, da deren Zugriffseinschränkungen verhindern, dass sie von Code auf Benutzerebene geöffnet werden. Als Nächstes ruft **PrintProcessNameAndID** die [**EnumProcessModules-Funktion**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) auf, um die Modulhandles abzurufen. Schließlich ruft **PrintProcessNameAndID** die [**GetModuleBaseName-Funktion**](/windows/desktop/api/Psapi/nf-psapi-getmodulebasenamea) auf, um den Namen der ausführbaren Datei abzurufen, und zeigt den Namen zusammen mit dem Prozessbezeichner an.

 

 
