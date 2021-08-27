---
description: Threadlokaler Speicher (Thread Local Storage, TLS) ermöglicht es mehreren Threads desselben Prozesses, einen von der TlsAlloc-Funktion zugeordneten Index zum Speichern und Abrufen eines lokalen Werts für den Thread zu verwenden.
ms.assetid: b7f5a206-a827-4b6b-86f6-5e3aea1246b7
title: Verwenden von TLS (threadlokaler Speicher)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bdac1306a4a2da10e6a24ba2e1b2444f6215fdac39be7b41cc6850c1e5a683d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127990"
---
# <a name="using-thread-local-storage"></a>Verwenden von TLS (threadlokaler Speicher)

[Threadlokaler Speicher (Thread Local Storage,](thread-local-storage.md) TLS) ermöglicht es mehreren Threads desselben Prozesses, einen von der [**TlsAlloc-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsalloc) zugeordneten Index zum Speichern und Abrufen eines lokalen Werts für den Thread zu verwenden. In diesem Beispiel wird ein Index zugeordnet, wenn der Prozess gestartet wird. Wenn jeder Thread gestartet wird, ordnet er einen Block mit dynamischem Arbeitsspeicher zu und speichert mithilfe der [**TlsSetValue-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlssetvalue) einen Zeiger auf diesen Speicher im TLS-Slot. Die CommonFunc-Funktion verwendet die [**TlsGetValue-Funktion,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) um auf die Daten zuzugreifen, die dem Index zugeordnet sind, der für den aufrufenden Thread lokal ist. Bevor jeder Thread beendet wird, gibt er seinen dynamischen Speicher frei. Bevor der Prozess beendet wird, ruft er [**TlsFree**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsfree) auf, um den Index freizugeben.


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

[Verwenden von threadlokalen Storage in einer Dynamic-Link Bibliothek](../dlls/using-thread-local-storage-in-a-dynamic-link-library.md)
</dt> </dl>

 

 
