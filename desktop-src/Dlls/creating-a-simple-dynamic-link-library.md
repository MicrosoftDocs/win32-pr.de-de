---
description: Das folgende Beispiel zeigt den Quellcode, der erforderlich ist, um eine einfache dll, Myputs.dll, zu erstellen.
ms.assetid: 3b11a83b-9943-4b66-8d0d-4a236ad5ffb8
title: Erstellen einer einfachen Dynamic-Link Bibliothek
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 572c25c87a3130739a55fcccfc9d8f9c6514d812
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359925"
---
# <a name="creating-a-simple-dynamic-link-library"></a><span data-ttu-id="d92b2-103">Erstellen einer einfachen Dynamic-Link Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d92b2-103">Creating a Simple Dynamic-Link Library</span></span>

<span data-ttu-id="d92b2-104">Das folgende Beispiel zeigt den Quellcode, der erforderlich ist, um eine einfache dll, Myputs.dll, zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d92b2-104">The following example is the source code needed to create a simple DLL, Myputs.dll.</span></span> <span data-ttu-id="d92b2-105">Es definiert eine einfache Funktion zum Drucken von Zeichen folgen, die als myputs bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="d92b2-105">It defines a simple string-printing function called myPuts.</span></span> <span data-ttu-id="d92b2-106">Die DLL-Datei "myputs" definiert keine Einstiegspunkt Funktion, da Sie mit der C-Lauf Zeit Bibliothek verknüpft ist und keine eigenen Initialisierungs-oder Bereinigungs Funktionen aufweist.</span><span class="sxs-lookup"><span data-stu-id="d92b2-106">The Myputs DLL does not define an entry-point function, because it is linked with the C run-time library and has no initialization or cleanup functions of its own to perform.</span></span>

<span data-ttu-id="d92b2-107">Um die dll zu erstellen, befolgen Sie die Anweisungen in der Dokumentation, die im Lieferumfang der Entwicklungs Tools enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="d92b2-107">To build the DLL, follow the directions in the documentation included with your development tools.</span></span>

<span data-ttu-id="d92b2-108">Ein Beispiel für die Verwendung von myputs finden [Sie unter using Load-Time Dynamic Linking](using-load-time-dynamic-linking.md) or [using Run-Time Dynamic Linking](using-run-time-dynamic-linking.md).</span><span class="sxs-lookup"><span data-stu-id="d92b2-108">For an example that uses myPuts, see [Using Load-Time Dynamic Linking](using-load-time-dynamic-linking.md) or [Using Run-Time Dynamic Linking](using-run-time-dynamic-linking.md).</span></span>


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



 

 



