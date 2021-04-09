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
# <a name="creating-a-view-within-a-file"></a><span data-ttu-id="da738-103">Erstellen einer Ansicht in einer Datei</span><span class="sxs-lookup"><span data-stu-id="da738-103">Creating a View Within a File</span></span>

<span data-ttu-id="da738-104">Wenn Sie einen Teil der Datei anzeigen möchten, der nicht am Anfang der Datei beginnt, müssen Sie ein Datei Zuordnungsobjekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="da738-104">If you want to view a portion of the file that does not start at the beginning of the file, you must create a file mapping object.</span></span> <span data-ttu-id="da738-105">Bei diesem Objekt handelt es sich um die Größe des Teils der Datei, die Sie anzeigen möchten, sowie um den Offset in der Datei.</span><span class="sxs-lookup"><span data-stu-id="da738-105">This object is the size of the portion of the file you want to view plus the offset into the file.</span></span> <span data-ttu-id="da738-106">Wenn Sie z. b. das 1 KB (1 k), das 131.072 bytes (128 KB) beginnt, in der Datei anzeigen möchten, müssen Sie ein Datei Zuordnungsobjekt mit einer Größe von mindestens 132.096 Byte (129k) erstellen.</span><span class="sxs-lookup"><span data-stu-id="da738-106">For example, if you want to view the 1 kilobyte (1K) that begins 131,072 bytes (128K) into the file, you must create a file mapping object of at least 132,096 bytes (129K) in size.</span></span> <span data-ttu-id="da738-107">In der Ansicht werden 131.072 bytes (128 KB) in der Datei gestartet und mindestens 1.024 Bytes erweitert.</span><span class="sxs-lookup"><span data-stu-id="da738-107">The view starts 131,072 bytes (128K) into the file and extend for at least 1,024 bytes.</span></span> <span data-ttu-id="da738-108">In diesem Beispiel wird davon ausgegangen, dass die Granularität der Datei Zuordnung 64 KB beträgt.</span><span class="sxs-lookup"><span data-stu-id="da738-108">This example assumes a file allocation granularity of 64K.</span></span>

<span data-ttu-id="da738-109">Die Granularität der Datei Zuordnung wirkt sich auf das Starten einer Kartenansicht aus.</span><span class="sxs-lookup"><span data-stu-id="da738-109">File allocation granularity affects where a map view can start.</span></span> <span data-ttu-id="da738-110">Eine Kartenansicht muss bei einem Offset in der Datei beginnen, bei der es sich um ein Vielfaches der Datei Zuordnungs Granularität handelt.</span><span class="sxs-lookup"><span data-stu-id="da738-110">A map view must start at an offset into the file that is a multiple of the file allocation granularity.</span></span> <span data-ttu-id="da738-111">Die Daten, die Sie anzeigen möchten, sind möglicherweise die Dateioffset Modulo der Zuordnungs Granularität in der Ansicht.</span><span class="sxs-lookup"><span data-stu-id="da738-111">So the data you want to view may be the file offset modulo the allocation granularity into the view.</span></span> <span data-ttu-id="da738-112">Die Größe der Sicht ist der Offset des Daten Modulo der Zuordnungs Granularität, zuzüglich der Größe der Daten, die Sie untersuchen möchten.</span><span class="sxs-lookup"><span data-stu-id="da738-112">The size of the view is the offset of the data modulo the allocation granularity, plus the size of the data that you want to examine.</span></span>

<span data-ttu-id="da738-113">Nehmen wir beispielsweise an, dass die [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) -Funktion eine Zuordnungs Granularität von 64K angibt.</span><span class="sxs-lookup"><span data-stu-id="da738-113">For example, suppose that the [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) function indicates an allocation granularity of 64K.</span></span> <span data-ttu-id="da738-114">Gehen Sie folgendermaßen vor, um 1 KB von Daten mit einer Größe von 138.240 bytes (135 KB) in der Datei zu überprüfen:</span><span class="sxs-lookup"><span data-stu-id="da738-114">To examine 1K of data that is 138,240 bytes (135K) into the file, do the following:</span></span>

1.  <span data-ttu-id="da738-115">Erstellen Sie ein Datei Zuordnung-Objekt mit einer Größe von mindestens 139.264 bytes (136 KB).</span><span class="sxs-lookup"><span data-stu-id="da738-115">Create a file mapping object of at least 139,264 bytes (136K) in size.</span></span>
2.  <span data-ttu-id="da738-116">Erstellen Sie eine Dateiansicht, die bei einem Dateioffset beginnt, bei dem es sich um das größte Vielfache der Datei Zuordnungs Granularität handelt, das geringer ist als der erforderliche Offset.</span><span class="sxs-lookup"><span data-stu-id="da738-116">Create a file view that starts at a file offset that is the largest multiple of the file allocation granularity less than the offset you require.</span></span> <span data-ttu-id="da738-117">In diesem Fall beginnt die Dateiansicht bei Offset 131.072 (128 KB) in der Datei.</span><span class="sxs-lookup"><span data-stu-id="da738-117">In this case, the file view starts at offset 131,072 (128K) into the file.</span></span> <span data-ttu-id="da738-118">Die Sicht beträgt 139264 bytes (136 KB) minus 131.072 Byte (128 KB) oder 8.192 Byte (8K), Größe.</span><span class="sxs-lookup"><span data-stu-id="da738-118">The view is 139264 bytes (136K) minus 131,072 bytes (128K), or 8,192 bytes (8K), in size.</span></span>
3.  <span data-ttu-id="da738-119">Erstellen Sie einen Zeiger Offset 7K in der Ansicht, um auf das 1K zuzugreifen, für das Sie sich interessieren.</span><span class="sxs-lookup"><span data-stu-id="da738-119">Create a pointer offset 7K into the view to access the 1K in which you are interested.</span></span>

<span data-ttu-id="da738-120">Wenn die Daten, die Sie mit einer granularitätsgrenze für die Datei Zuordnung überschreiten möchten, können Sie die Sicht auf die Granularität der Datei Zuordnung vergrößern.</span><span class="sxs-lookup"><span data-stu-id="da738-120">If the data you want straddles a file allocation granularity boundary, you could make the view larger than the file allocation granularity.</span></span> <span data-ttu-id="da738-121">Dadurch wird vermieden, dass die Daten in Teile zerlegt werden.</span><span class="sxs-lookup"><span data-stu-id="da738-121">This avoids breaking the data into pieces.</span></span>

<span data-ttu-id="da738-122">Das folgende Programm veranschaulicht das zweite obige Beispiel.</span><span class="sxs-lookup"><span data-stu-id="da738-122">The following program illustrates the second example above.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="da738-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="da738-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da738-124">Erstellen einer Dateiansicht</span><span class="sxs-lookup"><span data-stu-id="da738-124">Creating a File View</span></span>](creating-a-file-view.md)
</dt> </dl>

 

 
