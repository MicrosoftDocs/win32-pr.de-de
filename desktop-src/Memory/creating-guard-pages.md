---
description: Eine Wächter Seite bietet einen One-Shot-Alarm für den Zugriff auf die Speicherseite.
ms.assetid: 763bc763-e178-481e-a81a-c15715e56901
title: Erstellen von Wächter Seiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10768da75090a28ffecd5302d88dbc142ae9c147
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368091"
---
# <a name="creating-guard-pages"></a><span data-ttu-id="ed250-103">Erstellen von Wächter Seiten</span><span class="sxs-lookup"><span data-stu-id="ed250-103">Creating Guard Pages</span></span>

<span data-ttu-id="ed250-104">Eine Wächter Seite bietet einen One-Shot-Alarm für den Zugriff auf die Speicherseite.</span><span class="sxs-lookup"><span data-stu-id="ed250-104">A guard page provides a one-shot alarm for memory page access.</span></span> <span data-ttu-id="ed250-105">Dies kann für Anwendungen nützlich sein, die das Wachstum großer dynamischer Datenstrukturen überwachen müssen.</span><span class="sxs-lookup"><span data-stu-id="ed250-105">This can be useful for an application that needs to monitor the growth of large dynamic data structures.</span></span> <span data-ttu-id="ed250-106">Beispielsweise gibt es Betriebssysteme, die Guard-Seiten zum Implementieren der automatischen Stapel Überprüfung verwenden.</span><span class="sxs-lookup"><span data-stu-id="ed250-106">For example, there are operating systems that use guard pages to implement automatic stack checking.</span></span>

<span data-ttu-id="ed250-107">Zum Erstellen einer Wächter Seite legen Sie den **Page \_ Guard** -Seiten schutzmodifizierer für die Seite fest.</span><span class="sxs-lookup"><span data-stu-id="ed250-107">To create a guard page, set the **PAGE\_GUARD** page protection modifier for the page.</span></span> <span data-ttu-id="ed250-108">Dieser Wert kann zusammen mit anderen Modifizierers für den Seitenschutz in den Funktionen [**virtualzuordc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc), [**virtualindecex**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex), [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect)und [**virtualprotectex**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotectex) angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ed250-108">This value can be specified, along with other page protection modifiers, in the [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc), [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex), [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect), and [**VirtualProtectEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotectex) functions.</span></span> <span data-ttu-id="ed250-109">Der **Page \_ Guard** -Modifizierer kann mit allen anderen Modifizierern für den Seitenschutz verwendet werden, mit Ausnahme von **Page \_ NoAccess**.</span><span class="sxs-lookup"><span data-stu-id="ed250-109">The **PAGE\_GUARD** modifier can be used with any other page protection modifiers, except **PAGE\_NOACCESS**.</span></span>

<span data-ttu-id="ed250-110">Wenn ein Programm versucht, auf eine Adresse innerhalb einer Wächter Seite zuzugreifen, löst das System eine **Status \_ Wächter- \_ Seiten \_ Verletzung** (0x80000001) aus.</span><span class="sxs-lookup"><span data-stu-id="ed250-110">If a program attempts to access an address within a guard page, the system raises a **STATUS\_GUARD\_PAGE\_VIOLATION** (0x80000001) exception.</span></span> <span data-ttu-id="ed250-111">Das System löscht auch den **Page \_ Guard** -Modifizierer, sodass der Status der Schutz Seite der Arbeitsspeicher Seite entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="ed250-111">The system also clears the **PAGE\_GUARD** modifier, removing the memory page's guard page status.</span></span> <span data-ttu-id="ed250-112">Das System hält den nächsten Versuch, auf die Arbeitsspeicher Seite zuzugreifen, nicht an, mit einer Ausnahme der **\_ statuswächter- \_ Seiten \_ Verletzung** .</span><span class="sxs-lookup"><span data-stu-id="ed250-112">The system will not stop the next attempt to access the memory page with a **STATUS\_GUARD\_PAGE\_VIOLATION** exception.</span></span>

