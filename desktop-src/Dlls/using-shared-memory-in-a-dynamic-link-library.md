---
description: Im folgenden Beispiel wird veranschaulicht, wie die DLL-Einstiegspunkt Funktion ein Datei Zuordnungs Objekt zum Einrichten von Speicher verwenden kann, der von Prozessen gemeinsam genutzt werden kann, die die DLL laden.
ms.assetid: ab751ab1-3b40-4111-b724-9f8676b722a3
title: Verwenden von frei gegebenem Speicher in einer Dynamic-Link Bibliothek
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 978a6fa77964c6404b3f85e9c9bcec6c3644f2ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863372"
---
# <a name="using-shared-memory-in-a-dynamic-link-library"></a>Verwenden von frei gegebenem Speicher in einer Dynamic-Link Bibliothek

Im folgenden Beispiel wird veranschaulicht, wie die DLL-Einstiegspunkt Funktion ein Datei Zuordnungs Objekt zum Einrichten von Speicher verwenden kann, der von Prozessen gemeinsam genutzt werden kann, die die DLL laden. Der freigegebene DLL-Speicher bleibt nur bestehen, solange die dll geladen wird. Anwendungen können die Funktionen setsharedmem und getsharedmem verwenden, um auf den freigegebenen Speicher zuzugreifen.

## <a name="dll-that-implements-the-shared-memory"></a>DLL, die den freigegebenen Speicher implementiert

Im Beispiel wird die Datei Zuordnung verwendet, um einen Block mit dem Namen Shared Memory dem virtuellen Adressraum jedes Prozesses zuzuordnen, der die dll lädt. Zu diesem Zweck muss die Einstiegspunkt Funktion folgende Aktionen ausführen:

1.  Aufrufen der Funktion "Anordnen [**von Dateien"**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga) , um ein Handle für ein Datei Zuordnung-Objekt zu erhalten. Der erste Prozess, bei dem die dll geladen wird, erstellt das Datei Zuordnung-Objekt. Nachfolgende Prozesse öffnen ein Handle für das vorhandene Objekt. Weitere Informationen finden Sie unter [Erstellen eines File-Mapping Objekts](/windows/desktop/Memory/creating-a-file-mapping-object).
2.  Nennen Sie die [**MapViewOfFile**](/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffile) -Funktion, um eine Ansicht dem virtuellen Adressraum zuzuordnen. Dies ermöglicht es dem Prozess, auf den freigegebenen Speicher zuzugreifen. Weitere Informationen finden Sie unter [Erstellen einer Dateiansicht](/windows/desktop/Memory/creating-a-file-view).

Beachten Sie, dass Sie zwar Standard Sicherheits Attribute angeben können, indem Sie einen NULL-Wert für den *lpattributes* -Parameter von " [**kreatefilemapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga)" übergeben. Sie können jedoch auch eine [**Sicherheits \_ Attribut**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) Struktur verwenden, um zusätzliche Sicherheit bereitzustellen.


```C++
// The DLL code

#include <windows.h> 
#include <memory.h> 
 
#define SHMEMSIZE 4096 
 
static LPVOID lpvMem = NULL;      // pointer to shared memory
static HANDLE hMapObject = NULL;  // handle to file mapping

// The DLL entry-point function sets up shared memory using a 
// named file-mapping object. 
 
BOOL WINAPI DllMain(HINSTANCE hinstDLL,  // DLL module handle
    DWORD fdwReason,              // reason called 
    LPVOID lpvReserved)           // reserved 
{ 
    BOOL fInit, fIgnore; 
 
    switch (fdwReason) 
    { 
        // DLL load due to process initialization or LoadLibrary
 
          case DLL_PROCESS_ATTACH: 
 
            // Create a named file mapping object
 
            hMapObject = CreateFileMapping( 
                INVALID_HANDLE_VALUE,   // use paging file
                NULL,                   // default security attributes
                PAGE_READWRITE,         // read/write access
                0,                      // size: high 32-bits
                SHMEMSIZE,              // size: low 32-bits
                TEXT("dllmemfilemap")); // name of map object
            if (hMapObject == NULL) 
                return FALSE; 
 
            // The first process to attach initializes memory
 
            fInit = (GetLastError() != ERROR_ALREADY_EXISTS); 
 
            // Get a pointer to the file-mapped shared memory
 
            lpvMem = MapViewOfFile( 
                hMapObject,     // object to map view of
                FILE_MAP_WRITE, // read/write access
                0,              // high offset:  map from
                0,              // low offset:   beginning
                0);             // default: map entire file
            if (lpvMem == NULL) 
                return FALSE; 
 
            // Initialize memory if this is the first process
 
            if (fInit) 
                memset(lpvMem, '\0', SHMEMSIZE); 
 
            break; 
 
        // The attached process creates a new thread
 
        case DLL_THREAD_ATTACH: 
            break; 
 
        // The thread of the attached process terminates
 
        case DLL_THREAD_DETACH: 
            break; 
 
        // DLL unload due to process termination or FreeLibrary
 
        case DLL_PROCESS_DETACH: 
 
            // Unmap shared memory from the process's address space
 
            fIgnore = UnmapViewOfFile(lpvMem); 
 
            // Close the process's handle to the file-mapping object
 
            fIgnore = CloseHandle(hMapObject); 
 
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
 
// SetSharedMem sets the contents of the shared memory 
 
__declspec(dllexport) VOID __cdecl SetSharedMem(LPWSTR lpszBuf) 
{ 
    LPWSTR lpszTmp; 
    DWORD dwCount=1;
 
    // Get the address of the shared memory block
 
    lpszTmp = (LPWSTR) lpvMem; 
 
    // Copy the null-terminated string into shared memory
 
    while (*lpszBuf && dwCount<SHMEMSIZE) 
    {
        *lpszTmp++ = *lpszBuf++; 
        dwCount++;
    }
    *lpszTmp = '\0'; 
} 
 
// GetSharedMem gets the contents of the shared memory
 
__declspec(dllexport) VOID __cdecl GetSharedMem(LPWSTR lpszBuf, DWORD cchSize) 
{ 
    LPWSTR lpszTmp; 
 
    // Get the address of the shared memory block
 
    lpszTmp = (LPWSTR) lpvMem; 
 
    // Copy from shared memory into the caller's buffer
 
    while (*lpszTmp && --cchSize) 
        *lpszBuf++ = *lpszTmp++; 
    *lpszBuf = '\0'; 
}
#ifdef __cplusplus
}
#endif
```



