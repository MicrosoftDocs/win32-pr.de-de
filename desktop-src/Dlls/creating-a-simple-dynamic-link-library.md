---
description: Das folgende Beispiel ist der Quellcode, der zum Erstellen einer einfachen DLL erforderlich ist, Myputs.dll.
ms.assetid: 3b11a83b-9943-4b66-8d0d-4a236ad5ffb8
title: Erstellen einer simple Dynamic-Link Library
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c3708f98c6b916c54940bc1667ebc4827b29c78596f55102331491aca29e65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963790"
---
# <a name="creating-a-simple-dynamic-link-library"></a>Erstellen einer simple Dynamic-Link Library

Das folgende Beispiel ist der Quellcode, der zum Erstellen einer einfachen DLL erforderlich ist, Myputs.dll. Sie definiert eine einfache Zeichenfolgendruckfunktion namens myPuts. Die Myputs-DLL definiert keine Einstiegspunktfunktion, da sie mit der C-Laufzeitbibliothek verknüpft ist und über keine eigenen Initialisierungs- oder Bereinigungsfunktionen verfügt.

Um die DLL zu erstellen, befolgen Sie die Anweisungen in der Dokumentation, die in Ihren Entwicklungstools enthalten ist.

Ein Beispiel für die Verwendung von myPuts finden Sie unter [Using Load-Time Dynamic Linking](using-load-time-dynamic-linking.md) oder Using Run-Time Dynamic [Linking](using-run-time-dynamic-linking.md).


```C++
// The myPuts function writes a null-terminated string to
// the standard output device.
 
// The export mechanism used here is the __declspec(export)
// method supported by Microsoft Visual Studio, but any
// other export method supported by your development
// environment may be substituted.
 
 
#include <windows.h>
 
#define EOF (-1)
 
#ifdef __cplusplus    // If used by C++ code, 
extern "C" {          // we need to export the C interface
#endif
 
__declspec(dllexport) int __cdecl myPuts(LPWSTR lpszMsg)
{
    DWORD cchWritten;
    HANDLE hConout;
    BOOL fRet;
 
    // Get a handle to the console output device.

    hConout = CreateFileW(L"CONOUT$",
                         GENERIC_WRITE,
                         FILE_SHARE_WRITE,
                         NULL,
                         OPEN_EXISTING,
                         FILE_ATTRIBUTE_NORMAL,
                         NULL);

    if (INVALID_HANDLE_VALUE == hConout)
        return EOF;
 
    // Write a null-terminated string to the console output device.
 
    while (*lpszMsg != L'\0')
    {
        fRet = WriteConsole(hConout, lpszMsg, 1, &cchWritten, NULL);
        if( (FALSE == fRet) || (1 != cchWritten) )
            return EOF;
        lpszMsg++;
    }
    return 1;
}
 
#ifdef __cplusplus
}
#endif
```



 

 



