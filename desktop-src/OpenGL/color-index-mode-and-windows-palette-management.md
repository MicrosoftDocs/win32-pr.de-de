---
title: Color-Index Modus und Windows Palettenverwaltung
description: Der Farbindexmodus gibt Farben in einer logischen Palette mit einem Index für einen bestimmten Eintrag der logischen Palette an.
ms.assetid: 8cf07c3e-8a8b-4f28-a363-34d3c0d33890
keywords:
- OpenGL auf Windows,Palettenverwaltung
- OpenGL im Windows,Farbindexmodus
- Farbindexmodus OpenGL
- Palettenverwaltung OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72e4d7c9db02a80bdffdef93655e88cc5b2ca8197a58c5ffdb488c2b782f10d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119889260"
---
# <a name="color-index-mode-and-windows-palette-management"></a>Color-Index Modus und Windows Palettenverwaltung

Der Farbindexmodus gibt Farben in einer logischen Palette mit einem Index für einen bestimmten Eintrag der logischen Palette an. Die meisten GDI-Programme verwenden Farbindexpaletten, aber der RGBA-Modus funktioniert für OpenGL besser für verschiedene Effekte, z. B. Schattierung, Beleuchtung, Oberfläche und Texturzuordnung. Wenn es für Ihre OpenGL-Anwendung nicht wichtig ist, die wahrste Farbe zu haben, können Sie den Farbindexmodus verwenden (z. B. für eine topografische Karte, die "false color" verwendet, um den Farbverlauf der Erhöhung hervorzuheben).

## <a name="color-index-mode-palette-sample"></a>Palettenbeispiel für Color-Index Modus

Der folgende Code richtet eine [**PIXELFORMATDESCRIPTOR-Struktur**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) ein, die das Flag des **iPixelType-Members** auf PFD \_ TYPE \_ COLORINDEX festlegt. Dadurch wird angegeben, dass die Anwendung eine Farbindexpalette verwendet.


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



 

 




