---
description: Beispielcode, der zeigt, wie grundlegende NTFS-Dateisystemstreams verwendet werden.
ms.assetid: 9cd5f418-404c-40f5-aa51-ef4d2a5f238e
title: Verwenden von Streams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23ebb6e2297c82e8643eb79ce66991b32fdf27e46fc723113a2866c79b2f8377
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078390"
---
# <a name="using-streams"></a>Verwenden von Streams

Das Beispiel in diesem Thema veranschaulicht die Verwendung grundlegender NTFS-Dateisystemstreams.

In diesem Beispiel wird eine Datei namens "TestFile" mit einer Größe von 16 Bytes erstellt. Die Datei verfügt jedoch auch über einen zusätzlichen ::$DATA Streamtyp namens "Stream", der zusätzliche 23 Bytes hinzufügt, die nicht vom Betriebssystem gemeldet werden. Wenn Sie die Dateigrößeneigenschaft für die Datei anzeigen, wird daher nur die Größe des Standardstreams ::$DATA für die Datei angezeigt.


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



Wenn Sie **TestFile** eingeben an einer Eingabeaufforderung eingeben, wird die folgende Ausgabe angezeigt:

``` syntax
This is TestFile
```

Wenn Sie jedoch die Wörter **TestFile:Stream** eingeben, wird der folgende Fehler generiert:

"Die Syntax für Dateiname, Verzeichnisname oder Volumebezeichnung ist falsch."

Verwenden Sie einen der folgenden Befehle, um anzuzeigen, was sich in TestFile:stream befindet:

**Weitere < TestFile:Stream**

**Weitere < TestFile:Stream:$DATA**

Der angezeigte Text sieht wie folgt aus:

``` syntax
This is TestFile:Stream
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Datei-Streams](file-streams.md)
</dt> </dl>

 

 



