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
# <a name="loading-a-symbol-module"></a><span data-ttu-id="5a691-103">Laden eines Symbol Moduls</span><span class="sxs-lookup"><span data-stu-id="5a691-103">Loading a Symbol Module</span></span>

<span data-ttu-id="5a691-104">Wenn eine Anwendung die [**syminitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) -Funktion nicht aufruft und der *finvadeprocess* -Parameter auf " **true**" festgelegt ist, muss Sie Symbole für ein Modul laden, wenn Sie benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="5a691-104">If an application does not call the [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) function with the *fInvadeProcess* parameter set to **TRUE**, it must load symbols for a module when they are required.</span></span> <span data-ttu-id="5a691-105">Um ein Symbol Modul Bedarfs gesteuert zu laden, kann die Anwendung die [**symloadmoduleex**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) -Funktion mit einem vollständigen Pfad zu einem Modulnamen aufrufen.</span><span class="sxs-lookup"><span data-stu-id="5a691-105">To load a symbol module on demand, the application can call the [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) function with a full path to a module name.</span></span> <span data-ttu-id="5a691-106">Wenn das Modul geladen wird, lädt der Symbol Handler die Symbole entweder sofort direkt oder verzögert die Last, abhängig von den Optionen, die mithilfe der [**symsetoptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) -Funktion festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="5a691-106">When the module is loaded, the symbol handler will either load the symbols immediately or defer the load, depending on the options set using the [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) function.</span></span>

<span data-ttu-id="5a691-107">Mit dem folgenden Code wird ein Symbol Modul geladen.</span><span class="sxs-lookup"><span data-stu-id="5a691-107">The following code loads a symbol module.</span></span> <span data-ttu-id="5a691-108">Beachten Sie, dass Sie den Symbol Handler mithilfe des Codes beim [Initialisieren des Symbol Handlers](initializing-the-symbol-handler.md)initialisiert haben.</span><span class="sxs-lookup"><span data-stu-id="5a691-108">Note that it assumes you have initialized the symbol handler using the code in [Initializing the Symbol Handler](initializing-the-symbol-handler.md).</span></span>


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



<span data-ttu-id="5a691-109">Beachten Sie, dass " *szimagename* " ein Pfad zu allen ausführbaren Modulen sein kann, die über Debuginformationen verfügen (. exe,. dll,. drv,. sys,. scr,. cpl,. com).</span><span class="sxs-lookup"><span data-stu-id="5a691-109">Note that *szImageName* can be a path to any executable module that has debugging information (.exe, .dll, .drv, .sys, .scr, .cpl, .com).</span></span> <span data-ttu-id="5a691-110">Außerdem ist *dwbaseaddr* die Basisadresse des zu ladenden Symbol Moduls.</span><span class="sxs-lookup"><span data-stu-id="5a691-110">Also, *dwBaseAddr* is the base address of the symbol module to be loaded.</span></span> <span data-ttu-id="5a691-111">Wenn dieser Wert 0 ist, erhält der Symbol Handler die Basisadresse aus dem angegebenen Symbol Modul.</span><span class="sxs-lookup"><span data-stu-id="5a691-111">If this value is 0, the symbol handler will obtain the base address from the specified symbol module.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5a691-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5a691-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a691-113">Entladen eines Symbol Moduls</span><span class="sxs-lookup"><span data-stu-id="5a691-113">Unloading a Symbol Module</span></span>](unloading-a-symbol-module.md)
</dt> </dl>

 

 



