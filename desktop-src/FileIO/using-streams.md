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
# <a name="using-streams"></a>Verwenden von Streams

Das Beispiel in diesem Thema veranschaulicht die Verwendung grundlegender NTFS-Dateisystem Datenströme.

In diesem Beispiel wird eine Datei namens "TESTFILE" mit einer Größe von 16 Bytes erstellt. Die Datei verfügt jedoch auch über einen zusätzlichen:: $Data Streamtyp mit dem Namen "Stream", der weitere 23 Bytes hinzufügt, die nicht vom Betriebssystem gemeldet werden. Wenn Sie die Dateigrößen Eigenschaft für die Datei anzeigen, wird daher nur die Größe von Default:: $Data Stream für die Datei angezeigt.


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



Wenn Sie den **Typ TestFile** an einer Eingabeaufforderung eingeben, wird die folgende Ausgabe angezeigt:

``` syntax
This is TestFile
```

Wenn Sie jedoch die Wörter **Type TestFile: Stream** eingeben, wird der folgende Fehler generiert:

"Die Syntax für den Dateinamen, den Verzeichnisnamen oder die Volumebezeichnung ist falsch."

Verwenden Sie einen der folgenden Befehle, um anzuzeigen, was sich im TestFile: Stream befindet:

**Weitere < TestFile: Stream**

**Weitere < TestFile: Stream: $Data**

Der angezeigte Text lautet wie folgt:

``` syntax
This is TestFile:Stream
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Dateistreams](file-streams.md)
</dt> </dl>

 

 



