---
description: GetFinalPathNameByHandle, eingeführt in Windows Vista und Windows Server 2008, gibt einen Pfad von einem Handle zurück.
ms.assetid: 359673bf-cc4c-4881-b946-ecdbef4a7ecb
title: Abrufen eines Dateinamens aus einem Dateihand handle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f905051fdc9c26d16c00f3f1acb2629ae06b8581abb5e5de50944a74e0c6b8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118386413"
---
# <a name="obtaining-a-file-name-from-a-file-handle"></a>Abrufen eines Dateinamens aus einem Dateihand handle

[**GetFinalPathNameByHandle**](/windows/win32/api/fileapi/nf-fileapi-getfinalpathnamebyhandlea), eingeführt in Windows Vista und Windows Server 2008, gibt einen Pfad von einem Handle zurück. Wenn Sie dies für frühere Releases von Windows tun müssen, wird im folgenden Beispiel mithilfe eines Dateizuordnungsobjekts ein Dateiname aus einem Handle für ein Dateiobjekt erhalten. Zum Erstellen der Zuordnung werden die Funktionen [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) und [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) verwendet. Als Nächstes wird die [**GetMappedFileName-Funktion**](/windows/win32/api/psapi/nf-psapi-getmappedfilenamea) verwendet, um den Dateinamen zu erhalten. Bei Remotedateien wird der von dieser Funktion empfangene Gerätepfad gedruckt. Bei lokalen Dateien wird der Pfad so konvertiert, dass ein Laufwerkbuchstaben verwendet wird, und dieser Pfad wird gedruckt. Um diesen Code zu  testen, erstellen Sie eine Main-Funktion, die mit [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) eine Datei öffnet und das resultierende Handle an `GetFileNameFromHandle` übergibt.


```C++
#include <windows.h>
#include <stdio.h>
#include <tchar.h>
#include <string.h>
#include <psapi.h>
#include <strsafe.h>

#define BUFSIZE 512

BOOL GetFileNameFromHandle(HANDLE hFile) 
{
  BOOL bSuccess = FALSE;
  TCHAR pszFilename[MAX_PATH+1];
  HANDLE hFileMap;

  // Get the file size.
  DWORD dwFileSizeHi = 0;
  DWORD dwFileSizeLo = GetFileSize(hFile, &dwFileSizeHi); 

  if( dwFileSizeLo == 0 && dwFileSizeHi == 0 )
  {
     _tprintf(TEXT("Cannot map a file with a length of zero.\n"));
     return FALSE;
  }

  // Create a file mapping object.
  hFileMap = CreateFileMapping(hFile, 
                    NULL, 
                    PAGE_READONLY,
                    0, 
                    1,
                    NULL);

  if (hFileMap) 
  {
    // Create a file mapping to get the file name.
    void* pMem = MapViewOfFile(hFileMap, FILE_MAP_READ, 0, 0, 1);

    if (pMem) 
    {
      if (GetMappedFileName (GetCurrentProcess(), 
                             pMem, 
                             pszFilename,
                             MAX_PATH)) 
      {

        // Translate path with device name to drive letters.
        TCHAR szTemp[BUFSIZE];
        szTemp[0] = '\0';

        if (GetLogicalDriveStrings(BUFSIZE-1, szTemp)) 
        {
          TCHAR szName[MAX_PATH];
          TCHAR szDrive[3] = TEXT(" :");
          BOOL bFound = FALSE;
          TCHAR* p = szTemp;

          do 
          {
            // Copy the drive letter to the template string
            *szDrive = *p;

            // Look up each device name
            if (QueryDosDevice(szDrive, szName, MAX_PATH))
            {
              size_t uNameLen = _tcslen(szName);

              if (uNameLen < MAX_PATH) 
              {
                bFound = _tcsnicmp(pszFilename, szName, uNameLen) == 0
                         && *(pszFilename + uNameLen) == _T('\\');

                if (bFound) 
                {
                  // Reconstruct pszFilename using szTempFile
                  // Replace device path with DOS path
                  TCHAR szTempFile[MAX_PATH];
                  StringCchPrintf(szTempFile,
                            MAX_PATH,
                            TEXT("%s%s"),
                            szDrive,
                            pszFilename+uNameLen);
                  StringCchCopyN(pszFilename, MAX_PATH+1, szTempFile, _tcslen(szTempFile));
                }
              }
            }

            // Go to the next NULL character.
            while (*p++);
          } while (!bFound && *p); // end of string
        }
      }
      bSuccess = TRUE;
      UnmapViewOfFile(pMem);
    } 

    CloseHandle(hFileMap);
  }
  _tprintf(TEXT("File name is %s\n"), pszFilename);
  return(bSuccess);
}

int _tmain(int argc, TCHAR *argv[])
{
    HANDLE hFile;

    if( argc != 2 )
    {
        _tprintf(TEXT("This sample takes a file name as a parameter.\n"));
        return 0;
    }
    hFile = CreateFile(argv[1], GENERIC_READ, FILE_SHARE_READ, NULL,
        OPEN_EXISTING, 0, NULL);

    if(hFile == INVALID_HANDLE_VALUE)
    {
        _tprintf(TEXT("CreateFile failed with %d\n"), GetLastError());
        return 0;
    }
    GetFileNameFromHandle( hFile );
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Dateizuordnung](using-file-mapping.md)
</dt> <dt>

[**GetFinalPathNameByHandle**](/windows/win32/api/fileapi/nf-fileapi-getfinalpathnamebyhandlea)
</dt> </dl>

 

 
