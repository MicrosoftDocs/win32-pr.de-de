---
title: Auflisten aller Prozesse
description: Der folgende Beispielcode verwendet die EnumProcesses-Funktion, um die aktuellen Prozesse im System aufzuzählen.
ms.assetid: 0ed81548-4936-40e9-bfc8-baa71492310e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e64e127014910974b881a7ae21e807be9ac19452
ms.sourcegitcommit: d581811a577e00821667dad731710909979dc72d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/08/2021
ms.locfileid: "104530416"
---
# <a name="enumerating-all-processes"></a>Auflisten aller Prozesse

Der folgende Beispielcode verwendet die [**EnumProcesses**](/windows/win32/api/Psapi/nf-psapi-enumprocesses) -Funktion, um die Prozess-ID für jedes Prozess Objekt im System abzurufen. Anschließend wird " [enumprocessmodules](/windows/win32/api/psapi/nf-psapi-enumprocessmodules) " aufgerufen, um jeden Prozessnamen zu erhalten und ihn zu drucken.

>[!NOTE]
> Verwenden Sie für 64-Bit-prozepositionen die [enumprocessmodulesex](/windows/win32/api/psapi/nf-psapi-enumprocessmodulesex) -Funktion.

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



Die Main-Funktion Ruft mithilfe der [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) -Funktion eine Liste der Prozesse ab. Main Ruft für jeden Prozess die **printprocessnameandid** -Funktion auf und übergibt ihr den Prozess Bezeichner. **Print processnameandid** ruft wiederum die [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) -Funktion auf, um das Prozess Handle abzurufen. Wenn **OpenProcess** fehlschlägt, wird in der Ausgabe der Prozess Name als angezeigt <unknown> . Beispielsweise schlägt **OpenProcess** für die Prozesse im Leerlauf und für CSRSS fehl, da ihre Zugriffsbeschränkungen verhindern, dass Code auf Benutzerebene geöffnet wird. Als Nächstes ruft **printprocessnameandid** die [**enumprocessmodules**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) -Funktion auf, um die Modul Handles abzurufen. Zum Schluss ruft **printprocessnameandid** die [**getmodulebasename**](/windows/desktop/api/Psapi/nf-psapi-getmodulebasenamea) -Funktion auf, um den Namen der ausführbaren Datei abzurufen, und zeigt den Namen zusammen mit der Prozess-ID an.

 

 
