---
description: Beispielcode, der zeigt, wie eine Anwendung eine Datei an das Ende einer anderen Datei anfügen kann, einschließlich des Öffnens und Schließens von Dateien, Lesen und Schreiben in Dateien sowie Sperren und Entsperren von Dateien.
ms.assetid: e4d1f842-16a1-47e4-84b4-9bb44aaa1dc5
title: Anfügen einer Datei an eine andere Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 585521c1d0bb85c41806ba83c2c0940dc3523035731279d4da3f06af45334984
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766227"
---
# <a name="appending-one-file-to-another-file"></a>Anfügen einer Datei an eine andere Datei

Im Codebeispiel in diesem Thema wird gezeigt, wie Sie Dateien öffnen und schließen, In Dateien lesen und schreiben sowie Dateien sperren und entsperren.

Im Beispiel fügt die Anwendung eine Datei an das Ende einer anderen Datei an. Zunächst öffnet die Anwendung die Datei, die mit Berechtigungen angefügt wird, die es nur der Anwendung ermöglichen, in sie zu schreiben. Während des Anfügevorgangs können andere Prozesse die Datei jedoch mit schreibgeschützter Berechtigung öffnen, die eine Momentaufnahmeansicht der anzufügenden Datei bereitstellt. Anschließend wird die Datei während des eigentlichen Anfügevorgangs gesperrt, um die Integrität der Daten sicherzustellen, die in die Datei geschrieben werden.

In diesem Beispiel werden keine Transaktionen verwendet. Wenn Sie transaktive Vorgänge verwenden, verfügen Sie nur über schreibgeschützten Zugriff. In diesem Fall werden die angefügten Daten erst angezeigt, nachdem der Transaktionscommitvorgang abgeschlossen wurde.

Das Beispiel zeigt auch, dass die Anwendung mit [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)zwei Dateien öffnet:

-   One.txt wird zum Lesen geöffnet.
-   Two.txt wird zum Schreiben und zum gemeinsamen Lesen geöffnet.

Anschließend verwendet die Anwendung [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) und [**WriteFile,**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) um den Inhalt von One.txt durch Lesen und Schreiben der 4-KB-Blöcke an das Ende Two.txt anzufügen. Vor dem Schreiben in die zweite Datei verwendet die Anwendung [**jedoch SetFilePointer,**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) um den Zeiger der zweiten Datei auf das Ende dieser Datei festzulegen, und [**verwendet LockFile,**](/windows/desktop/api/FileAPI/nf-fileapi-lockfile) um den zu schreibenden Bereich zu sperren. Dadurch wird verhindert, dass ein anderer Thread oder Prozess mit einem doppelten Handle auf den Bereich zugreift, während der Schreibvorgang ausgeführt wird. Wenn jeder Schreibvorgang abgeschlossen ist, wird [**UnlockFile**](/windows/desktop/api/FileAPI/nf-fileapi-unlockfile) verwendet, um den gesperrten Bereich zu entsperren.


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



 

 



