---
description: Das folgende Beispiel veranschaulicht die Verwendung der Funktionen VirtualAlloc und VirtualFree beim Reservieren und Committen von Arbeitsspeicher nach Bedarf für ein dynamisches Array.
ms.assetid: f46bd57d-7684-4a08-8ac7-de204aecb207
title: Reservieren und Committen von Arbeitsspeicher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 615f3c4321dc432b5ef83a841cea12215563e7d103443512a4d3b2c553849540
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118386278"
---
# <a name="reserving-and-committing-memory"></a>Reservieren und Committen von Arbeitsspeicher

Das folgende Beispiel veranschaulicht die Verwendung der [**Funktionen VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) und [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) beim Reservieren und Committen von Arbeitsspeicher nach Bedarf für ein dynamisches Array. Zunächst wird **VirtualAlloc** aufgerufen, um einen Block von Seiten mit **NULL** als Basisadressenparameter zu reservieren, sodass das System gezwungen wird, den Speicherort des Blocks zu bestimmen. Später wird **VirtualAlloc** immer dann aufgerufen, wenn ein Commit für eine Seite aus dieser reservierten Region erforderlich ist und die Basisadresse der nächsten Seite angegeben wird, für die ein Commit ausgeführt werden soll.

Im Beispiel wird eine strukturierte Ausnahmebehandlungssyntax verwendet, um Seiten aus der reservierten Region zu commiten. Wenn während der Ausführung des **\_ \_ try-Blocks** eine Seitenfehlerausnahme auftritt, wird die Filterfunktion im Ausdruck vor dem **\_ \_ except-Block** ausgeführt. Wenn die Filterfunktion eine andere Seite zuordnen kann, wird die Ausführung im **\_ \_ try-Block** an dem Punkt fortgesetzt, an dem die Ausnahme aufgetreten ist. Andernfalls wird der Ausnahmehandler im **\_ \_ except-Block** ausgeführt. Weitere Informationen finden Sie unter [Strukturierte Ausnahmebehandlung.](../debug/structured-exception-handling.md)

Als Alternative zur dynamischen Zuordnung kann der Prozess einfach ein Commit für die gesamte Region erstellen, anstatt sie nur zu reservieren. Beide Methoden führen zur gleichen physischen Speicherauslastung, da seiten, für die ein Committed durchgeführt wurde, erst dann physischen Speicher nutzen, wenn auf sie zugegriffen wird. Der Vorteil der dynamischen Zuordnung besteht in der Minimierung der Gesamtzahl der Seiten, für die ein Committed auf dem System besteht. Bei sehr großen Zuordnungen kann das Vorab committen einer gesamten Zuordnung dazu führen, dass dem System keine commitbaren Seiten mehr zur Verfügung sind, was zu Fehlern bei der virtuellen Speicherbelegung führt.

Die [**ExitProcess-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) im **\_ \_ except-Block** gibt automatisch virtuelle Speicherzuordnungen frei, sodass es nicht erforderlich ist, die Seiten explizit frei zu geben, wenn das Programm über diesen Ausführungspfad beendet wird. Die [**VirtualFree-Funktion**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) gibt die reservierten seiten und die Seiten, für die ein Committed ausgeführt wurde, frei, wenn das Programm mit deaktivierter Ausnahmebehandlung erstellt wurde. Diese Funktion verwendet **MEM \_ RELEASE,** um denCommit für die gesamte Region reservierter und mit einem Committed gebundener Seiten zu dekomprimiert und frei zu geben.

Im folgenden C++-Beispiel wird die dynamische Speicherbelegung mithilfe eines strukturierten Ausnahmehandlers veranschaulicht.


