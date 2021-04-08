---
title: Color-Index Modus und Windows-Palettenverwaltung
description: Der Farb Index Modus gibt Farben in einer logischen Palette mit einem Index zu einem bestimmten logischen Paletteneintrag an.
ms.assetid: 8cf07c3e-8a8b-4f28-a363-34d3c0d33890
keywords:
- OpenGL unter Windows, Palettenverwaltung
- OpenGL unter Windows, Farb Index Modus
- Farb Index Modus OpenGL
- Palette Management OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 873308c4ac64d496e344b1c71d440d4dc8321418
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037240"
---
# <a name="color-index-mode-and-windows-palette-management"></a><span data-ttu-id="cdefb-107">Color-Index Modus und Windows-Palettenverwaltung</span><span class="sxs-lookup"><span data-stu-id="cdefb-107">Color-Index Mode and Windows Palette Management</span></span>

<span data-ttu-id="cdefb-108">Der Farb Index Modus gibt Farben in einer logischen Palette mit einem Index zu einem bestimmten logischen Paletteneintrag an.</span><span class="sxs-lookup"><span data-stu-id="cdefb-108">The color-index mode specifies colors in a logical palette with an index to a specific logical-palette entry.</span></span> <span data-ttu-id="cdefb-109">Die meisten GDI-Programme verwenden Farb Index Paletten, aber der RGBA-Modus funktioniert für OpenGL besser, wenn es um verschiedene Effekte geht, z. b. Schattierung, Beleuchtung, Nebel und Textur Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="cdefb-109">Most GDI programs use color-index palettes, but the RGBA mode works better for OpenGL for several effects, such as shading, lighting, fog, and texture mapping.</span></span> <span data-ttu-id="cdefb-110">Wenn die unwahre Farbe für Ihre OpenGL-Anwendung nicht entscheidend ist, können Sie den Farb Index Modus verwenden (z. b. für eine Topographic-Karte, die "false Color" verwendet, um den uploververlauf hervorzuheben).</span><span class="sxs-lookup"><span data-stu-id="cdefb-110">If having the truest color isn't critical for your OpenGL application, you might choose to use the color-index mode (for example, for a topographic map that uses "false color" to emphasize the elevation gradient).</span></span>

## <a name="color-index-mode-palette-sample"></a><span data-ttu-id="cdefb-111">Beispiel für Color-Index Modus-Palette</span><span class="sxs-lookup"><span data-stu-id="cdefb-111">Color-Index Mode Palette Sample</span></span>

<span data-ttu-id="cdefb-112">Der folgende Code richtet eine [**pixelformatdescriptor**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) -Struktur ein, die das-Flag des **ipixeltype** -Members auf den PFD- \_ Typ \_ ColorIndex festlegt.</span><span class="sxs-lookup"><span data-stu-id="cdefb-112">The following code sets up a [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) structure that sets the flag of the **iPixelType** member to PFD\_TYPE\_COLORINDEX.</span></span> <span data-ttu-id="cdefb-113">Dies gibt an, dass die Anwendung eine Farb Index Palette verwendet.</span><span class="sxs-lookup"><span data-stu-id="cdefb-113">This specifies that the application use a color-index palette.</span></span>


```C++
BOOL bSetupPixelFormat(HDC hdc) 
{ 
    PIXELFORMATDESCRIPTOR pfd, *ppfd; 
    int pixelformat; 
 
    ppfd = &pfd; 
 
    ppfd->nSize = sizeof(PIXELFORMATDESCRIPTOR); 
    ppfd->nVersion = 1; 
    ppfd->dwFlags = PFD_DRAW_TO_WINDOW | PFD_SUPPORT_OPENGL |  
                        PFD_DOUBLEBUFFER; 
    ppfd->dwLayerMask = PFD_MAIN_PLANE; 
 
    /* Set to color-index mode and use the default color palette. */ 
    ppfd->iPixelType = PFD_TYPE_COLORINDEX;  
 
    ppfd->cColorBits = 8; 
    ppfd->cDepthBits = 16; 
    ppfd->cAccumBits = 0; 
    ppfd->cStencilBits = 0; 
 
    pixelformat = ChoosePixelFormat(hdc, ppfd); 
 
    if ( (pixelformat = ChoosePixelFormat(hdc, ppfd)) == 0 ) 
    { 
        MessageBox(NULL, "ChoosePixelFormat failed", "Error", MB_OK); 
        return FALSE; 
    } 
 
    if (SetPixelFormat(hdc, pixelformat, ppfd) == FALSE) 
    { 
        MessageBox(NULL, "SetPixelFormat failed", "Error", MB_OK); 
        return FALSE; 
    } 
 
    return TRUE; 
}
```



 

 




