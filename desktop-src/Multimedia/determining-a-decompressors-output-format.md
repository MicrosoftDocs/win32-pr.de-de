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
# <a name="determining-a-decompressors-output-format"></a><span data-ttu-id="f000d-108">Bestimmen des Ausgabeformats eines dekompressors</span><span class="sxs-lookup"><span data-stu-id="f000d-108">Determining a Decompressor's Output Format</span></span>

<span data-ttu-id="f000d-109">Im folgenden Beispiel wird die Puffergröße bestimmt, die für die Daten erforderlich ist, die das Dekomprimierungs Format mithilfe des [**icdecompressgetformatsize**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformatsize) -Makros angeben. dabei wird ein Puffer der entsprechenden Größe mithilfe der [globalzuordc](/windows/win32/api/winbase/nf-winbase-globalalloc) -Funktion zugewiesen, und die Informationen zur Dekomprimierungs Formatierung werden mithilfe des [**icdecompressgetformat**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformat) -Makros abgerufen.</span><span class="sxs-lookup"><span data-stu-id="f000d-109">The following example determines the buffer size needed for the data specifying the decompression format using the [**ICDecompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformatsize) macro, allocates a buffer of the appropriate size using the [GlobalAlloc](/windows/win32/api/winbase/nf-winbase-globalalloc) function, and retrieves the decompression format information using the [**ICDecompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformat) macro.</span></span>


```C++
LPBITMAPINFOHEADER lpbiIn, lpbiOut; 
 
// Assume *lpbiIn points to the input (compressed) format. 
dwFormatSize = ICDecompressGetFormatSize(hIC, lpbiIn); 
h = GlobalAlloc(GHND, dwFormatSize); 
lpbiOut = (LPBITMAPINFOHEADER)GlobalLock(h); 
ICDecompressGetFormat(hIC, lpbiIn, lpbiOut); 
 
```



<span data-ttu-id="f000d-110">Das folgende Beispiel zeigt, wie eine Anwendung das [**icdecompressquery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery) -Makro verwenden kann, um zu bestimmen, ob ein Dekompressor die Eingabe-und Ausgabeformate verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="f000d-110">The following example shows how an application can use the [**ICDecompressQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery) macro to determine if a decompressor can handle the input and output formats.</span></span>


```C++
LPBITMAPINFOHEADER lpbiIn, lpbiOut; 
// Assume *lpbiIn & *lpbiOut are initialized to the respective 
// formats.
 
if (ICDecompressQuery(hIC, lpbiIn, lpbiOut) == ICERR_OK)
{ 
    
    // Format is supported - use the decompressor. 
    
} 
 
```



<span data-ttu-id="f000d-111">Das folgende Code Fragment zeigt, wie die Paletteninformationen mithilfe des [**icdecompressgetpalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetpalette) -Makros abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f000d-111">The following code fragment shows how to get the palette information using the [**ICDecompressGetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetpalette) macro.</span></span>


```C++
ICDecompressGetPalette(hIC, lpbiIn, lpbiOut); 
 
// Move up to the palette. 
lpPalette = (LPBYTE)lpbiOut + lpbi->biSize;
 
 
```



 

 