---
title: Bestimmen des Ausgabeformats eines dekompressors
description: Bestimmen des Ausgabeformats eines dekompressors
ms.assetid: afedef5e-a506-40bd-aaad-fd85b0468ed7
keywords:
- Videokomprimierungs-Manager (VCM), Ausgabeformat
- VCM (Videokomprimierungs-Manager), Ausgabeformat
- ICDE compressgetformatsize-Makro
- Icabcompressquery-Makro
- ICDE compressgetpalette-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fcb4140a4118cb2a36ccd75088556c53c55fdcb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101574"
---
# <a name="determining-a-decompressors-output-format"></a>Bestimmen des Ausgabeformats eines dekompressors

Im folgenden Beispiel wird die Puffergröße bestimmt, die für die Daten erforderlich ist, die das Dekomprimierungs Format mithilfe des [**icdecompressgetformatsize**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformatsize) -Makros angeben. dabei wird ein Puffer der entsprechenden Größe mithilfe der [globalzuordc](/windows/win32/api/winbase/nf-winbase-globalalloc) -Funktion zugewiesen, und die Informationen zur Dekomprimierungs Formatierung werden mithilfe des [**icdecompressgetformat**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformat) -Makros abgerufen.


```C++
LPBITMAPINFOHEADER lpbiIn, lpbiOut; 
 
// Assume *lpbiIn points to the input (compressed) format. 
dwFormatSize = ICDecompressGetFormatSize(hIC, lpbiIn); 
h = GlobalAlloc(GHND, dwFormatSize); 
lpbiOut = (LPBITMAPINFOHEADER)GlobalLock(h); 
ICDecompressGetFormat(hIC, lpbiIn, lpbiOut); 
 
```



Das folgende Beispiel zeigt, wie eine Anwendung das [**icdecompressquery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery) -Makro verwenden kann, um zu bestimmen, ob ein Dekompressor die Eingabe-und Ausgabeformate verarbeiten kann.


```C++
LPBITMAPINFOHEADER lpbiIn, lpbiOut; 
// Assume *lpbiIn & *lpbiOut are initialized to the respective 
// formats.
 
if (ICDecompressQuery(hIC, lpbiIn, lpbiOut) == ICERR_OK)
{ 
    
    // Format is supported - use the decompressor. 
    
} 
 
```



Das folgende Code Fragment zeigt, wie die Paletteninformationen mithilfe des [**icdecompressgetpalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetpalette) -Makros abgerufen werden.


```C++
ICDecompressGetPalette(hIC, lpbiIn, lpbiOut); 
 
// Move up to the palette. 
lpPalette = (LPBYTE)lpbiOut + lpbi->biSize;
 
 
```



 

 