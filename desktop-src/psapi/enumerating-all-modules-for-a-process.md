---
title: Auflisten aller Module für einen Prozess
description: Um zu ermitteln, welche Prozesse eine bestimmte dll geladen haben, müssen Sie die Module für jeden Prozess auflisten. Der folgende Beispielcode verwendet die enumprocessmodules-Funktion, um die Module der aktuellen Prozesse im System aufzulisten.
ms.assetid: 2e411eba-ba60-4678-bf6f-bc15b6e8b478
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bf09d02d4ae9dc7e55177653e05e3d19df4ab7b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315153"
---
# <a name="enumerating-all-modules-for-a-process"></a>Auflisten aller Module für einen Prozess

Um zu ermitteln, welche Prozesse eine bestimmte dll geladen haben, müssen Sie die Module für jeden Prozess auflisten. Der folgende Beispielcode verwendet die [**enumprocessmodules**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) -Funktion, um die Module der aktuellen Prozesse im System aufzulisten.


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>
#include <psapi.h>

// To ensure correct resolution of symbols, add Psapi.lib to TARGETLIBS
// and compile with -DPSAPI_VERSION=1

int PrintModules( DWORD processID )
{
    HMODULE hMods[1024];
    HANDLE hProcess;
    DWORD cbNeeded;
    unsigned int i;

    // Print the process identifier.

    printf( "\nProcess ID: %u\n", processID );

    // Get a handle to the process.

    hProcess = OpenProcess( PROCESS_QUERY_INFORMATION |
                            PROCESS_VM_READ,
                            FALSE, processID );
    if (NULL == hProcess)
        return 1;

   // Get a list of all the modules in this process.

    if( EnumProcessModules(hProcess, hMods, sizeof(hMods), &cbNeeded))
    {
        for ( i = 0; i < (cbNeeded / sizeof(HMODULE)); i++ )
        {
            TCHAR szModName[MAX_PATH];

            // Get the full path to the module's file.

            if ( GetModuleFileNameEx( hProcess, hMods[i], szModName,
                                      sizeof(szModName) / sizeof(TCHAR)))
            {
                // Print the module name and handle value.

                _tprintf( TEXT("\t%s (0x%08X)\n"), szModName, hMods[i] );
            }
        }
    }
    
    // Release the handle to the process.

    CloseHandle( hProcess );

    return 0;
}

int main( void )
{

    DWORD aProcesses[1024]; 
    DWORD cbNeeded; 
    DWORD cProcesses;
    unsigned int i;

    // Get the list of process identifiers.

    if ( !EnumProcesses( aProcesses, sizeof(aProcesses), &cbNeeded ) )
        return 1;

    // Calculate how many process identifiers were returned.

    cProcesses = cbNeeded / sizeof(DWORD);

    // Print the names of the modules for each process.

    for ( i = 0; i < cProcesses; i++ )
    {
        PrintModules( aProcesses[i] );
    }

    return 0;
}
```



Die Main-Funktion Ruft mithilfe der [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) -Funktion eine Liste der Prozesse ab. Die Main-Funktion Ruft für jeden Prozess die printmodules-Funktion auf und übergibt ihr den Prozess Bezeichner. Print modules wiederum ruft die [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) -Funktion auf, um das Prozess Handle abzurufen. Wenn **OpenProcess** fehlschlägt, zeigt die Ausgabe nur die Prozess-ID an. Beispielsweise schlägt **OpenProcess** für die Prozesse im Leerlauf und für CSRSS fehl, da ihre Zugriffsbeschränkungen verhindern, dass Code auf Benutzerebene geöffnet wird. Als Nächstes ruft printmodules die [**enumprocessmodules**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) -Funktion auf, um die Modul Handles-Funktion abzurufen. Zum Schluss ruft printmodules die [**getmoduledatameex**](/windows/desktop/api/Psapi/nf-psapi-getmodulefilenameexa) -Funktion einmal für jedes Modul auf, um die Modulnamen abzurufen.

 

 