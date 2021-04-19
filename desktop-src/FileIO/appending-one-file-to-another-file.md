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
# <a name="appending-one-file-to-another-file"></a><span data-ttu-id="d3b44-103">Anhängen einer Datei an eine andere Datei</span><span class="sxs-lookup"><span data-stu-id="d3b44-103">Appending One File to Another File</span></span>

<span data-ttu-id="d3b44-104">Das Codebeispiel in diesem Thema veranschaulicht das Öffnen und Schließen von Dateien, das Lesen und Schreiben in Dateien sowie das Sperren und Entsperren von Dateien.</span><span class="sxs-lookup"><span data-stu-id="d3b44-104">The code example in this topic shows you how to open and close files, read and write to files, and lock and unlock files.</span></span>

<span data-ttu-id="d3b44-105">Im Beispiel fügt die Anwendung eine Datei an das Ende einer anderen Datei an.</span><span class="sxs-lookup"><span data-stu-id="d3b44-105">In the example, the application appends one file to the end of another file.</span></span> <span data-ttu-id="d3b44-106">Zuerst öffnet die Anwendung die Datei, die mit Berechtigungen versehen wird, die nur der Anwendung das Schreiben erlauben.</span><span class="sxs-lookup"><span data-stu-id="d3b44-106">First, the application opens the file being appended with permissions that allow only the application to write to it.</span></span> <span data-ttu-id="d3b44-107">Während des Anfüge Vorgangs können andere Prozesse die Datei jedoch mit einer schreibgeschützten Berechtigung Öffnen, die eine Momentaufnahme Ansicht der angefügten Datei bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="d3b44-107">However, during the append process other processes can open the file with read-only permission, which provides a snapshot view of the file being appended.</span></span> <span data-ttu-id="d3b44-108">Anschließend wird die Datei während des eigentlichen Anfüge Vorgangs gesperrt, um die Integrität der Daten sicherzustellen, die in die Datei geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="d3b44-108">Then, the file is locked during the actual append process to ensure the integrity of the data being written to the file.</span></span>

<span data-ttu-id="d3b44-109">In diesem Beispiel werden keine Transaktionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="d3b44-109">This example does not use transactions.</span></span> <span data-ttu-id="d3b44-110">Wenn Sie transaktive Vorgänge verwendet haben, können Sie nur schreibgeschützten Zugriff haben.</span><span class="sxs-lookup"><span data-stu-id="d3b44-110">If you were using transacted operations, you would only be able have read-only access.</span></span> <span data-ttu-id="d3b44-111">In diesem Fall werden nur die angefügten Daten angezeigt, nachdem der Transaktionscommit-Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="d3b44-111">In this case, you would only see the appended data after the transaction commit operation completed.</span></span>

<span data-ttu-id="d3b44-112">Das Beispiel zeigt auch, dass die Anwendung zwei Dateien mithilfe von "- [**Datei**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)" ("") "</span><span class="sxs-lookup"><span data-stu-id="d3b44-112">The example also shows that the application opens two files by using [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea):</span></span>

-   <span data-ttu-id="d3b44-113">One.txt zum Lesen geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="d3b44-113">One.txt is opened for reading.</span></span>
-   <span data-ttu-id="d3b44-114">Two.txt ist zum Schreiben und zum gemeinsamen Lesen geöffnet.</span><span class="sxs-lookup"><span data-stu-id="d3b44-114">Two.txt is opened for writing and shared reading.</span></span>

<span data-ttu-id="d3b44-115">Dann verwendet die Anwendung [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) und [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) , um den Inhalt von One.txt am Ende der Two.txt anzufügen, indem Sie die 4-KB-Blöcke liest und schreibt.</span><span class="sxs-lookup"><span data-stu-id="d3b44-115">Then the application uses [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) and [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) to append the contents of One.txt to the end of Two.txt by reading and writing the 4 KB blocks.</span></span> <span data-ttu-id="d3b44-116">Vor dem Schreiben in die zweite Datei verwendet die Anwendung jedoch [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) , um den Zeiger der zweiten Datei auf das Ende dieser Datei festzulegen, und verwendet [**lockfile**](/windows/desktop/api/FileAPI/nf-fileapi-lockfile) , um den zu schreibenden Bereich zu sperren.</span><span class="sxs-lookup"><span data-stu-id="d3b44-116">However, before writing to the second file, the application uses [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) to set the pointer of the second file to the end of that file, and uses [**LockFile**](/windows/desktop/api/FileAPI/nf-fileapi-lockfile) to lock the area to be written.</span></span> <span data-ttu-id="d3b44-117">Dadurch wird verhindert, dass ein anderer Thread oder Prozess mit einem doppelten Handle auf den Bereich zugreift, während der Schreibvorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d3b44-117">This prevents another thread or process with a duplicate handle from accessing the area while the write operation is in progress.</span></span> <span data-ttu-id="d3b44-118">Wenn jeder Schreibvorgang beendet ist, wird [**unlockfile**](/windows/desktop/api/FileAPI/nf-fileapi-unlockfile) verwendet, um den gesperrten Bereich zu entsperren.</span><span class="sxs-lookup"><span data-stu-id="d3b44-118">When each write operation is complete, [**UnlockFile**](/windows/desktop/api/FileAPI/nf-fileapi-unlockfile) is used to unlock the locked area.</span></span>


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



 

 



