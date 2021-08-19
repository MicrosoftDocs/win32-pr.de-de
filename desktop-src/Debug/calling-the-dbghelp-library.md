---
description: Obwohl DbgHelp.dll mit allen Versionen von Windows ausgeliefert wird, sollten Aufrufer erwägen, eine der neueren Versionen dieser DLL zu verwenden, wie im Paket Debugtools für Windows zu finden. Ausführliche Informationen zur Verteilung von DbgHelp finden Sie unter DbgHelp-Versionen.
ms.assetid: 4e615e75-5ab8-4155-a3d3-b96313b37e9b
title: Aufrufen der DbgHelp-Bibliothek
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4d6a111da8b0874a0c66fa08840e1ea4edeabf539afab2e9decf0eb19372db3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957159"
---
# <a name="calling-the-dbghelp-library"></a>Aufrufen der DbgHelp-Bibliothek

Obwohl DbgHelp.dll mit allen Versionen von Windows ausgeliefert wird, sollten Aufrufer erwägen, eine der neueren Versionen dieser DLL zu verwenden, wie im [Paket Debugtools für Windows](https://www.microsoft.com/?ref=go) zu finden. Ausführliche Informationen zur Verteilung von DbgHelp finden Sie unter [DbgHelp-Versionen.](dbghelp-versions.md)

Bei Verwendung von DbgHelp besteht die beste Strategie darin, eine Kopie der Bibliothek aus dem [Paket Debugtools für Windows](https://www.microsoft.com/?ref=go) im Anwendungsverzeichnis zu installieren, das logisch neben der Software liegt, die sie aufruft. Wenn auch Symbolserver und Quellserver benötigt werden, müssen sowohl SymSrv.dll als auch SrcSrv.dll im selben Verzeichnis wie DbgHelp.dll installiert werden, da DbgHelp diese DLLs nur aufruft, wenn sie dasselbe Verzeichnis verwenden. (Beachten Sie, dass DbgHelp diese beiden DLLs nicht aus dem Standardsuchpfad aufruft.) Dadurch wird verhindert, dass nicht übereinstimmende DLLs verwendet werden. Ebenso verbessert es auch die Sicherheit insgesamt.

Der folgende Code wird aus der DbgHelp-Quelle extrahiert. Es wird gezeigt, wie DbgHelp nur Versionen von SymSrv.dll und SrcSrv.dll aus demselben Verzeichnis lädt, in dem sich DbgHelp.dll befinden.


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



Nach dem Laden dieser beiden DLLs ruft DbgHelp [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) auf, um die benötigten Funktionen von ihnen abzurufen.

Normalerweise stellt Code, der DbgHelp.dll aufruft, sicher, dass die richtige Version geladen wird, indem DbgHelp.dll im gleichen Verzeichnis wie die Anwendung installiert wird, die den aktuellen Prozess initiiert hat. Wenn sich der aufrufende Code in einer DLL befindet und keinen Zugriff auf den Speicherort des ursprünglichen Prozesses hat oder diesen nicht kann, muss DbgHelp.dll zusammen mit der aufrufenden DLL installiert werden, und es sollte Code ähnlich wie LoadDLL von DbgHelp verwendet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DbgHelp-Versionen](dbghelp-versions.md)
</dt> <dt>

[**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)
</dt> </dl>

 

 
