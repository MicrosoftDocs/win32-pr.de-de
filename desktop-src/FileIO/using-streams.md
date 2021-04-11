---
description: Beispielcode, der zeigt, wie grundlegende NTFS-Dateisystem Datenströme verwendet werden.
ms.assetid: 9cd5f418-404c-40f5-aa51-ef4d2a5f238e
title: Verwenden von Streams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04edc73a3524d45eeead4cd6c0d508925e6caa5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217368"
---
# <a name="using-streams"></a><span data-ttu-id="d4d1d-103">Verwenden von Streams</span><span class="sxs-lookup"><span data-stu-id="d4d1d-103">Using Streams</span></span>

<span data-ttu-id="d4d1d-104">Das Beispiel in diesem Thema veranschaulicht die Verwendung grundlegender NTFS-Dateisystem Datenströme.</span><span class="sxs-lookup"><span data-stu-id="d4d1d-104">The example in this topic demonstrates how to use basic NTFS file system streams.</span></span>

<span data-ttu-id="d4d1d-105">In diesem Beispiel wird eine Datei namens "TESTFILE" mit einer Größe von 16 Bytes erstellt.</span><span class="sxs-lookup"><span data-stu-id="d4d1d-105">This example creates a file, called "TestFile," with a size of 16 bytes.</span></span> <span data-ttu-id="d4d1d-106">Die Datei verfügt jedoch auch über einen zusätzlichen:: $Data Streamtyp mit dem Namen "Stream", der weitere 23 Bytes hinzufügt, die nicht vom Betriebssystem gemeldet werden.</span><span class="sxs-lookup"><span data-stu-id="d4d1d-106">However, the file also has an additional ::$DATA stream type, named "Stream" which adds an additional 23 bytes that is not reported by the operating system.</span></span> <span data-ttu-id="d4d1d-107">Wenn Sie die Dateigrößen Eigenschaft für die Datei anzeigen, wird daher nur die Größe von Default:: $Data Stream für die Datei angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d4d1d-107">Therefore, when you view the file size property for the file, you see only the size of default ::$DATA stream for the file.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

void main( )
 {
  HANDLE hFile, hStream;
  DWORD dwRet;

  hFile = CreateFile( TEXT("TestFile"), // Filename
                      GENERIC_WRITE,    // Desired access
                      FILE_SHARE_WRITE, // Share flags
                      NULL,             // Security Attributes
                      OPEN_ALWAYS,      // Creation Disposition
                      0,                // Flags and Attributes
                      NULL );           // OVERLAPPED pointer
  if( hFile == INVALID_HANDLE_VALUE )
   {
    printf( "Cannot open TestFile\n" );
    return;
   }
  else
   {
    WriteFile( hFile,              // Handle
               "This is TestFile", // Data to be written
               16,                 // Size of data, in bytes
               &dwRet,             // Number of bytes written
               NULL );             // OVERLAPPED pointer
    CloseHandle( hFile );
    hFile = INVALID_HANDLE_VALUE;
   }

  hStream = CreateFile( TEXT("TestFile:Stream"), // Filename
                        GENERIC_WRITE,           // Desired access
                        FILE_SHARE_WRITE,        // Share flags
                        NULL,                    // Security Attributes
                        OPEN_ALWAYS,             // Creation Disposition
                        0,                       // Flags and Attributes
                        NULL );                  // OVERLAPPED pointer
  if( hStream == INVALID_HANDLE_VALUE )
    printf( "Cannot open TestFile:Stream\n" );
  else
   {
    WriteFile( hStream,                   // Handle
               "This is TestFile:Stream", // Data to be written
               23,                        // Size of data
               &dwRet,                    // Number of bytes written
               NULL);                     // OVERLAPPED pointer
    CloseHandle( hStream );
    hStream = INVALID_HANDLE_VALUE;
   }
}
```



<span data-ttu-id="d4d1d-108">Wenn Sie den **Typ TestFile** an einer Eingabeaufforderung eingeben, wird die folgende Ausgabe angezeigt:</span><span class="sxs-lookup"><span data-stu-id="d4d1d-108">If you type **Type TestFile** at a command prompt, it displays the following output:</span></span>

``` syntax
This is TestFile
```

<span data-ttu-id="d4d1d-109">Wenn Sie jedoch die Wörter **Type TestFile: Stream** eingeben, wird der folgende Fehler generiert:</span><span class="sxs-lookup"><span data-stu-id="d4d1d-109">However, if you type the words **Type TestFile:Stream**, it generates the following error:</span></span>

<span data-ttu-id="d4d1d-110">"Die Syntax für den Dateinamen, den Verzeichnisnamen oder die Volumebezeichnung ist falsch."</span><span class="sxs-lookup"><span data-stu-id="d4d1d-110">"The filename, directory name, or volume label syntax is incorrect."</span></span>

<span data-ttu-id="d4d1d-111">Verwenden Sie einen der folgenden Befehle, um anzuzeigen, was sich im TestFile: Stream befindet:</span><span class="sxs-lookup"><span data-stu-id="d4d1d-111">To view what is in TestFile:stream, use one of the following commands:</span></span>

<span data-ttu-id="d4d1d-112">**Weitere < TestFile: Stream**</span><span class="sxs-lookup"><span data-stu-id="d4d1d-112">**More < TestFile:Stream**</span></span>

<span data-ttu-id="d4d1d-113">**Weitere < TestFile: Stream: $Data**</span><span class="sxs-lookup"><span data-stu-id="d4d1d-113">**More < TestFile:Stream:$DATA**</span></span>

<span data-ttu-id="d4d1d-114">Der angezeigte Text lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d4d1d-114">The text displayed is as follows:</span></span>

``` syntax
This is TestFile:Stream
```

## <a name="related-topics"></a><span data-ttu-id="d4d1d-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d4d1d-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4d1d-116">Dateistreams</span><span class="sxs-lookup"><span data-stu-id="d4d1d-116">File Streams</span></span>](file-streams.md)
</dt> </dl>

 

 