Gemeinsam genutzter Arbeitsspeicher kann einer anderen Adresse in jedem Prozess zugeordnet werden. Aus diesem Grund verfügt jeder Prozess über eine eigene Instanz von lpvmem, die als globale Variable deklariert ist, sodass Sie für alle DLL-Funktionen verfügbar ist. Im Beispiel wird davon ausgegangen, dass die globalen DLL-Daten nicht freigegeben werden, sodass jeder Prozess, der die dll lädt, über eine eigene Instanz von lpvmem verfügt.

Beachten Sie, dass der freigegebene Speicher freigegeben wird, wenn das letzte Handle für das Datei Zuordnung-Objekt geschlossen wird. Um permanenten gemeinsam genutzten Speicher zu erstellen, müssen Sie sicherstellen, dass ein Prozess immer über ein geöffnetes Handle für das Datei Zuordnung-Objekt verfügt.

## <a name="processes-that-use-the-shared-memory"></a>Prozesse, die den freigegebenen Arbeitsspeicher verwenden

Die folgenden Prozesse verwenden den gemeinsam genutzten Speicher, der von der oben definierten dll bereitgestellt wird. Der erste Prozess ruft setsharedmem auf, um eine Zeichenfolge zu schreiben, während der zweite Prozess getsharedmem aufruft, um diese Zeichenfolge abzurufen.

Dieser Prozess verwendet die setsharedmem-Funktion, die von der dll implementiert wird, um die Zeichenfolge "Dies ist eine Test Zeichenfolge" in den freigegebenen Speicher zu schreiben. Außerdem wird ein untergeordneter Prozess gestartet, mit dem die Zeichenfolge aus dem freigegebenen Speicher gelesen wird.


```C++
// Parent process

#include <windows.h>
#include <tchar.h>
#include <stdio.h>

extern "C" VOID __cdecl SetSharedMem(LPWSTR lpszBuf);

HANDLE CreateChildProcess(LPTSTR szCmdline) 
{ 
   PROCESS_INFORMATION piProcInfo; 
   STARTUPINFO siStartInfo;
   BOOL bFuncRetn = FALSE; 
 
// Set up members of the PROCESS_INFORMATION structure. 
 
   ZeroMemory( &piProcInfo, sizeof(PROCESS_INFORMATION) );
 
// Set up members of the STARTUPINFO structure. 
 
   ZeroMemory( &siStartInfo, sizeof(STARTUPINFO) );
   siStartInfo.cb = sizeof(STARTUPINFO); 
 
// Create the child process. 
    
   bFuncRetn = CreateProcess(NULL, 
      szCmdline,     // command line 
      NULL,          // process security attributes 
      NULL,          // primary thread security attributes 
      TRUE,          // handles are inherited 
      0,             // creation flags 
      NULL,          // use parent's environment 
      NULL,          // use parent's current directory 
      &siStartInfo,  // STARTUPINFO pointer 
      &piProcInfo);  // receives PROCESS_INFORMATION 
   
   if (bFuncRetn == 0) 
   {
      printf("CreateProcess failed (%)\n", GetLastError());
      return INVALID_HANDLE_VALUE;
   }
   else 
   {
      CloseHandle(piProcInfo.hThread);
      return piProcInfo.hProcess;
   }
}

int _tmain(int argc, TCHAR *argv[])
{
   HANDLE hProcess;

   if (argc == 1) 
   {
      printf("Please specify an input file");
      ExitProcess(0);
   }

   // Call the DLL function
   printf("\nProcess is writing to shared memory...\n\n");
   SetSharedMem(L"This is a test string");

   // Start the child process that will read the memory
   hProcess = CreateChildProcess(argv[1]);

   // Ensure this process is around until the child process terminates
   if (INVALID_HANDLE_VALUE != hProcess) 
   {
      WaitForSingleObject(hProcess, INFINITE);
      CloseHandle(hProcess);
   }
   return 0;
}

```



Dieser Prozess verwendet die getsharedmem-Funktion, die von der dll implementiert wird, um eine Zeichenfolge aus dem gemeinsam genutzten Speicher zu lesen. Sie wird vom übergeordneten Prozess oben gestartet.


```C++
// Child process

#include <windows.h>
#include <tchar.h>
#include <stdio.h>

extern "C" VOID __cdecl GetSharedMem(LPWSTR lpszBuf, DWORD cchSize);

int _tmain( void )
{
    WCHAR cBuf[MAX_PATH];

    GetSharedMem(cBuf, MAX_PATH);
 
    printf("Child process read from shared memory: %S\n", cBuf);
    
    return 0;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Dynamic Link Library-Daten](dynamic-link-library-data.md)
</dt> </dl>

 

 
