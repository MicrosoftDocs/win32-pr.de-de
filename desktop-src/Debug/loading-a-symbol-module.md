---
description: Wenn eine Anwendung die syminitialize-Funktion nicht aufruft und der finvadeprocess-Parameter auf "true" festgelegt ist, muss Sie Symbole für ein Modul laden, wenn Sie benötigt werden.
ms.assetid: 01cee812-d1f2-4459-acee-bce8719a85b2
title: Laden eines Symbol Moduls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5182322e62b450333a064069ea5f5de2aa95e912
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125972"
---
# <a name="loading-a-symbol-module"></a>Laden eines Symbol Moduls

Wenn eine Anwendung die [**syminitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) -Funktion nicht aufruft und der *finvadeprocess* -Parameter auf " **true**" festgelegt ist, muss Sie Symbole für ein Modul laden, wenn Sie benötigt werden. Um ein Symbol Modul Bedarfs gesteuert zu laden, kann die Anwendung die [**symloadmoduleex**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) -Funktion mit einem vollständigen Pfad zu einem Modulnamen aufrufen. Wenn das Modul geladen wird, lädt der Symbol Handler die Symbole entweder sofort direkt oder verzögert die Last, abhängig von den Optionen, die mithilfe der [**symsetoptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) -Funktion festgelegt werden.

Mit dem folgenden Code wird ein Symbol Modul geladen. Beachten Sie, dass Sie den Symbol Handler mithilfe des Codes beim [Initialisieren des Symbol Handlers](initializing-the-symbol-handler.md)initialisiert haben.


```C++
TCHAR  szImageName[MAX_PATH] = TEXT("foo.dll");
DWORD64 dwBaseAddr = 0;

if (SymLoadModuleEx(hProcess,    // target process 
                    NULL,        // handle to image - not used
                    szImageName, // name of image file
                    NULL,        // name of module - not required
                    dwBaseAddr,  // base address - not required
                    0,           // size of image - not required
                    NULL,        // MODLOAD_DATA used for special cases 
                    0))          // flags - not required
{
    // SymLoadModuleEx returned success
}
else
{
    // SymLoadModuleEx failed
    DWORD error = GetLastError();
    printf("SymLoadModuleEx returned error : %d\n", error);
}
```



Beachten Sie, dass " *szimagename* " ein Pfad zu allen ausführbaren Modulen sein kann, die über Debuginformationen verfügen (. exe,. dll,. drv,. sys,. scr,. cpl,. com). Außerdem ist *dwbaseaddr* die Basisadresse des zu ladenden Symbol Moduls. Wenn dieser Wert 0 ist, erhält der Symbol Handler die Basisadresse aus dem angegebenen Symbol Modul.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entladen eines Symbol Moduls](unloading-a-symbol-module.md)
</dt> </dl>

 

 



