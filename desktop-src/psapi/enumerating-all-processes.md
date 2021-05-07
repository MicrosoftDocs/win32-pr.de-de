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
# <a name="enumerating-all-processes"></a>Aufzählen aller Prozesse

Im folgenden Beispielcode wird die [**EnumProcesses-Funktion**](/windows/win32/api/Psapi/nf-psapi-enumprocesses) verwendet, um den Prozessbezeichner für jedes Prozessobjekt im System abzurufen. [EnumProcessModules wird](/windows/win32/api/psapi/nf-psapi-enumprocessmodules) dann aufgerufen, um jeden Prozessnamen zu erhalten und ausgedruckt.

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



Die main-Funktion erhält mithilfe der [**EnumProcesses-Funktion**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) eine Liste von Prozessen. Für jeden Prozess ruft main die **PrintProcessNameAndID-Funktion** auf und über gibt den Prozessbezeichner an sie weiter. **PrintProcessNameAndID** ruft wiederum die [**OpenProcess-Funktion**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) auf, um das Prozesshandle zu erhalten. Wenn **OpenProcess fehlschlägt,** zeigt die Ausgabe den Prozessnamen als <unknown> an. Beispielsweise schlägt **OpenProcess für die Leerlauf-** und CSRSS-Prozesse fehl, da ihre Zugriffseinschränkungen verhindern, dass Code auf Benutzerebene sie öffnet. Als Nächstes **ruft PrintProcessNameAndID** die [**EnumProcessModules-Funktion**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) auf, um die Modulhandles zu erhalten. Schließlich ruft **PrintProcessNameAndID** die [**GetModuleBaseName-Funktion**](/windows/desktop/api/Psapi/nf-psapi-getmodulebasenamea) auf, um den Namen der ausführbaren Datei zu erhalten, und zeigt den Namen zusammen mit dem Prozessbezeichner an.

 

 