```C++
// A short program to demonstrate dynamic memory allocation
// using a structured exception handler.

#include <windows.h>
#include <tchar.h>
#include <stdio.h>
#include <stdlib.h>             // For exit

#define PAGELIMIT 80            // Number of pages to ask for

LPTSTR lpNxtPage;               // Address of the next page to ask for
DWORD dwPages = 0;              // Count of pages gotten so far
DWORD dwPageSize;               // Page size on this computer

INT PageFaultExceptionFilter(DWORD dwCode)
{
    LPVOID lpvResult;

    // If the exception is not a page fault, exit.

    if (dwCode != EXCEPTION_ACCESS_VIOLATION)
    {
        _tprintf(TEXT("Exception code = %d.\n"), dwCode);
        return EXCEPTION_EXECUTE_HANDLER;
    }

    _tprintf(TEXT("Exception is a page fault.\n"));

    // If the reserved pages are used up, exit.

    if (dwPages >= PAGELIMIT)
    {
        _tprintf(TEXT("Exception: out of pages.\n"));
        return EXCEPTION_EXECUTE_HANDLER;
    }

    // Otherwise, commit another page.

    lpvResult = VirtualAlloc(
                     (LPVOID) lpNxtPage, // Next page to commit
                     dwPageSize,         // Page size, in bytes
                     MEM_COMMIT,         // Allocate a committed page
                     PAGE_READWRITE);    // Read/write access
    if (lpvResult == NULL )
    {
        _tprintf(TEXT("VirtualAlloc failed.\n"));
        return EXCEPTION_EXECUTE_HANDLER;
    }
    else
    {
        _tprintf(TEXT("Allocating another page.\n"));
    }

    // Increment the page count, and advance lpNxtPage to the next page.

    dwPages++;
    lpNxtPage = (LPTSTR) ((PCHAR) lpNxtPage + dwPageSize);

    // Continue execution where the page fault occurred.

    return EXCEPTION_CONTINUE_EXECUTION;
}

VOID ErrorExit(LPTSTR lpMsg)
{
    _tprintf(TEXT("Error! %s with error code of %ld.\n"),
             lpMsg, GetLastError ());
    exit (0);
}

VOID _tmain(VOID)
{
    LPVOID lpvBase;               // Base address of the test memory
    LPTSTR lpPtr;                 // Generic character pointer
    BOOL bSuccess;                // Flag
    DWORD i;                      // Generic counter
    SYSTEM_INFO sSysInfo;         // Useful information about the system

    GetSystemInfo(&sSysInfo);     // Initialize the structure.

    _tprintf (TEXT("This computer has page size %d.\n"), sSysInfo.dwPageSize);

    dwPageSize = sSysInfo.dwPageSize;

    // Reserve pages in the virtual address space of the process.

    lpvBase = VirtualAlloc(
                     NULL,                 // System selects address
                     PAGELIMIT*dwPageSize, // Size of allocation
                     MEM_RESERVE,          // Allocate reserved pages
                     PAGE_NOACCESS);       // Protection = no access
    if (lpvBase == NULL )
        ErrorExit(TEXT("VirtualAlloc reserve failed."));

    lpPtr = lpNxtPage = (LPTSTR) lpvBase;

    // Use structured exception handling when accessing the pages.
    // If a page fault occurs, the exception filter is executed to
    // commit another page from the reserved block of pages.

    for (i=0; i < PAGELIMIT*dwPageSize; i++)
    {
        __try
        {
            // Write to memory.

            lpPtr[i] = 'a';
        }

        // If there's a page fault, commit another page and try again.

        __except ( PageFaultExceptionFilter( GetExceptionCode() ) )
        {

            // This code is executed only if the filter function
            // is unsuccessful in committing the next page.

            _tprintf (TEXT("Exiting process.\n"));

            ExitProcess( GetLastError() );

        }

    }

    // Release the block of pages when you are finished using them.

    bSuccess = VirtualFree(
                       lpvBase,       // Base address of block
                       0,             // Bytes of committed pages
                       MEM_RELEASE);  // Decommit the pages

    _tprintf (TEXT("Release %s.\n"), bSuccess ? TEXT("succeeded") : TEXT("failed") );

}
```



 

 
