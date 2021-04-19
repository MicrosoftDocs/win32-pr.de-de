---
description: In diesem Abschnitt wird die Verwendung einer DLL-Einstiegspunkt Funktion zum Einrichten eines Thread lokalen Speicher Index (TLS) zum Bereitstellen des privaten Speichers für jeden Thread eines multithreadprozesses veranschaulicht.
ms.assetid: a300f223-b513-4a22-a7a4-5d98cf74d77d
title: Verwenden des lokalen Thread Speichers in einer Dynamic-Link-Bibliothek
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 261ef7482520b4cb6e6c7b630f10ebb456231283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347851"
---
# <a name="using-thread-local-storage-in-a-dynamic-link-library"></a>Verwenden des lokalen Thread Speichers in einer Dynamic-Link-Bibliothek

In diesem Abschnitt wird die Verwendung einer DLL-Einstiegspunkt Funktion zum Einrichten eines Thread lokalen Speicher Index (TLS) zum Bereitstellen des privaten Speichers für jeden Thread eines multithreadprozesses veranschaulicht.

Der TLS-Index wird in einer globalen Variablen gespeichert, sodass er für alle DLL-Funktionen verfügbar ist. In diesem Beispiel wird davon ausgegangen, dass die globalen Daten der dll nicht freigegeben werden, da der TLS-Index für jeden Prozess, der die dll lädt, nicht notwendigerweise identisch ist.

Die Einstiegspunkt Funktion verwendet die [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) -Funktion, um einen TLS-Index zuzuweisen, wenn ein Prozess die dll lädt. Jeder Thread kann diesen Index dann verwenden, um einen Zeiger auf seinen eigenen Speicherblock zu speichern.

Wenn die Einstiegspunkt Funktion mit dem Anfüge Wert des dll-Prozesses aufgerufen wird \_ \_ , führt der Code die folgenden Aktionen aus:

1.  Verwendet die [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) -Funktion, um einen TLS-Index zuzuordnen.
2.  Ordnet einen Speicherblock zu, der exklusiv vom ursprünglichen Thread des Prozesses verwendet werden soll.
3.  Verwendet den TLS-Index in einem Aufrufe der [**TlsSetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlssetvalue) -Funktion, um die Adresse des Speicherblocks in dem TLS-Slot zu speichern, der dem Index zugeordnet ist.

Jedes Mal, wenn der Prozess einen neuen Thread erstellt, wird die Einstiegspunkt Funktion mit dem \_ Anfüge Wert des dll-Threads aufgerufen \_ . Die Einstiegspunkt Funktion ordnet dann einen Speicherblock für den neuen Thread zu und speichert einen Zeiger darauf mithilfe des TLS-Indexes.

Wenn eine Funktion Zugriff auf die Daten erfordert, die einem TLS-Index zugeordnet sind, geben Sie den Index in einem Aufrufen der [**TlsGetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) -Funktion an. Dadurch wird der Inhalt des TLS-Slots für den aufrufenden Thread abgerufen, bei dem es sich in diesem Fall um einen Zeiger auf den Speicherblock für die Daten handelt. Wenn ein Prozess Lade Zeit-Verknüpfungen mit dieser DLL verwendet, reicht die Einstiegspunkt Funktion aus, um den lokalen Thread Speicher zu verwalten. Es können Probleme bei einem Prozess auftreten, der die Laufzeit-Verknüpfung verwendet, da die Einstiegspunkt Funktion nicht für Threads aufgerufen wird, die vor dem Aufruf der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion vorhanden sind, sodass der TLS-Speicher für diese Threads nicht zugeordnet wird. In diesem Beispiel wird dieses Problem gelöst, indem der von der [**TlsGetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) -Funktion zurückgegebene Wert überprüft und Arbeitsspeicher belegt wird, wenn der Wert angibt, dass der TLS-Slot für diesen Thread nicht festgelegt ist.

Wenn jeder Thread keinen TLS-Index mehr verwenden muss, muss der Arbeitsspeicher freigegeben werden, dessen Zeiger im TLS-Slot gespeichert wird. Wenn alle Threads einen TLS-Index verwendet haben, verwenden Sie die [**TlsFree**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsfree) -Funktion, um den Index freizugeben.

Wenn ein Thread beendet wird, wird die Einstiegspunkt Funktion mit dem \_ Trenn Wert des dll-Threads aufgerufen, \_ und der Speicher für diesen Thread wird freigegeben. Wenn ein Prozess beendet wird, wird die Einstiegspunkt Funktion mit dem \_ Trenn Wert des dll-Prozesses aufgerufen, \_ und der Speicher, auf den der Zeiger im TLS-Index verweist, wird freigegeben.


