---
title: Zuschneiden eines Bilds
description: Zuschneiden eines Bilds
ms.assetid: 6600751c-d4b6-481d-bf69-be2d34244c05
keywords:
- Mciwndgetsource-Makro
- Mciwndputsource-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2d73eb37792c124ad907f660d4b906ca80e715d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471189"
---
# <a name="cropping-an-image"></a><span data-ttu-id="a8a53-105">Zuschneiden eines Bilds</span><span class="sxs-lookup"><span data-stu-id="a8a53-105">Cropping an Image</span></span>

<span data-ttu-id="a8a53-106">Im folgenden Beispiel wird ein mciwnd-Fenster erstellt und eine AVI-Datei geladen.</span><span class="sxs-lookup"><span data-stu-id="a8a53-106">The following example creates an MCIWnd window and loads an AVI file.</span></span> <span data-ttu-id="a8a53-107">Das Fenster enthält einen Befehl zum Zuschneiden im Menü, das eine Viertel der Höhe oder Breite von jeder der vier Seiten des Frames aufbindet.</span><span class="sxs-lookup"><span data-stu-id="a8a53-107">The window includes a crop command in the menu, which crops one-quarter of the height or width from each of the four sides of the frame.</span></span> <span data-ttu-id="a8a53-108">Im Beispiel werden die aktuellen (anfänglichen) Dimensionen des Quell Rechtecks mithilfe des [**mciwndgetsource**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource) -Makros abgerufen.</span><span class="sxs-lookup"><span data-stu-id="a8a53-108">The example retrieves the current (initial) dimensions of the source rectangle by using the [**MCIWndGetSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource) macro.</span></span> <span data-ttu-id="a8a53-109">Das geänderte Quell Rechteck ist die Hälfte der ursprünglichen Höhe und Breite und wird im ursprünglichen Frame zentriert.</span><span class="sxs-lookup"><span data-stu-id="a8a53-109">The modified source rectangle is half the original height and width and is centered in the original frame.</span></span> <span data-ttu-id="a8a53-110">Der-Befehl zum [**mciwndputsource**](/windows/desktop/api/Vfw/nf-vfw-mciwndputsource) -Makro definiert die Koordinaten des Quell Rechtecks neu.</span><span class="sxs-lookup"><span data-stu-id="a8a53-110">The call to the [**MCIWndPutSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndputsource) macro redefines the coordinates of the source rectangle.</span></span>


```C++
// extern RECT rSource, rDest; 
 
case WM_COMMAND: 
    switch (wParam) 
    { 
        case IDM_CREATEMCIWND: 
            g_hwndMCIWnd = MCIWndCreate( hwnd, 
                g_hinst, 
                WS_CHILD | WS_VISIBLE, 
                "sample.avi" ); 
            break; 
        case IDM_CROPIMAGE:                          // crops image 
            MCIWndGetSource(g_hwndMCIWnd, &rSource); // source rectangle
            rDest.left = rSource.left +              // new boundaries
                ((rSource.right - rSource.left) / 4); 
            rDest.right = rSource.right - 
                ((rSource.right - rSource.left) / 4); 
            rDest.top = rSource.top + 
                ((rSource.bottom - rSource.top) / 4); 
            rDest.bottom = rSource.bottom - 
                ((rSource.bottom - rSource.top) / 4); 
 
            MCIWndPutSource(g_hwndMCIWnd, &rDest);   // new source rectangle 
    } 
    break; 

    // Handle other messages here. 
```



 

 




