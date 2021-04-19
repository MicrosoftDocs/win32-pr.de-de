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
# <a name="creating-named-shared-memory"></a>Erstellen von benanntem Shared Memory

Zum Freigeben von Daten können mehrere Prozesse im Speicher abgebildete Dateien verwenden, die vom System Auslagerungs Dateien gespeichert werden.

## <a name="first-process"></a>Erster Prozess

Der erste Prozess erstellt das Datei Zuordnung-Objekt durch Aufrufen der [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) -Funktion mit einem **ungültigen \_ handle- \_ Wert** und einem Namen für das Objekt. Mit dem Flag für die **Seiten \_ Lese** Berechtigung verfügt der Prozess über die Lese-/Schreibberechtigung für den Arbeitsspeicher über alle erstellten Datei Sichten.

Anschließend verwendet der Prozess das Datei zuordnungsobjekthandle, das von " [**kreatefilemapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) " in einem Befehl von " [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) " zurückgegeben wird, um eine Ansicht der Datei im Prozess Adressraum zu erstellen. Die **MapViewOfFile** -Funktion gibt einen Zeiger auf die Dateiansicht zurück `pBuf` . Der Prozess verwendet dann die [**CopyMemory**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)) -Funktion, um eine Zeichenfolge in die Sicht zu schreiben, auf die von anderen Prozessen zugegriffen werden kann.

Durch die vorab Korrektur der Datei zuordnungsobjektnamen mit "Global \\ " können Prozesse miteinander kommunizieren, auch wenn Sie sich in unterschiedlichen Terminal Server Sitzungen befinden. Hierfür muss der erste Prozess über die Berechtigung " [**SeCreateGlobalPrivilege**](../secauthz/privilege-constants.md) " verfügen.

Wenn der Prozess keinen Zugriff mehr auf das Datei Zuordnungs Objekt benötigt, sollte er die [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) -Funktion aufrufen. Wenn alle Handles geschlossen sind, kann das System den Abschnitt der vom Objekt verwendeten Auslagerungs Datei freigeben.


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

Ein zweiter Prozess kann durch Aufrufen der [**OpenFileMapping**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) -Funktion auf die Zeichenfolge zugreifen, die vom ersten Prozess in den gemeinsam genutzten Speicher geschrieben wird. dabei wird der gleiche Name für das Zuordnungs Objekt als der erste Prozess angegeben. Anschließend kann Sie die [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) -Funktion verwenden, um einen Zeiger auf die Dateiansicht zu erhalten `pBuf` . Der Prozess kann diese Zeichenfolge wie jede andere Zeichenfolge anzeigen. In diesem Beispiel enthält das angezeigte Meldungs Feld die Meldung "Meldung vom ersten Prozess", die vom ersten Prozess geschrieben wurde.


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

 

 
