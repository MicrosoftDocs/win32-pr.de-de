---
description: Das folgende Beispiel veranschaulicht die Verwendung der Funktionen virtualzuordc und VirtualFree beim reservieren und committen von Arbeitsspeicher nach Bedarf für ein dynamisches Array.
ms.assetid: f46bd57d-7684-4a08-8ac7-de204aecb207
title: Reservieren und Commit des Arbeitsspeichers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66ff5853d01561454265e1ee2102fbf6ebd9bb04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369884"
---
# <a name="reserving-and-committing-memory"></a><span data-ttu-id="9a25a-103">Reservieren und Commit des Arbeitsspeichers</span><span class="sxs-lookup"><span data-stu-id="9a25a-103">Reserving and Committing Memory</span></span>

<span data-ttu-id="9a25a-104">Das folgende Beispiel veranschaulicht die Verwendung der Funktionen [**virtualzuordc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) und [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) beim reservieren und committen von Arbeitsspeicher nach Bedarf für ein dynamisches Array.</span><span class="sxs-lookup"><span data-stu-id="9a25a-104">The following example illustrates the use of the [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) and [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) functions in reserving and committing memory as needed for a dynamic array.</span></span> <span data-ttu-id="9a25a-105">Zunächst wird **virtualzuweisung** aufgerufen, um einen Block von Seiten zu reservieren, wobei **null** als Basis Adress Parameter angegeben wird. Dadurch wird das System gezwungen, den Speicherort des Blocks zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="9a25a-105">First, **VirtualAlloc** is called to reserve a block of pages with **NULL** specified as the base address parameter, forcing the system to determine the location of the block.</span></span> <span data-ttu-id="9a25a-106">Später wird **virtualbelegc** aufgerufen, wenn es erforderlich ist, einen Commit für eine Seite aus dieser reservierten Region durchzusetzen, und die Basisadresse der nächsten Seite, für die ein Commit ausgeführt werden soll, angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9a25a-106">Later, **VirtualAlloc** is called whenever it is necessary to commit a page from this reserved region, and the base address of the next page to be committed is specified.</span></span>

<span data-ttu-id="9a25a-107">Im Beispiel wird eine strukturierte Ausnahme Behandlungs Syntax verwendet, um Seiten aus dem reservierten Bereich zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="9a25a-107">The example uses structured exception-handling syntax to commit pages from the reserved region.</span></span> <span data-ttu-id="9a25a-108">Wenn während der Ausführung des **\_ \_ try** -Blocks eine Seiten Fehler Ausnahme auftritt, wird die Filter-Funktion im Ausdruck ausgeführt, der **\_ \_ mit Ausnahme** Block vorangestellt ist.</span><span class="sxs-lookup"><span data-stu-id="9a25a-108">Whenever a page fault exception occurs during the execution of the **\_\_try** block, the filter function in the expression preceding the **\_\_except** block is executed.</span></span> <span data-ttu-id="9a25a-109">Wenn die Filterfunktion eine andere Seite zuordnen kann, wird die Ausführung im **\_ \_ try** -Block an dem Punkt fortgesetzt, an dem die Ausnahme aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="9a25a-109">If the filter function can allocate another page, execution continues in the **\_\_try** block at the point where the exception occurred.</span></span> <span data-ttu-id="9a25a-110">Andernfalls wird der Ausnahmehandler im **\_ \_ Ausnahme** -Block ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9a25a-110">Otherwise, the exception handler in the **\_\_except** block is executed.</span></span> <span data-ttu-id="9a25a-111">Weitere Informationen finden Sie unter [strukturierte Ausnahmebehandlung](../debug/structured-exception-handling.md).</span><span class="sxs-lookup"><span data-stu-id="9a25a-111">For more information, see [Structured Exception Handling](../debug/structured-exception-handling.md).</span></span>

<span data-ttu-id="9a25a-112">Als Alternative zur dynamischen Zuordnung kann der Prozess einfach einen Commit für die gesamte Region durchsetzen, anstatt ihn nur zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="9a25a-112">As an alternative to dynamic allocation, the process can simply commit the entire region instead of only reserving it.</span></span> <span data-ttu-id="9a25a-113">Beide Methoden führen zu derselben physischen Speicherauslastung, da commitseiten keinen physischen Speicher beanspruchen, bis auf Sie zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="9a25a-113">Both methods result in the same physical memory usage because committed pages do not consume any physical storage until they are first accessed.</span></span> <span data-ttu-id="9a25a-114">Der Vorteil der dynamischen Zuordnung besteht darin, dass dadurch die Gesamtzahl der zugegebenen Seiten im System minimiert wird.</span><span class="sxs-lookup"><span data-stu-id="9a25a-114">The advantage of dynamic allocation is that it minimizes the total number of committed pages on the system.</span></span> <span data-ttu-id="9a25a-115">Bei sehr großen Zuordnungen kann das System vor dem Commit einer vollständigen Zuordnung dazu führen, dass das System nicht über commitfähige Seiten verfügt. Dies führt zu Fehlern bei der virtuellen Speicher Belegung.</span><span class="sxs-lookup"><span data-stu-id="9a25a-115">For very large allocations, pre-committing an entire allocation can cause the system to run out of committable pages, resulting in virtual memory allocation failures.</span></span>

<span data-ttu-id="9a25a-116">Die [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) -Funktion im **\_ \_ Ausnahme** Block gibt automatisch virtuelle Speicher Belegungen frei, sodass es nicht notwendig ist, die Seiten explizit freizugeben, wenn das Programm den Ausführungs Pfad beendet.</span><span class="sxs-lookup"><span data-stu-id="9a25a-116">The [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) function in the **\_\_except** block automatically releases virtual memory allocations, so it is not necessary to explicitly free the pages when the program terminates through this execution path.</span></span> <span data-ttu-id="9a25a-117">Die [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) -Funktion gibt die reservierten und zugesicherte Seiten frei, wenn das Programm mit deaktivierter Ausnahmebehandlung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="9a25a-117">The [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) function frees the reserved and committed pages if the program is built with exception handling disabled.</span></span> <span data-ttu-id="9a25a-118">Diese Funktion verwendet die Arbeitsspeicher **\_ Freigabe** , um den gesamten Bereich von reservierten und commitenden Seiten zu übernehmen und freizugeben.</span><span class="sxs-lookup"><span data-stu-id="9a25a-118">This function uses **MEM\_RELEASE** to decommit and release the entire region of reserved and committed pages.</span></span>

<span data-ttu-id="9a25a-119">Im folgenden C++-Beispiel wird die dynamische Speicher Belegung mithilfe eines strukturierten Ausnahme Handlers veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="9a25a-119">The following C++ example demonstrates dynamic memory allocation using a structured exception handler.</span></span>


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



 

 
