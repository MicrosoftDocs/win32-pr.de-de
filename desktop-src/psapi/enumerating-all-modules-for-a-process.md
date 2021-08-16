---
title: Aufzählen aller Module für einen Prozess
description: Um zu bestimmen, welche Prozesse eine bestimmte DLL geladen haben, müssen Sie die Module für jeden Prozess aufzählen. Im folgenden Beispielcode wird die EnumProcessModules-Funktion verwendet, um die Module der aktuellen Prozesse im System aufzuzählen.
ms.assetid: 2e411eba-ba60-4678-bf6f-bc15b6e8b478
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17012019c21f550940ea8c11c07153b0c3495471b4d62bf2f8af469ef6b7b90b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032988"
---
# <a name="enumerating-all-modules-for-a-process"></a>Aufzählen aller Module für einen Prozess

Um zu bestimmen, welche Prozesse eine bestimmte DLL geladen haben, müssen Sie die Module für jeden Prozess aufzählen. Im folgenden Beispielcode wird die [**EnumProcessModules-Funktion**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) verwendet, um die Module der aktuellen Prozesse im System aufzuzählen.


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



Die main-Funktion erhält mithilfe der [**EnumProcesses-Funktion**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) eine Liste von Prozessen. Für jeden Prozess ruft die Main-Funktion die PrintModules-Funktion auf und über gibt ihr den Prozessbezeichner. PrintModules ruft wiederum die [**OpenProcess-Funktion**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) auf, um das Prozesshand handle zu erhalten. Wenn **OpenProcess fehlschlägt,** zeigt die Ausgabe nur den Prozessbezeichner an. Beispielsweise schlägt **OpenProcess für die Leerlauf-** und CSRSS-Prozesse fehl, da ihre Zugriffseinschränkungen verhindern, dass Code auf Benutzerebene sie öffnet. Als Nächstes ruft PrintModules die [**EnumProcessModules-Funktion**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) auf, um die Modulhandles-Funktion zu erhalten. Schließlich ruft PrintModules die [**GetModuleFileNameEx-Funktion**](/windows/desktop/api/Psapi/nf-psapi-getmodulefilenameexa) einmal für jedes Modul auf, um die Modulnamen zu erhalten.

 

 