---
description: Wenn Sie einen Teil der Datei anzeigen möchten, der nicht am Anfang der Datei beginnt, müssen Sie ein Datei Zuordnungsobjekt erstellen.
ms.assetid: e47a0e79-3000-479b-afba-dcd36210ea3d
title: Erstellen einer Ansicht in einer Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9425a1c491a5c7d8ae7861d53418ee0f349bf212
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862435"
---
# <a name="creating-a-view-within-a-file"></a>Erstellen einer Ansicht in einer Datei

Wenn Sie einen Teil der Datei anzeigen möchten, der nicht am Anfang der Datei beginnt, müssen Sie ein Datei Zuordnungsobjekt erstellen. Bei diesem Objekt handelt es sich um die Größe des Teils der Datei, die Sie anzeigen möchten, sowie um den Offset in der Datei. Wenn Sie z. b. das 1 KB (1 k), das 131.072 bytes (128 KB) beginnt, in der Datei anzeigen möchten, müssen Sie ein Datei Zuordnungsobjekt mit einer Größe von mindestens 132.096 Byte (129k) erstellen. In der Ansicht werden 131.072 bytes (128 KB) in der Datei gestartet und mindestens 1.024 Bytes erweitert. In diesem Beispiel wird davon ausgegangen, dass die Granularität der Datei Zuordnung 64 KB beträgt.

Die Granularität der Datei Zuordnung wirkt sich auf das Starten einer Kartenansicht aus. Eine Kartenansicht muss bei einem Offset in der Datei beginnen, bei der es sich um ein Vielfaches der Datei Zuordnungs Granularität handelt. Die Daten, die Sie anzeigen möchten, sind möglicherweise die Dateioffset Modulo der Zuordnungs Granularität in der Ansicht. Die Größe der Sicht ist der Offset des Daten Modulo der Zuordnungs Granularität, zuzüglich der Größe der Daten, die Sie untersuchen möchten.

Nehmen wir beispielsweise an, dass die [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) -Funktion eine Zuordnungs Granularität von 64K angibt. Gehen Sie folgendermaßen vor, um 1 KB von Daten mit einer Größe von 138.240 bytes (135 KB) in der Datei zu überprüfen:

1.  Erstellen Sie ein Datei Zuordnung-Objekt mit einer Größe von mindestens 139.264 bytes (136 KB).
2.  Erstellen Sie eine Dateiansicht, die bei einem Dateioffset beginnt, bei dem es sich um das größte Vielfache der Datei Zuordnungs Granularität handelt, das geringer ist als der erforderliche Offset. In diesem Fall beginnt die Dateiansicht bei Offset 131.072 (128 KB) in der Datei. Die Sicht beträgt 139264 bytes (136 KB) minus 131.072 Byte (128 KB) oder 8.192 Byte (8K), Größe.
3.  Erstellen Sie einen Zeiger Offset 7K in der Ansicht, um auf das 1K zuzugreifen, für das Sie sich interessieren.

Wenn die Daten, die Sie mit einer granularitätsgrenze für die Datei Zuordnung überschreiten möchten, können Sie die Sicht auf die Granularität der Datei Zuordnung vergrößern. Dadurch wird vermieden, dass die Daten in Teile zerlegt werden.

Das folgende Programm veranschaulicht das zweite obige Beispiel.


