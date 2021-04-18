---
description: Obwohl DbgHelp.dll in allen Versionen von Windows enthalten ist, sollten Aufrufer die Verwendung einer der neueren Versionen dieser DLL in Erwägung gezogen werden, die im Paket Debuggingtools für Windows enthalten ist. Ausführliche Informationen zur Verteilung von dbghelp finden Sie unter dbghelp-Versionen.
ms.assetid: 4e615e75-5ab8-4155-a3d3-b96313b37e9b
title: Aufrufen der DbgHelp-Bibliothek
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70cc06f6a0e28f163d80490647ee8f33754c249b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482750"
---
# <a name="calling-the-dbghelp-library"></a><span data-ttu-id="264f4-104">Aufrufen der DbgHelp-Bibliothek</span><span class="sxs-lookup"><span data-stu-id="264f4-104">Calling the DbgHelp Library</span></span>

<span data-ttu-id="264f4-105">Obwohl DbgHelp.dll in allen Versionen von Windows enthalten ist, sollten Aufrufer die Verwendung einer der neueren Versionen dieser DLL in Erwägung gezogen werden, die im Paket [Debuggingtools für Windows](https://www.microsoft.com/?ref=go) enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="264f4-105">Although DbgHelp.dll ships with all versions of Windows, callers should consider using one of the more recent versions of this DLL as found in the [Debugging Tools For Windows](https://www.microsoft.com/?ref=go) package.</span></span> <span data-ttu-id="264f4-106">Ausführliche Informationen zur Verteilung von dbghelp finden Sie unter [dbghelp-Versionen](dbghelp-versions.md).</span><span class="sxs-lookup"><span data-stu-id="264f4-106">For details on distribution of DbgHelp, see [DbgHelp Versions](dbghelp-versions.md).</span></span>

<span data-ttu-id="264f4-107">Bei Verwendung von dbghelp besteht die beste Strategie darin, eine Kopie der Bibliothek aus dem Paket " [Debugtools für Windows](https://www.microsoft.com/?ref=go) " im Anwendungsverzeichnis zu installieren, das logisch neben der Software basiert, die Sie aufruft.</span><span class="sxs-lookup"><span data-stu-id="264f4-107">When using DbgHelp, the best strategy is to install a copy of the library from the [Debugging Tools For Windows](https://www.microsoft.com/?ref=go) package in the application directory logically adjacent to the software that calls it.</span></span> <span data-ttu-id="264f4-108">Wenn Symbol Server und Quell Server ebenfalls benötigt werden, müssen sowohl SymSrv.dll als auch SrcSrv.dll in demselben Verzeichnis wie DbgHelp.dll installiert werden, da dbghelp diese DLLs nur aufruft, wenn Sie dasselbe Verzeichnis gemeinsam verwenden.</span><span class="sxs-lookup"><span data-stu-id="264f4-108">If Symbol Server and Source Server are also needed, then both SymSrv.dll and SrcSrv.dll must be installed in the same directory as DbgHelp.dll, as DbgHelp will only call these DLLs if they share the same directory with it.</span></span> <span data-ttu-id="264f4-109">(Beachten Sie, dass dbghelp diese beiden DLLs nicht vom Standard Suchpfad aufruft.) Dadurch wird die Verwendung von nicht übereinstimmenden DLLs verhindert. Ebenso wird die Gesamtsicherheit verbessert.</span><span class="sxs-lookup"><span data-stu-id="264f4-109">(Note that DbgHelp will not call these two DLLs from the standard search path.) This helps prevent the usage of mismatched DLLs; likewise, it also improves security overall.</span></span>

<span data-ttu-id="264f4-110">Der folgende Code wird aus der dbghelp-Quelle extrahiert.</span><span class="sxs-lookup"><span data-stu-id="264f4-110">The following code is extracted from the DbgHelp source.</span></span> <span data-ttu-id="264f4-111">Es zeigt, wie dbghelp nur Versionen von SymSrv.dll und SrcSrv.dll aus demselben Verzeichnis lädt, in dem DbgHelp.dll sich befindet.</span><span class="sxs-lookup"><span data-stu-id="264f4-111">It shows how DbgHelp only loads versions of SymSrv.dll and SrcSrv.dll from the same directory that DbgHelp.dll resides in.</span></span>


```C++
HINSTANCE ghinst;

// For calculating the size of arrays for safe string functions.

#ifndef cch
 #define ccht(Array, EltType) (sizeof(Array) / sizeof(EltType))
 #define cch(Array) ccht(Array, (Array)[0])
#endif

//
// LoadLibrary() a DLL, using the same directory as dbghelp.dll.
//

HMODULE 
LoadDLL(
    __in PCWSTR filename
    )
{
    WCHAR drive[10] = L"";
    WCHAR dir[MAX_PATH + 1] = L"";
    WCHAR file[MAX_PATH + 1] = L"";
    WCHAR ext[MAX_PATH + 1] = L"";
    WCHAR path[MAX_PATH + 1] = L"";
    HMODULE hm;
    
    // Chop up 'filename' into its elements.
    
    _wsplitpath_s(filename, drive, cch(drive), dir, cch(dir), file, cch(file), ext, cch(ext));

    // If 'filename' contains no path information, then get the path to our module and 
    // use it to create a fully qualified path to the module we are loading.  Then load it.
    
    if (!*drive && !*dir) 
    {
        // ghinst is the HINSTANCE of this module, initialized in DllMain or WinMain
         
        if (GetModuleFileNameW(ghinst, path, MAX_PATH)) 
        {
            _wsplitpath_s(path, drive, cch(drive), dir, cch(dir), NULL, 0, NULL, 0);
            if (*drive || *dir) 
            {
                swprintf_s(path, cch(path), L"%s%s%s%s", drive, dir, file, ext);
                hm = LoadLibrary(path);
                if (hm)
                    return hm;
            }
        }
    }
    else
    {
        // If we wanted to, we could have LoadDLL also support directories being specified
        // in 'filename'.  We could pass the path here.  The result is if no path is specified,
        // the module path is used as above, otherwise the path in 'filename' is specified.
        // But the standard search logic of LoadLibrary is still avoided.
        
        /*
        hm = LoadLibrary(path);
        if (hm)
            return hm;
        */
    }
    
    return 0;
}
```



<span data-ttu-id="264f4-112">Nachdem Sie diese beiden DLLs geladen haben, ruft dbghelp [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) auf, um die benötigten Funktionen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="264f4-112">After loading these two DLLs, DbgHelp calls [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) to obtain the functions it needs from them.</span></span>

<span data-ttu-id="264f4-113">Normalerweise wird durch Code, der DbgHelp.dll aufruft, sichergestellt, dass die richtige Version geladen wird, indem DbgHelp.dll in demselben Verzeichnis wie die Anwendung installiert wird, die den aktuellen Prozess initiiert hat.</span><span class="sxs-lookup"><span data-stu-id="264f4-113">Normally, code that calls DbgHelp.dll ensures that the correct version is loaded by installing DbgHelp.dll in the same directory as the application that initiated the current process.</span></span> <span data-ttu-id="264f4-114">Wenn sich der aufrufende Code in einer DLL befindet und keinen Zugriff auf den Speicherort des anfänglichen Prozesses hat, müssen DbgHelp.dll zusammen mit der aufrufenden dll installiert werden, und der Code, der der loaddll von dbghelp ähnelt, sollte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="264f4-114">If the calling code is in a DLL and does not have access to or knowledge of the location of the initial process, then DbgHelp.dll must be installed alongside the calling DLL and code similar to DbgHelp's LoadDLL should be used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="264f4-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="264f4-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="264f4-116">Dbghelp-Versionen</span><span class="sxs-lookup"><span data-stu-id="264f4-116">DbgHelp Versions</span></span>](dbghelp-versions.md)
</dt> <dt>

[<span data-ttu-id="264f4-117">**LoadLibrary**</span><span class="sxs-lookup"><span data-stu-id="264f4-117">**LoadLibrary**</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[<span data-ttu-id="264f4-118">**GetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="264f4-118">**GetProcAddress**</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[<span data-ttu-id="264f4-119">**Fehler bei GetModuleFileName**</span><span class="sxs-lookup"><span data-stu-id="264f4-119">**GetModuleFileName**</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)
</dt> </dl>

 

 
