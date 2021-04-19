---
description: Zum Freigeben von Daten können mehrere Prozesse im Speicher abgebildete Dateien verwenden, die vom System Auslagerungs Dateien gespeichert werden.
ms.assetid: 17458be2-3ef7-42f2-a717-abf73ac4846f
title: Erstellen von benanntem Shared Memory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18ac708497ceb12ed099c7a9c0b3788d7a05a925
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346511"
---
# <a name="creating-named-shared-memory"></a><span data-ttu-id="cb017-103">Erstellen von benanntem Shared Memory</span><span class="sxs-lookup"><span data-stu-id="cb017-103">Creating Named Shared Memory</span></span>

<span data-ttu-id="cb017-104">Zum Freigeben von Daten können mehrere Prozesse im Speicher abgebildete Dateien verwenden, die vom System Auslagerungs Dateien gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="cb017-104">To share data, multiple processes can use memory-mapped files that the system paging file stores.</span></span>

## <a name="first-process"></a><span data-ttu-id="cb017-105">Erster Prozess</span><span class="sxs-lookup"><span data-stu-id="cb017-105">First Process</span></span>

<span data-ttu-id="cb017-106">Der erste Prozess erstellt das Datei Zuordnung-Objekt durch Aufrufen der [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) -Funktion mit einem **ungültigen \_ handle- \_ Wert** und einem Namen für das Objekt.</span><span class="sxs-lookup"><span data-stu-id="cb017-106">The first process creates the file mapping object by calling the [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) function with **INVALID\_HANDLE\_VALUE** and a name for the object.</span></span> <span data-ttu-id="cb017-107">Mit dem Flag für die **Seiten \_ Lese** Berechtigung verfügt der Prozess über die Lese-/Schreibberechtigung für den Arbeitsspeicher über alle erstellten Datei Sichten.</span><span class="sxs-lookup"><span data-stu-id="cb017-107">By using the **PAGE\_READWRITE** flag, the process has read/write permission to the memory through any file views that are created.</span></span>

<span data-ttu-id="cb017-108">Anschließend verwendet der Prozess das Datei zuordnungsobjekthandle, das von " [**kreatefilemapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) " in einem Befehl von " [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) " zurückgegeben wird, um eine Ansicht der Datei im Prozess Adressraum zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="cb017-108">Then the process uses the file mapping object handle that [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) returns in a call to [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) to create a view of the file in the process address space.</span></span> <span data-ttu-id="cb017-109">Die **MapViewOfFile** -Funktion gibt einen Zeiger auf die Dateiansicht zurück `pBuf` .</span><span class="sxs-lookup"><span data-stu-id="cb017-109">The **MapViewOfFile** function returns a pointer to the file view, `pBuf`.</span></span> <span data-ttu-id="cb017-110">Der Prozess verwendet dann die [**CopyMemory**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)) -Funktion, um eine Zeichenfolge in die Sicht zu schreiben, auf die von anderen Prozessen zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="cb017-110">The process then uses the [**CopyMemory**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)) function to write a string to the view that can be accessed by other processes.</span></span>

<span data-ttu-id="cb017-111">Durch die vorab Korrektur der Datei zuordnungsobjektnamen mit "Global \\ " können Prozesse miteinander kommunizieren, auch wenn Sie sich in unterschiedlichen Terminal Server Sitzungen befinden.</span><span class="sxs-lookup"><span data-stu-id="cb017-111">Prefixing the file mapping object names with "Global\\" allows processes to communicate with each other even if they are in different terminal server sessions.</span></span> <span data-ttu-id="cb017-112">Hierfür muss der erste Prozess über die Berechtigung " [**SeCreateGlobalPrivilege**](../secauthz/privilege-constants.md) " verfügen.</span><span class="sxs-lookup"><span data-stu-id="cb017-112">This requires that the first process must have the [**SeCreateGlobalPrivilege**](../secauthz/privilege-constants.md) privilege.</span></span>

