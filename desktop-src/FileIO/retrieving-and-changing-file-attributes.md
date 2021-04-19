---
description: Beispielcode, der zeigt, wie die Funktion getfileattributesex zum Abrufen von Dateiattributen verwendet wird.
ms.assetid: f6eaea8a-0cc2-4fb6-bec5-7fb12b20c075
title: Abrufen und Ändern von Dateiattributen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c980ddd6390f016b2057392f42f6bf645859307
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356960"
---
# <a name="retrieving-and-changing-file-attributes"></a>Abrufen und Ändern von Dateiattributen

Eine Anwendung kann die Dateiattribute mithilfe der [**getfileattribute**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) -Funktion oder der [**getfileattributesex**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) -Funktion abrufen. Die Funktionen "Funktion [**" und "**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) [**setfileattribute**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) " können viele Attribute festlegen. Allerdings können Anwendungen nicht alle Attribute festlegen.

Das Codebeispiel in diesem Thema verwendet die [**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile) -Funktion, um alle Textdateien (txt-Dateien) im aktuellen Verzeichnis in ein neues Verzeichnis mit schreibgeschützten Dateien zu kopieren. Dateien im neuen Verzeichnis werden bei Bedarf in schreibgeschützt geändert.

Die Anwendung erstellt das Verzeichnis, das als Parameter angegeben wird, mithilfe der Funktion " [**kreatedirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) ". Das Verzeichnis darf nicht bereits vorhanden sein.

Die Anwendung durchsucht das aktuelle Verzeichnis nach allen Textdateien mithilfe der Funktionen " [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) " und " [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) ". Jede Textdatei wird in das \\ textro-Verzeichnis kopiert. Nachdem eine Datei kopiert wurde, wird von der [**getfileattribute**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) -Funktion bestimmt, ob eine Datei schreibgeschützt ist. Wenn die Datei nicht schreibgeschützt ist, ändert die Anwendung die Verzeichnisse in \\ textro und konvertiert die kopierte Datei mithilfe der [**setfileattributorfunktion**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) in schreibgeschützt.

Nachdem alle Textdateien im aktuellen Verzeichnis kopiert wurden, schließt die Anwendung das Such Handle mithilfe der [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) -Funktion.


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>
#include <strsafe.h>

void _tmain(int argc, TCHAR* argv[])
{
   WIN32_FIND_DATA FileData;
   HANDLE          hSearch;
   DWORD           dwAttrs;
   TCHAR           szNewPath[MAX_PATH];   
 
   BOOL            fFinished = FALSE; 

   if(argc != 2)
   {
      _tprintf(TEXT("Usage: %s <dir>\n"), argv[0]);
      return;
   }
 
// Create a new directory. 
 
   if (!CreateDirectory(argv[1], NULL)) 
   { 
      printf("CreateDirectory failed (%d)\n", GetLastError()); 
      return;
   } 
 
// Start searching for text files in the current directory. 
 
   hSearch = FindFirstFile(TEXT("*.txt"), &FileData); 
   if (hSearch == INVALID_HANDLE_VALUE) 
   { 
      printf("No text files found.\n"); 
      return;
   } 
 
// Copy each .TXT file to the new directory 
// and change it to read only, if not already. 
 
   while (!fFinished) 
   { 
      StringCchPrintf(szNewPath, sizeof(szNewPath)/sizeof(szNewPath[0]), TEXT("%s\\%s"), argv[1], FileData.cFileName);

      if (CopyFile(FileData.cFileName, szNewPath, FALSE))
      { 
         dwAttrs = GetFileAttributes(FileData.cFileName); 
         if (dwAttrs==INVALID_FILE_ATTRIBUTES) return; 

         if (!(dwAttrs & FILE_ATTRIBUTE_READONLY)) 
         { 
            SetFileAttributes(szNewPath, 
                dwAttrs | FILE_ATTRIBUTE_READONLY); 
         } 
      } 
      else 
      { 
         printf("Could not copy file.\n"); 
         return;
      } 
 
      if (!FindNextFile(hSearch, &FileData)) 
      {
         if (GetLastError() == ERROR_NO_MORE_FILES) 
         { 
            _tprintf(TEXT("Copied *.txt to %s\n"), argv[1]); 
            fFinished = TRUE; 
         } 
         else 
         { 
            printf("Could not find next file.\n"); 
            return;
         } 
      }
   } 
 
// Close the search handle. 
 
   FindClose(hSearch);
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Datei Attribut Konstanten**](file-attribute-constants.md)
</dt> <dt>

[Dateinamen, Pfade und Namespaces](naming-a-file.md)
</dt> </dl>

 

 



