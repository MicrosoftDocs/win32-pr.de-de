---
title: Sammeln von Informationen zur Speicherauslastung für einen Prozess
description: Um die Effizienz der Anwendung zu ermitteln, können Sie die Speicherauslastung untersuchen. Im folgenden Beispielcode wird die getprocessmemoryinfo-Funktion verwendet, um Informationen über die Speicherauslastung eines Prozesses zu erhalten.
ms.assetid: 23641bf8-3653-4cb9-8008-cd99137ca268
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ead17b8308424be8b959c4043eec606b18292708
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390491"
---
# <a name="collecting-memory-usage-information-for-a-process"></a>Sammeln von Informationen zur Speicherauslastung für einen Prozess

Um die Effizienz der Anwendung zu ermitteln, können Sie die Speicherauslastung untersuchen. Im folgenden Beispielcode wird die [**getprocessmemoryinfo**](/windows/desktop/api/Psapi/nf-psapi-getprocessmemoryinfo) -Funktion verwendet, um Informationen über die Speicherauslastung eines Prozesses zu erhalten.


```C++
#include <windows.h>
#include <stdio.h>
#include <psapi.h>

// To ensure correct resolution of symbols, add Psapi.lib to TARGETLIBS
// and compile with -DPSAPI_VERSION=1

void PrintMemoryInfo( DWORD processID )
{
    HANDLE hProcess;
    PROCESS_MEMORY_COUNTERS pmc;

    // Print the process identifier.

    printf( "\nProcess ID: %u\n", processID );

    // Print information about the memory usage of the process.

    hProcess = OpenProcess(  PROCESS_QUERY_INFORMATION |
                                    PROCESS_VM_READ,
                                    FALSE, processID );
    if (NULL == hProcess)
        return;

    if ( GetProcessMemoryInfo( hProcess, &pmc, sizeof(pmc)) )
    {
        printf( "\tPageFaultCount: 0x%08X\n", pmc.PageFaultCount );
        printf( "\tPeakWorkingSetSize: 0x%08X\n", 
                  pmc.PeakWorkingSetSize );
        printf( "\tWorkingSetSize: 0x%08X\n", pmc.WorkingSetSize );
        printf( "\tQuotaPeakPagedPoolUsage: 0x%08X\n", 
                  pmc.QuotaPeakPagedPoolUsage );
        printf( "\tQuotaPagedPoolUsage: 0x%08X\n", 
                  pmc.QuotaPagedPoolUsage );
        printf( "\tQuotaPeakNonPagedPoolUsage: 0x%08X\n", 
                  pmc.QuotaPeakNonPagedPoolUsage );
        printf( "\tQuotaNonPagedPoolUsage: 0x%08X\n", 
                  pmc.QuotaNonPagedPoolUsage );
        printf( "\tPagefileUsage: 0x%08X\n", pmc.PagefileUsage ); 
        printf( "\tPeakPagefileUsage: 0x%08X\n", 
                  pmc.PeakPagefileUsage );
    }

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

    // Print the memory usage for each process

    for ( i = 0; i < cProcesses; i++ )
    {
        PrintMemoryInfo( aProcesses[i] );
    }

    return 0;
}
```



Die Main-Funktion Ruft mithilfe der [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) -Funktion eine Liste der Prozesse ab. Main Ruft für jeden Prozess die printmemoryinfo-Funktion auf und übergibt dabei den Prozess Bezeichner. Printmemoryinfo ruft wiederum die [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) -Funktion auf, um das Prozess Handle abzurufen. Wenn **OpenProcess** fehlschlägt, zeigt die Ausgabe nur die Prozess-ID an. Beispielsweise schlägt **OpenProcess** für die Prozesse im Leerlauf und für CSRSS fehl, da ihre Zugriffsbeschränkungen verhindern, dass Code auf Benutzerebene geöffnet wird. Zum Schluss ruft printmemoryinfo die [**getprocessmemoryinfo**](/windows/desktop/api/Psapi/nf-psapi-getprocessmemoryinfo) -Funktion auf, um die Informationen zur Speicherauslastung zu erhalten.

 

 