<span data-ttu-id="cb017-113">Wenn der Prozess keinen Zugriff mehr auf das Datei Zuordnungs Objekt benötigt, sollte er die [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="cb017-113">When the process no longer needs access to the file mapping object, it should call the [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) function.</span></span> <span data-ttu-id="cb017-114">Wenn alle Handles geschlossen sind, kann das System den Abschnitt der vom Objekt verwendeten Auslagerungs Datei freigeben.</span><span class="sxs-lookup"><span data-stu-id="cb017-114">When all handles are closed, the system can free the section of the paging file that the object uses.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <conio.h>
#include <tchar.h>

#define BUF_SIZE 256
TCHAR szName[]=TEXT("Global\\MyFileMappingObject");
TCHAR szMsg[]=TEXT("Message from first process.");

int _tmain()
{
   HANDLE hMapFile;
   LPCTSTR pBuf;

   hMapFile = CreateFileMapping(
                 INVALID_HANDLE_VALUE,    // use paging file
                 NULL,                    // default security
                 PAGE_READWRITE,          // read/write access
                 0,                       // maximum object size (high-order DWORD)
                 BUF_SIZE,                // maximum object size (low-order DWORD)
                 szName);                 // name of mapping object

   if (hMapFile == NULL)
   {
      _tprintf(TEXT("Could not create file mapping object (%d).\n"),
             GetLastError());
      return 1;
   }
   pBuf = (LPTSTR) MapViewOfFile(hMapFile,   // handle to map object
                        FILE_MAP_ALL_ACCESS, // read/write permission
                        0,
                        0,
                        BUF_SIZE);

   if (pBuf == NULL)
   {
      _tprintf(TEXT("Could not map view of file (%d).\n"),
             GetLastError());

       CloseHandle(hMapFile);

      return 1;
   }


   CopyMemory((PVOID)pBuf, szMsg, (_tcslen(szMsg) * sizeof(TCHAR)));
    _getch();

   UnmapViewOfFile(pBuf);

   CloseHandle(hMapFile);

   return 0;
}
```



## <a name="second-process"></a><span data-ttu-id="cb017-115">Zweiter Prozess</span><span class="sxs-lookup"><span data-stu-id="cb017-115">Second Process</span></span>

<span data-ttu-id="cb017-116">Ein zweiter Prozess kann durch Aufrufen der [**OpenFileMapping**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) -Funktion auf die Zeichenfolge zugreifen, die vom ersten Prozess in den gemeinsam genutzten Speicher geschrieben wird. dabei wird der gleiche Name für das Zuordnungs Objekt als der erste Prozess angegeben.</span><span class="sxs-lookup"><span data-stu-id="cb017-116">A second process can access the string written to the shared memory by the first process by calling the [**OpenFileMapping**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) function specifying the same name for the mapping object as the first process.</span></span> <span data-ttu-id="cb017-117">Anschließend kann Sie die [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) -Funktion verwenden, um einen Zeiger auf die Dateiansicht zu erhalten `pBuf` .</span><span class="sxs-lookup"><span data-stu-id="cb017-117">Then it can use the [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) function to obtain a pointer to the file view, `pBuf`.</span></span> <span data-ttu-id="cb017-118">Der Prozess kann diese Zeichenfolge wie jede andere Zeichenfolge anzeigen.</span><span class="sxs-lookup"><span data-stu-id="cb017-118">The process can display this string as it would any other string.</span></span> <span data-ttu-id="cb017-119">In diesem Beispiel enthält das angezeigte Meldungs Feld die Meldung "Meldung vom ersten Prozess", die vom ersten Prozess geschrieben wurde.</span><span class="sxs-lookup"><span data-stu-id="cb017-119">In this example, the message box displayed contains the message "Message from first process" that was written by the first process.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <conio.h>
#include <tchar.h>
#pragma comment(lib, "user32.lib")

#define BUF_SIZE 256
TCHAR szName[]=TEXT("Global\\MyFileMappingObject");

int _tmain()
{
   HANDLE hMapFile;
   LPCTSTR pBuf;

   hMapFile = OpenFileMapping(
                   FILE_MAP_ALL_ACCESS,   // read/write access
                   FALSE,                 // do not inherit the name
                   szName);               // name of mapping object

   if (hMapFile == NULL)
   {
      _tprintf(TEXT("Could not open file mapping object (%d).\n"),
             GetLastError());
      return 1;
   }

   pBuf = (LPTSTR) MapViewOfFile(hMapFile, // handle to map object
               FILE_MAP_ALL_ACCESS,  // read/write permission
               0,
               0,
               BUF_SIZE);

   if (pBuf == NULL)
   {
      _tprintf(TEXT("Could not map view of file (%d).\n"),
             GetLastError());

      CloseHandle(hMapFile);

      return 1;
   }

   MessageBox(NULL, pBuf, TEXT("Process2"), MB_OK);

   UnmapViewOfFile(pBuf);

   CloseHandle(hMapFile);

   return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="cb017-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cb017-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb017-121">Freigeben von Dateien und Arbeitsspeicher</span><span class="sxs-lookup"><span data-stu-id="cb017-121">Sharing Files and Memory</span></span>](sharing-files-and-memory.md)
</dt> </dl>

 

 
