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
# <a name="color-index-mode-and-windows-palette-management"></a>Color-Index Modus und Windows-Palettenverwaltung

Der Farb Index Modus gibt Farben in einer logischen Palette mit einem Index zu einem bestimmten logischen Paletteneintrag an. Die meisten GDI-Programme verwenden Farb Index Paletten, aber der RGBA-Modus funktioniert für OpenGL besser, wenn es um verschiedene Effekte geht, z. b. Schattierung, Beleuchtung, Nebel und Textur Zuordnung. Wenn die unwahre Farbe für Ihre OpenGL-Anwendung nicht entscheidend ist, können Sie den Farb Index Modus verwenden (z. b. für eine Topographic-Karte, die "false Color" verwendet, um den uploververlauf hervorzuheben).

## <a name="color-index-mode-palette-sample"></a>Beispiel für Color-Index Modus-Palette

Der folgende Code richtet eine [**pixelformatdescriptor**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) -Struktur ein, die das-Flag des **ipixeltype** -Members auf den PFD- \_ Typ \_ ColorIndex festlegt. Dies gibt an, dass die Anwendung eine Farb Index Palette verwendet.


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



 

 




