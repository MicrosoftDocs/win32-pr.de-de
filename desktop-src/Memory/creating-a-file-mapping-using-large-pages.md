---
description: Im folgenden Beispiel wird die Funktion "kreatefilemapping" mit dem sec- \_ \_ Flag für große Seiten verwendet, um große Seiten zu verwenden. Hierfür ist Windows Server 2003 mit Service Pack 1 (SP1) oder höher erforderlich.
ms.assetid: be2cdcbc-03e8-407d-8ae2-569f8fd8cba8
title: Erstellen einer Datei Zuordnung mithilfe von großen Seiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49a852de187f6798904ef1795dca5955663283f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345702"
---
# <a name="creating-a-file-mapping-using-large-pages"></a><span data-ttu-id="d51f5-104">Erstellen einer Datei Zuordnung mithilfe von großen Seiten</span><span class="sxs-lookup"><span data-stu-id="d51f5-104">Creating a File Mapping Using Large Pages</span></span>

<span data-ttu-id="d51f5-105">Im folgenden Beispiel wird die Funktion " [**kreatefilemapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) " mit dem sec-Flag für **\_ große \_ Seiten** verwendet, um große Seiten zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="d51f5-105">The following example uses the [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) function with the **SEC\_LARGE\_PAGES** flag to use large pages.</span></span> <span data-ttu-id="d51f5-106">Der Puffer muss groß genug sein, um die minimale Größe einer großen Seite zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="d51f5-106">The buffer must be large enough to contain the minimum size of a large page.</span></span> <span data-ttu-id="d51f5-107">Dieser Wert wird mithilfe der [**GetLargePageMinimum**](/windows/win32/api/memoryapi/nf-memoryapi-getlargepageminimum) -Funktion abgerufen.</span><span class="sxs-lookup"><span data-stu-id="d51f5-107">This value is obtained using the [**GetLargePageMinimum**](/windows/win32/api/memoryapi/nf-memoryapi-getlargepageminimum) function.</span></span> <span data-ttu-id="d51f5-108">Diese Funktion erfordert auch die Berechtigung "SeLockMemoryPrivilege".</span><span class="sxs-lookup"><span data-stu-id="d51f5-108">This feature also requires the "SeLockMemoryPrivilege" privilege.</span></span>

> [!NOTE]
> <span data-ttu-id="d51f5-109">Ab Windows 10, Version 1703, ordnet die [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) -Funktion standardmäßig eine Ansicht mithilfe von kleinen Seiten zu, auch für Datei Zuordnungs Objekte, die mit dem sec-Flag für **\_ große \_ Seiten** erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="d51f5-109">Starting in Windows 10, version 1703, the [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) function maps a view using small pages by default, even for file mapping objects created with the **SEC\_LARGE\_PAGES** flag.</span></span> <span data-ttu-id="d51f5-110">In dieser und späteren Betriebssystemversionen müssen Sie das Flag für die Datei Zuordnung für **\_ \_ große \_ Seiten** mit der [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) -Funktion angeben, um große Seiten zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="d51f5-110">In this and later OS versions, you must specify the **FILE\_MAP\_LARGE\_PAGES** flag with the [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) function to map large pages.</span></span> <span data-ttu-id="d51f5-111">Dieses Flag wird bei Betriebssystemversionen vor Windows 10, Version 1703, ignoriert.</span><span class="sxs-lookup"><span data-stu-id="d51f5-111">This flag is ignored on OS versions before Windows 10, version 1703.</span></span>


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

#define BUF_SIZE 65536

TCHAR szName[]=TEXT("LARGEPAGE");
typedef int (*GETLARGEPAGEMINIMUM)(void);

void DisplayError(const wchar_t* pszAPI, DWORD dwError)
{
    LPVOID lpvMessageBuffer;

    FormatMessage(FORMAT_MESSAGE_ALLOCATE_BUFFER |
                  FORMAT_MESSAGE_FROM_SYSTEM |
                  FORMAT_MESSAGE_IGNORE_INSERTS,
                  NULL, dwError,
                  MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT),
                  (LPTSTR)&lpvMessageBuffer, 0, NULL);

    //... now display this string
    _tprintf(TEXT("ERROR: API        = %s\n"), pszAPI);
    _tprintf(TEXT("       error code = %d\n"), dwError);
    _tprintf(TEXT("       message    = %s\n"), lpvMessageBuffer);

    // Free the buffer allocated by the system
    LocalFree(lpvMessageBuffer);

    ExitProcess(GetLastError());
}