<span data-ttu-id="ed250-113">Wenn bei einem Systemdienst eine Schutz Seiten Ausnahme auftritt, schlägt der Dienst fehl und gibt in der Regel einen Fehlerstatus Indikator zurück.</span><span class="sxs-lookup"><span data-stu-id="ed250-113">If a guard page exception occurs during a system service, the service fails and typically returns some failure status indicator.</span></span> <span data-ttu-id="ed250-114">Da das System auch den Status der Guard-Seite der relevanten Arbeitsspeicher Seite entfernt, schlägt der nächste Aufruf desselben System dienstanders aufgrund einer Ausnahme der **statusschutzseitenverletzung \_ \_ \_** nicht fehl (es sei denn, natürlich wird die Schutz Seite wieder hergestellt).</span><span class="sxs-lookup"><span data-stu-id="ed250-114">Since the system also removes the relevant memory page's guard page status, the next invocation of the same system service won't fail due to a **STATUS\_GUARD\_PAGE\_VIOLATION** exception (unless, of course, someone reestablishes the guard page).</span></span>

<span data-ttu-id="ed250-115">Das folgende kurze Programm veranschaulicht das Verhalten des Schutzes von Schutz Seiten.</span><span class="sxs-lookup"><span data-stu-id="ed250-115">The following short program illustrates the behavior of guard page protection.</span></span>


```C++
/* A program to demonstrate the use of guard pages of memory. Allocate
   a page of memory as a guard page, then try to access the page. That
   will fail, but doing so releases the lock on the guard page, so the
   next access works correctly.

   The output will look like this. The actual address may vary.

   This computer has a page size of 4096.
   Committed 4096 bytes at address 0x00520000
   Cannot lock at 00520000, error = 0x80000001
   2nd Lock Achieved at 00520000

   This sample does not show how to use the guard page fault to
   "grow" a dynamic array, such as a stack. */

#include <windows.h>
#include <stdio.h>
#include <stdlib.h>
#include <tchar.h>

int main()
{
  LPVOID lpvAddr;               // address of the test memory
  DWORD dwPageSize;             // amount of memory to allocate.
  BOOL bLocked;                 // address of the guarded memory
  SYSTEM_INFO sSysInfo;         // useful information about the system

  GetSystemInfo(&sSysInfo);     // initialize the structure

  _tprintf(TEXT("This computer has page size %d.\n"), sSysInfo.dwPageSize);

  dwPageSize = sSysInfo.dwPageSize;

  // Try to allocate the memory.

  lpvAddr = VirtualAlloc(NULL, dwPageSize,
                         MEM_RESERVE | MEM_COMMIT,
                         PAGE_READONLY | PAGE_GUARD);

  if(lpvAddr == NULL) {
    _tprintf(TEXT("VirtualAlloc failed. Error: %ld\n"),
             GetLastError());
    return 1;

  } else {
    _ftprintf(stderr, TEXT("Committed %lu bytes at address 0x%lp\n"),
              dwPageSize, lpvAddr);
  }

  // Try to lock the committed memory. This fails the first time 
  // because of the guard page.

  bLocked = VirtualLock(lpvAddr, dwPageSize);
  if (!bLocked) {
    _ftprintf(stderr, TEXT("Cannot lock at %lp, error = 0x%lx\n"),
              lpvAddr, GetLastError());
  } else {
    _ftprintf(stderr, TEXT("Lock Achieved at %lp\n"), lpvAddr);
  }

  // Try to lock the committed memory again. This succeeds the second
  // time because the guard page status was removed by the first 
  // access attempt.

  bLocked = VirtualLock(lpvAddr, dwPageSize);

  if (!bLocked) {
    _ftprintf(stderr, TEXT("Cannot get 2nd lock at %lp, error = %lx\n"),
              lpvAddr, GetLastError());
  } else {
    _ftprintf(stderr, TEXT("2nd Lock Achieved at %lp\n"), lpvAddr);
  }

  return 0;
}
```



<span data-ttu-id="ed250-116">Beim ersten Versuch, den Speicherblock zu sperren, tritt ein Fehler auf, und es wird eine Ausnahme der **\_ statusschutzseite \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ed250-116">The first attempt to lock the memory block fails, raising a **STATUS\_GUARD\_PAGE\_VIOLATION** exception.</span></span> <span data-ttu-id="ed250-117">Der zweite Versuch ist erfolgreich, da der Schutz der Schutz Seite des Speicherblocks beim ersten Versuch deaktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="ed250-117">The second attempt succeeds, because the memory block's guard page protection has been toggled off by the first attempt.</span></span>

 

 