```C++
// The DLL code

#include <windows.h>

static DWORD dwTlsIndex; // address of shared memory
 
// DllMain() is the entry-point function for this DLL. 
 
BOOL WINAPI DllMain(HINSTANCE hinstDLL, // DLL module handle
    DWORD fdwReason,                    // reason called
    LPVOID lpvReserved)                 // reserved
{ 
    LPVOID lpvData; 
    BOOL fIgnore; 
 
    switch (fdwReason) 
    { 
        // The DLL is loading due to process 
        // initialization or a call to LoadLibrary. 
 
        case DLL_PROCESS_ATTACH: 
 
            // Allocate a TLS index.
 
            if ((dwTlsIndex = TlsAlloc()) == TLS_OUT_OF_INDEXES) 
                return FALSE; 
 
            // No break: Initialize the index for first thread.
 
        // The attached process creates a new thread. 
 
        case DLL_THREAD_ATTACH: 
 
            // Initialize the TLS index for this thread.
 
            lpvData = (LPVOID) LocalAlloc(LPTR, 256); 
            if (lpvData != NULL) 
                fIgnore = TlsSetValue(dwTlsIndex, lpvData); 
 
            break; 
 
        // The thread of the attached process terminates.
 
        case DLL_THREAD_DETACH: 
 
            // Release the allocated memory for this thread.
 
            lpvData = TlsGetValue(dwTlsIndex); 
            if (lpvData != NULL) 
                LocalFree((HLOCAL) lpvData); 
 
            break; 
 
        // DLL unload due to process termination or FreeLibrary. 
 
        case DLL_PROCESS_DETACH: 
 
            // Release the allocated memory for this thread.
 
            lpvData = TlsGetValue(dwTlsIndex); 
            if (lpvData != NULL) 
                LocalFree((HLOCAL) lpvData); 
 
            // Release the TLS index.
 
            TlsFree(dwTlsIndex); 
            break; 
 
        default: 
            break; 
    } 
 
    return TRUE; 
    UNREFERENCED_PARAMETER(hinstDLL); 
    UNREFERENCED_PARAMETER(lpvReserved); 
}

// The export mechanism used here is the __declspec(export)
// method supported by Microsoft Visual Studio, but any
// other export method supported by your development
// environment may be substituted.

#ifdef __cplusplus    // If used by C++ code, 
extern "C" {          // we need to export the C interface
#endif

__declspec(dllexport)
BOOL WINAPI StoreData(DWORD dw)
{
   LPVOID lpvData; 
   DWORD * pData;  // The stored memory pointer 

   lpvData = TlsGetValue(dwTlsIndex); 
   if (lpvData == NULL)
   {
      lpvData = (LPVOID) LocalAlloc(LPTR, 256); 
      if (lpvData == NULL) 
         return FALSE;
      if (!TlsSetValue(dwTlsIndex, lpvData))
         return FALSE;
   }

   pData = (DWORD *) lpvData; // Cast to my data type.
   // In this example, it is only a pointer to a DWORD
   // but it can be a structure pointer to contain more complicated data.

   (*pData) = dw;
   return TRUE;
}

__declspec(dllexport)
BOOL WINAPI GetData(DWORD *pdw)
{
   LPVOID lpvData; 
   DWORD * pData;  // The stored memory pointer 

   lpvData = TlsGetValue(dwTlsIndex); 
   if (lpvData == NULL)
      return FALSE;

   pData = (DWORD *) lpvData;
   (*pdw) = (*pData);
   return TRUE;
}
#ifdef __cplusplus
}
#endif
```



Der folgende Code veranschaulicht die Verwendung der DLL-Funktionen, die im vorherigen Beispiel definiert wurden.


```C++
#include <windows.h> 
#include <stdio.h> 
 
#define THREADCOUNT 4 
#define DLL_NAME TEXT("testdll")

VOID ErrorExit(LPSTR); 

extern "C" BOOL WINAPI StoreData(DWORD dw);
extern "C" BOOL WINAPI GetData(DWORD *pdw);
 
DWORD WINAPI ThreadFunc(VOID) 
{   
   int i;

   if(!StoreData(GetCurrentThreadId()))
      ErrorExit("StoreData error");

   for(i=0; i<THREADCOUNT; i++)
   {
      DWORD dwOut;
      if(!GetData(&dwOut))
         ErrorExit("GetData error");
      if( dwOut != GetCurrentThreadId())
         printf("thread %d: data is incorrect (%d)\n", GetCurrentThreadId(), dwOut);
      else printf("thread %d: data is correct\n", GetCurrentThreadId());
      Sleep(0);
   }
   return 0; 
} 
 
int main(VOID) 
{ 
   DWORD IDThread; 
   HANDLE hThread[THREADCOUNT]; 
   int i; 
   HMODULE hm;
 
// Load the DLL

   hm = LoadLibrary(DLL_NAME);
   if(!hm)
   {
      ErrorExit("DLL failed to load");
   }

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
 
   WaitForMultipleObjects(THREADCOUNT, hThread, TRUE, INFINITE); 

   FreeLibrary(hm);
 
   return 0; 
} 
 
VOID ErrorExit (LPSTR lpszMessage) 
{ 
   fprintf(stderr, "%s\n", lpszMessage); 
   ExitProcess(0); 
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Dynamic Link Library-Daten](dynamic-link-library-data.md)
</dt> <dt>

[Verwenden von TLS (threadlokaler Speicher)](/windows/desktop/ProcThread/using-thread-local-storage)
</dt> </dl>

 

 