void Privilege(const wchar_t* pszPrivilege, BOOL bEnable)
{
    HANDLE           hToken;
    TOKEN_PRIVILEGES tp;
    BOOL             status;
    DWORD            error;

    // open process token
    if (!OpenProcessToken(GetCurrentProcess(), TOKEN_ADJUST_PRIVILEGES | TOKEN_QUERY, &hToken))
        DisplayError(TEXT("OpenProcessToken"), GetLastError());

    // get the luid
    if (!LookupPrivilegeValue(NULL, pszPrivilege, &tp.Privileges[0].Luid))
        DisplayError(TEXT("LookupPrivilegeValue"), GetLastError());

    tp.PrivilegeCount = 1;

    // enable or disable privilege
    if (bEnable)
        tp.Privileges[0].Attributes = SE_PRIVILEGE_ENABLED;
    else
        tp.Privileges[0].Attributes = 0;

    // enable or disable privilege
    status = AdjustTokenPrivileges(hToken, FALSE, &tp, 0, (PTOKEN_PRIVILEGES)NULL, 0);

    // It is possible for AdjustTokenPrivileges to return TRUE and still not succeed.
    // So always check for the last error value.
    error = GetLastError();
    if (!status || (error != ERROR_SUCCESS))
        DisplayError(TEXT("AdjustTokenPrivileges"), GetLastError());

    // close the handle
    if (!CloseHandle(hToken))
        DisplayError(TEXT("CloseHandle"), GetLastError());
}

int _tmain(void)
{
    HANDLE hMapFile;
    LPCTSTR pBuf;
    DWORD size;
    GETLARGEPAGEMINIMUM pGetLargePageMinimum;
    HINSTANCE  hDll;

    // call succeeds only on Windows Server 2003 SP1 or later
    hDll = LoadLibrary(TEXT("kernel32.dll"));
    if (hDll == NULL)
        DisplayError(TEXT("LoadLibrary"), GetLastError());

    pGetLargePageMinimum = (GETLARGEPAGEMINIMUM)GetProcAddress(hDll,
        "GetLargePageMinimum");
    if (pGetLargePageMinimum == NULL)
        DisplayError(TEXT("GetProcAddress"), GetLastError());

    size = (*pGetLargePageMinimum)();

    FreeLibrary(hDll);

    _tprintf(TEXT("Page Size: %u\n"), size);

    Privilege(TEXT("SeLockMemoryPrivilege"), TRUE);

    hMapFile = CreateFileMapping(
         INVALID_HANDLE_VALUE,    // use paging file
         NULL,                    // default security
         PAGE_READWRITE | SEC_COMMIT | SEC_LARGE_PAGES,
         0,                       // max. object size
         size,                    // buffer size
         szName);                 // name of mapping object

    if (hMapFile == NULL)
        DisplayError(TEXT("CreateFileMapping"), GetLastError());
    else
        _tprintf(TEXT("File mapping object successfully created.\n"));

    Privilege(TEXT("SeLockMemoryPrivilege"), FALSE);

    pBuf = (LPTSTR) MapViewOfFile(hMapFile,          // handle to map object
         FILE_MAP_ALL_ACCESS | FILE_MAP_LARGE_PAGES, // read/write permission
         0,
         0,
         BUF_SIZE);

    if (pBuf == NULL)
        DisplayError(TEXT("MapViewOfFile"), GetLastError());
    else
        _tprintf(TEXT("View of file successfully mapped.\n"));

    // do nothing, clean up an exit
    UnmapViewOfFile(pBuf);
    CloseHandle(hMapFile);
}
```



## <a name="related-topics"></a><span data-ttu-id="d51f5-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d51f5-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d51f5-113">Erstellen eines Datei Mapping-Objekts</span><span class="sxs-lookup"><span data-stu-id="d51f5-113">Creating a File Mapping Object</span></span>](creating-a-file-mapping-object.md)
</dt> <dt>

[<span data-ttu-id="d51f5-114">Unterstützung für große Seiten</span><span class="sxs-lookup"><span data-stu-id="d51f5-114">Large Page Support</span></span>](large-page-support.md)
</dt> </dl>

 

 
