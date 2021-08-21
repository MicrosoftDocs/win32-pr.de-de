---
description: Eine Schutzseite bietet einen einmaligen Alarm für den Zugriff auf die Speicherseite.
ms.assetid: 763bc763-e178-481e-a81a-c15715e56901
title: Erstellen von Guard Pages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fee4d4a44a6e64d6af81e4b847347f357c3590edbd7e6b806e8f32653e1f869
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963290"
---
# <a name="creating-guard-pages"></a>Erstellen von Guard Pages

Eine Schutzseite bietet einen einmaligen Alarm für den Zugriff auf die Speicherseite. Dies kann für eine Anwendung nützlich sein, die das Wachstum großer dynamischer Datenstrukturen überwachen muss. Es gibt beispielsweise Betriebssysteme, die Schutzseiten verwenden, um die automatische Stapelüberprüfung zu implementieren.

Um eine Schutzseite zu erstellen, legen Sie den Seitenschutzmodifizierer **PAGE \_ GUARD** für die Seite fest. Dieser Wert kann zusammen mit anderen Seitenschutzmodifizierern in den Funktionen [**VirtualAlloc,**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) [**VirtualAllocEx,**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect)und [**VirtualProtectEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotectex) angegeben werden. Der **PAGE GUARD-Modifizierer \_** kann mit allen anderen Seitenschutzmodifizierern außer **PAGE \_ NOACCESS** verwendet werden.

Wenn ein Programm versucht, auf eine Adresse innerhalb einer Schutzseite zuzugreifen, löst das System eine **STATUS \_ GUARD PAGE \_ VIOLATION(0x80000001)-Ausnahme \_** aus. Das System löscht auch den **PAGE GUARD-Modifizierer, \_** wodurch der Status der Schutzseite der Speicherseite entfernt wird. Das System beendet nicht den nächsten Versuch, mit einer **STATUS \_ GUARD PAGE \_ \_ VIOLATION-Ausnahme** auf die Speicherseite zuzugreifen.

Wenn während eines Systemdiensts eine Schutzseitenausnahme auftritt, schlägt der Dienst fehl und gibt in der Regel einen Fehlerstatusindikator zurück. Da das System auch den Schutzseitenstatus der relevanten Speicherseite entfernt, schlägt der nächste Aufruf desselben Systemdiensts aufgrund einer **STATUS \_ GUARD PAGE \_ \_ VIOLATION-Ausnahme** nicht fehl (es sei denn, die Schutzseite wird wieder hergestellt).

Das folgende kurze Programm veranschaulicht das Verhalten des Wächterseitenschutzes.


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



Der erste Versuch, den Speicherblock zu sperren, schlägt fehl und löst eine **STATUS \_ GUARD PAGE \_ \_ VIOLATION-Ausnahme** aus. Der zweite Versuch ist erfolgreich, da der Schutz der Schutzseite des Speicherblocks beim ersten Versuch deaktiviert wurde.

 

 
