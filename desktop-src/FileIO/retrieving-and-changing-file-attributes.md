---
description: Beispielcode, der zeigt, wie die GetFileAttributesEx-Funktion zum Abrufen von Dateiattributen verwendet wird.
ms.assetid: f6eaea8a-0cc2-4fb6-bec5-7fb12b20c075
title: Abrufen und Ändern von Dateiattributen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d2609030d1657b78c266ed6b10841159e0df4d40a2e3b07b0fce42e98b45d54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015138"
---
# <a name="retrieving-and-changing-file-attributes"></a>Abrufen und Ändern von Dateiattributen

Eine Anwendung kann die Dateiattribute mithilfe der [**GetFileAttributes-**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) oder [**GetFileAttributesEx-Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) abrufen. Die Funktionen [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) und [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) können viele der Attribute festlegen. Anwendungen können jedoch nicht alle Attribute festlegen.

Im Codebeispiel in diesem Thema wird die [**CopyFile-Funktion**](/windows/desktop/api/WinBase/nf-winbase-copyfile) verwendet, um alle Textdateien (.txt) im aktuellen Verzeichnis in ein neues Verzeichnis schreibgeschützter Dateien zu kopieren. Dateien im neuen Verzeichnis werden bei Bedarf in schreibgeschützte Dateien geändert.

Die Anwendung erstellt das als Parameter angegebene Verzeichnis mithilfe der [**CreateDirectory-Funktion.**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) Das Verzeichnis darf nicht bereits vorhanden sein.

Die Anwendung durchsucht das aktuelle Verzeichnis mithilfe der Funktionen [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) und [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) nach allen Textdateien. Jede Textdatei wird in das \\ TextRO-Verzeichnis kopiert. Nachdem eine Datei kopiert wurde, bestimmt die [**GetFileAttributes-Funktion,**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) ob eine Datei schreibgeschützt ist. Wenn die Datei nicht schreibgeschützt ist, ändert die Anwendung die Verzeichnisse in \\ TextRO und konvertiert die kopierte Datei mithilfe der [**SetFileAttributes-Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) in schreibgeschützt.

Nachdem alle Textdateien im aktuellen Verzeichnis kopiert wurden, schließt die Anwendung das Suchhandle mithilfe der [**Funktion FindClose.**](/windows/desktop/api/FileAPI/nf-fileapi-findclose)


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

[**Dateiattributkonstanten**](file-attribute-constants.md)
</dt> <dt>

[Dateinamen, Pfade und Namespaces](naming-a-file.md)
</dt> </dl>

 

 



