---
description: Um Daten freizugeben, können mehrere Prozesse speicherzuordnungsbasierte Dateien verwenden, die in der Auslagerungsdatei des Systems gespeichert werden.
ms.assetid: 17458be2-3ef7-42f2-a717-abf73ac4846f
title: Erstellen von benanntem freigegebenen Arbeitsspeicher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2fc5ec3d9865d310807d01ac9f76967d4378fc92e4c9588d00b2933a08c953f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869920"
---
# <a name="creating-named-shared-memory"></a>Erstellen von benanntem freigegebenen Arbeitsspeicher

Um Daten freizugeben, können mehrere Prozesse speicherzuordnungsbasierte Dateien verwenden, die in der Auslagerungsdatei des Systems gespeichert werden.

## <a name="first-process"></a>Erster Prozess

Der erste Prozess erstellt das Dateizuordnungsobjekt, indem die [**CreateFileMapping-Funktion**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) mit **INVALID HANDLE \_ \_ VALUE** und einem Namen für das Objekt aufgerufen wird. Mithilfe des **PAGE \_ READWRITE-Flags** verfügt der Prozess über Lese-/Schreibberechtigungen für den Arbeitsspeicher über alle erstellten Dateiansichten.

Anschließend verwendet der Prozess das Dateizuordnungsobjekthandle, das [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) in einem Aufruf von [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) zurückgibt, um eine Ansicht der Datei im Prozessadressraum zu erstellen. Die **MapViewOfFile-Funktion** gibt einen Zeiger auf die Dateiansicht `pBuf` zurück. Der Prozess verwendet dann die [**CopyMemory-Funktion,**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)) um eine Zeichenfolge in die Ansicht zu schreiben, auf die andere Prozesse zugreifen können.

Durch das Präfix der Dateizuordnungsobjektnamen mit \\ "Global" können Prozesse miteinander kommunizieren, auch wenn sie sich in verschiedenen Terminalserversitzungen befinden. Dies erfordert, dass der erste Prozess über die [**SeCreateGlobalPrivilege-Berechtigung verfügt.**](../secauthz/privilege-constants.md)

Wenn der Prozess keinen Zugriff mehr auf das Dateizuordnungsobjekt benötigt, sollte er die [**CloseHandle-Funktion**](/windows/win32/api/handleapi/nf-handleapi-closehandle) aufrufen. Wenn alle Handles geschlossen sind, kann das System den Abschnitt der paging-Datei freigeben, die das -Objekt verwendet.


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



## <a name="second-process"></a>Zweiter Prozess

Ein zweiter Prozess kann auf die Zeichenfolge zugreifen, die vom ersten Prozess in den freigegebenen Arbeitsspeicher geschrieben wurde, indem die [**OpenFileMapping-Funktion**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) aufgerufen wird, die den gleichen Namen für das Zuordnungsobjekt wie der erste Prozess angibt. Anschließend kann die [**MapViewOfFile-Funktion**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) verwendet werden, um einen Zeiger auf die Dateiansicht `pBuf` abzurufen. Der Prozess kann diese Zeichenfolge wie jede andere Zeichenfolge anzeigen. In diesem Beispiel enthält das angezeigte Meldungsfeld die Meldung "Nachricht vom ersten Prozess", die vom ersten Prozess geschrieben wurde.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Freigeben von Dateien und Arbeitsspeicher](sharing-files-and-memory.md)
</dt> </dl>

 

 