```C++
/*
   This program demonstrates file mapping, especially how to align a
   view with the system file allocation granularity.
*/

#include <windows.h>
#include <stdio.h>
#include <tchar.h>

#define BUFFSIZE 1024 // size of the memory to examine at any one time

#define FILE_MAP_START 138240 // starting point within the file of
                              // the data to examine (135K)

/* The test file. The code below creates the file and populates it,
   so there is no need to supply it in advance. */

TCHAR * lpcTheFile = TEXT("fmtest.txt"); // the file to be manipulated

int main(void)
{
  HANDLE hMapFile;      // handle for the file's memory-mapped region
  HANDLE hFile;         // the file handle
  BOOL bFlag;           // a result holder
  DWORD dBytesWritten;  // number of bytes written
  DWORD dwFileSize;     // temporary storage for file sizes
  DWORD dwFileMapSize;  // size of the file mapping
  DWORD dwMapViewSize;  // the size of the view
  DWORD dwFileMapStart; // where to start the file map view
  DWORD dwSysGran;      // system allocation granularity
  SYSTEM_INFO SysInfo;  // system information; used to get granularity
  LPVOID lpMapAddress;  // pointer to the base address of the
                        // memory-mapped region
  char * pData;         // pointer to the data
  int i;                // loop counter
  int iData;            // on success contains the first int of data
  int iViewDelta;       // the offset into the view where the data
                        //shows up

  // Create the test file. Open it "Create Always" to overwrite any
  // existing file. The data is re-created below
  hFile = CreateFile(lpcTheFile,
                     GENERIC_READ | GENERIC_WRITE,
                     0,
                     NULL,
                     CREATE_ALWAYS,
                     FILE_ATTRIBUTE_NORMAL,
                     NULL);

  if (hFile == INVALID_HANDLE_VALUE)
  {
    _tprintf(TEXT("hFile is NULL\n"));
    _tprintf(TEXT("Target file is %s\n"),
             lpcTheFile);
    return 4;
  }

  // Get the system allocation granularity.
  GetSystemInfo(&SysInfo);
  dwSysGran = SysInfo.dwAllocationGranularity;

  // Now calculate a few variables. Calculate the file offsets as
  // 64-bit values, and then get the low-order 32 bits for the
  // function calls.

  // To calculate where to start the file mapping, round down the
  // offset of the data into the file to the nearest multiple of the
  // system allocation granularity.
  dwFileMapStart = (FILE_MAP_START / dwSysGran) * dwSysGran;
  _tprintf (TEXT("The file map view starts at %ld bytes into the file.\n"),
          dwFileMapStart);

  // Calculate the size of the file mapping view.
  dwMapViewSize = (FILE_MAP_START % dwSysGran) + BUFFSIZE;
  _tprintf (TEXT("The file map view is %ld bytes large.\n"),
            dwMapViewSize);

  // How large will the file mapping object be?
  dwFileMapSize = FILE_MAP_START + BUFFSIZE;
  _tprintf (TEXT("The file mapping object is %ld bytes large.\n"),
          dwFileMapSize);

  // The data of interest isn't at the beginning of the
  // view, so determine how far into the view to set the pointer.
  iViewDelta = FILE_MAP_START - dwFileMapStart;
  _tprintf (TEXT("The data is %d bytes into the view.\n"),
            iViewDelta);

  // Now write a file with data suitable for experimentation. This
  // provides unique int (4-byte) offsets in the file for easy visual
  // inspection. Note that this code does not check for storage
  // medium overflow or other errors, which production code should
  // do. Because an int is 4 bytes, the value at the pointer to the
  // data should be one quarter of the desired offset into the file

  for (i=0; i<(int)dwSysGran; i++)
  {
    WriteFile (hFile, &i, sizeof (i), &dBytesWritten, NULL);
  }

  // Verify that the correct file size was written.
  dwFileSize = GetFileSize(hFile,  NULL);
  _tprintf(TEXT("hFile size: %10d\n"), dwFileSize);

  // Create a file mapping object for the file
  // Note that it is a good idea to ensure the file size is not zero
  hMapFile = CreateFileMapping( hFile,          // current file handle
                NULL,           // default security
                PAGE_READWRITE, // read/write permission
                0,              // size of mapping object, high
                dwFileMapSize,  // size of mapping object, low
                NULL);          // name of mapping object

  if (hMapFile == NULL)
  {
    _tprintf(TEXT("hMapFile is NULL: last error: %d\n"), GetLastError() );
    return (2);
  }

  // Map the view and test the results.

  lpMapAddress = MapViewOfFile(hMapFile,            // handle to
                                                    // mapping object
                               FILE_MAP_ALL_ACCESS, // read/write
                               0,                   // high-order 32
                                                    // bits of file
                                                    // offset
                               dwFileMapStart,      // low-order 32
                                                    // bits of file
                                                    // offset
                               dwMapViewSize);      // number of bytes
                                                    // to map
  if (lpMapAddress == NULL)
  {
    _tprintf(TEXT("lpMapAddress is NULL: last error: %d\n"), GetLastError());
    return 3;
  }

  // Calculate the pointer to the data.
  pData = (char *) lpMapAddress + iViewDelta;

  // Extract the data, an int. Cast the pointer pData from a "pointer
  // to char" to a "pointer to int" to get the whole thing
  iData = *(int *)pData;

  _tprintf (TEXT("The value at the pointer is %d,\nwhich %s one quarter of the desired file offset.\n"),
            iData,
            iData*4 == FILE_MAP_START ? TEXT("is") : TEXT("is not"));

  // Close the file mapping object and the open file

  bFlag = UnmapViewOfFile(lpMapAddress);
  bFlag = CloseHandle(hMapFile); // close the file mapping object

  if(!bFlag)
  {
    _tprintf(TEXT("\nError %ld occurred closing the mapping object!"),
             GetLastError());
  }

  bFlag = CloseHandle(hFile);   // close the file itself

  if(!bFlag)
  {
    _tprintf(TEXT("\nError %ld occurred closing the file!"),
           GetLastError());
  }

  return 0;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer Dateiansicht](creating-a-file-view.md)
</dt> </dl>

 

 
