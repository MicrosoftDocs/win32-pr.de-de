---
description: Der Thread lokale Speicher (TLS) ermöglicht es mehreren Threads desselben Prozesses, einen von der TlsAlloc-Funktion zugewiesenen Index zum Speichern und Abrufen eines lokalen Werts für den Thread zu verwenden.
ms.assetid: b7f5a206-a827-4b6b-86f6-5e3aea1246b7
title: Verwenden von TLS (threadlokaler Speicher)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9221d4d0d68891ab8e2d0f2462b7c0aae307c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347628"
---
# <a name="using-thread-local-storage"></a>Verwenden von TLS (threadlokaler Speicher)

Der [Thread lokale Speicher](thread-local-storage.md) (TLS) ermöglicht es mehreren Threads desselben Prozesses, einen von der [**TlsAlloc**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsalloc) -Funktion zugewiesenen Index zum Speichern und Abrufen eines lokalen Werts für den Thread zu verwenden. In diesem Beispiel wird ein Index zugeordnet, wenn der Prozess gestartet wird. Wenn die einzelnen Threads gestartet werden, wird ein Block dynamischer Arbeitsspeicher zugeordnet, und es wird ein Zeiger auf diesen Speicher im TLS-Slot mithilfe der [**TlsSetValue**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlssetvalue) -Funktion gespeichert. Die commonfunc-Funktion verwendet die [**TlsGetValue**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) -Funktion, um auf die Daten zuzugreifen, die mit dem lokalen Index des aufrufenden Threads verknüpft sind. Bevor jeder Thread beendet wird, wird der dynamische Arbeitsspeicher freigegeben. Bevor der Prozess beendet wird, ruft er [**TlsFree**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsfree) auf, um den Index freizugeben.


```C++
#include <windows.h> 
#include <stdio.h> 
 
#define THREADCOUNT 4 
DWORD dwTlsIndex; 
 
VOID ErrorExit (LPCSTR message);
 
VOID CommonFunc(VOID) 
{ 
   LPVOID lpvData; 
 
// Retrieve a data pointer for the current thread. 
 
   lpvData = TlsGetValue(dwTlsIndex); 
   if ((lpvData == 0) && (GetLastError() != ERROR_SUCCESS)) 
      ErrorExit("TlsGetValue error"); 
 
// Use the data stored for the current thread. 
 
   printf("common: thread %d: lpvData=%lx\n", 
      GetCurrentThreadId(), lpvData); 
 
   Sleep(5000); 
} 
 
DWORD WINAPI ThreadFunc(VOID) 
{ 
   LPVOID lpvData; 
 
// Initialize the TLS index for this thread. 
 
   lpvData = (LPVOID) LocalAlloc(LPTR, 256); 
   if (! TlsSetValue(dwTlsIndex, lpvData)) 
      ErrorExit("TlsSetValue error"); 
 
   printf("thread %d: lpvData=%lx\n", GetCurrentThreadId(), lpvData); 
 
   CommonFunc(); 
 
// Release the dynamic memory before the thread returns. 
 
   lpvData = TlsGetValue(dwTlsIndex); 
   if (lpvData != 0) 
      LocalFree((HLOCAL) lpvData); 
 
   return 0; 
} 
 
int main(VOID) 
{ 
   DWORD IDThread; 
   HANDLE hThread[THREADCOUNT]; 
   int i; 
 
// Allocate a TLS index. 
 
   if ((dwTlsIndex = TlsAlloc()) == TLS_OUT_OF_INDEXES) 
      ErrorExit("TlsAlloc failed"); 
 
// Create multiple threads. 
 
   for (i = 0; i < THREADCOUNT; i++) 
   { 
      hThread[i] = CreateThread(NULL, // default security attributes 
         0,                           // use default stack size 
         (LPTHREAD_START_ROUTINE) ThreadFunc, // thread function 
         NULL,                    // no thread function argument 
         0,                       // use default creation flags 
         &IDThread);              // returns thread identifier 
 
   // Check the return value for success. 
      if (hThread[i] == NULL) 
         ErrorExit("CreateThread error\n"); 
   } 
 
   for (i = 0; i < THREADCOUNT; i++) 
      WaitForSingleObject(hThread[i], INFINITE); 
 
   TlsFree(dwTlsIndex);

   return 0; 
} 
 
VOID ErrorExit (LPCSTR message)
{ 
   fprintf(stderr, "%s\n", message); 
   ExitProcess(0); 
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des lokalen Thread Speichers in einer Dynamic-Link-Bibliothek](../dlls/using-thread-local-storage-in-a-dynamic-link-library.md)
</dt> </dl>

 

 
