---
description: Beispielcode, der zeigt, wie eine Anwendung eine Datei am Ende einer anderen Datei anfügen kann, einschließlich der Vorgehensweise zum Öffnen und Schließen von Dateien, lesen und Schreiben in Dateien und Sperren und Entsperren von Dateien.
ms.assetid: e4d1f842-16a1-47e4-84b4-9bb44aaa1dc5
title: Anhängen einer Datei an eine andere Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 546d24fe88a2bbf22c190a0caca3b3f98e753720
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356195"
---
# <a name="appending-one-file-to-another-file"></a>Anhängen einer Datei an eine andere Datei

Das Codebeispiel in diesem Thema veranschaulicht das Öffnen und Schließen von Dateien, das Lesen und Schreiben in Dateien sowie das Sperren und Entsperren von Dateien.

Im Beispiel fügt die Anwendung eine Datei an das Ende einer anderen Datei an. Zuerst öffnet die Anwendung die Datei, die mit Berechtigungen versehen wird, die nur der Anwendung das Schreiben erlauben. Während des Anfüge Vorgangs können andere Prozesse die Datei jedoch mit einer schreibgeschützten Berechtigung Öffnen, die eine Momentaufnahme Ansicht der angefügten Datei bereitstellt. Anschließend wird die Datei während des eigentlichen Anfüge Vorgangs gesperrt, um die Integrität der Daten sicherzustellen, die in die Datei geschrieben werden.

In diesem Beispiel werden keine Transaktionen verwendet. Wenn Sie transaktive Vorgänge verwendet haben, können Sie nur schreibgeschützten Zugriff haben. In diesem Fall werden nur die angefügten Daten angezeigt, nachdem der Transaktionscommit-Vorgang abgeschlossen wurde.

Das Beispiel zeigt auch, dass die Anwendung zwei Dateien mithilfe von "- [**Datei**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)" ("") "

-   One.txt zum Lesen geöffnet ist.
-   Two.txt ist zum Schreiben und zum gemeinsamen Lesen geöffnet.

Dann verwendet die Anwendung [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) und [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) , um den Inhalt von One.txt am Ende der Two.txt anzufügen, indem Sie die 4-KB-Blöcke liest und schreibt. Vor dem Schreiben in die zweite Datei verwendet die Anwendung jedoch [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) , um den Zeiger der zweiten Datei auf das Ende dieser Datei festzulegen, und verwendet [**lockfile**](/windows/desktop/api/FileAPI/nf-fileapi-lockfile) , um den zu schreibenden Bereich zu sperren. Dadurch wird verhindert, dass ein anderer Thread oder Prozess mit einem doppelten Handle auf den Bereich zugreift, während der Schreibvorgang ausgeführt wird. Wenn jeder Schreibvorgang beendet ist, wird [**unlockfile**](/windows/desktop/api/FileAPI/nf-fileapi-unlockfile) verwendet, um den gesperrten Bereich zu entsperren.


```C++
#include <windows.h>
#include <stdio.h>

void main()
{
  HANDLE hFile;
  HANDLE hAppend;
  DWORD  dwBytesRead, dwBytesWritten, dwPos;
  BYTE   buff[4096];

  // Open the existing file.

  hFile = CreateFile(TEXT("one.txt"), // open One.txt
            GENERIC_READ,             // open for reading
            0,                        // do not share
            NULL,                     // no security
            OPEN_EXISTING,            // existing file only
            FILE_ATTRIBUTE_NORMAL,    // normal file
            NULL);                    // no attr. template

  if (hFile == INVALID_HANDLE_VALUE)
  {
     printf("Could not open One.txt."); 
     return;
  }

  // Open the existing file, or if the file does not exist,
  // create a new file.

  hAppend = CreateFile(TEXT("two.txt"), // open Two.txt
              FILE_APPEND_DATA,         // open for writing
              FILE_SHARE_READ,          // allow multiple readers
              NULL,                     // no security
              OPEN_ALWAYS,              // open or create
              FILE_ATTRIBUTE_NORMAL,    // normal file
              NULL);                    // no attr. template

  if (hAppend == INVALID_HANDLE_VALUE)
  {
     printf("Could not open Two.txt."); 
     return;
  }

  // Append the first file to the end of the second file.
  // Lock the second file to prevent another process from
  // accessing it while writing to it. Unlock the
  // file when writing is complete.

  while (ReadFile(hFile, buff, sizeof(buff), &dwBytesRead, NULL)
      && dwBytesRead > 0)
    {
    dwPos = SetFilePointer(hAppend, 0, NULL, FILE_END);
    LockFile(hAppend, dwPos, 0, dwBytesRead, 0);
    WriteFile(hAppend, buff, dwBytesRead, &dwBytesWritten, NULL);
    UnlockFile(hAppend, dwPos, 0, dwBytesRead, 0);
    }

  // Close both files.

  CloseHandle(hFile);
  CloseHandle(hAppend);
}
```



 

 



