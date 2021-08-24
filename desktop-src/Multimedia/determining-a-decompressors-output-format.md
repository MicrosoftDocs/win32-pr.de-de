---
title: Bestimmen des Ausgabeformats eines Dekomprimierers
description: Bestimmen des Ausgabeformats eines Dekomprimierers
ms.assetid: afedef5e-a506-40bd-aaad-fd85b0468ed7
keywords:
- Videokomprimierungs-Manager (VCM), Ausgabeformat
- VCM (Videokomprimierungs-Manager),Ausgabeformat
- ICDecompressGetFormatSize-Makro
- ICDecompressQuery-Makro
- ICDecompressGetPalette-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cc17db0d7aa015c955825840fb70d12714be3c0a44a69bf5abc59290ebc633c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497420"
---
# <a name="determining-a-decompressors-output-format"></a>Bestimmen des Ausgabeformats eines Dekomprimierers

Im folgenden Beispiel wird die Puffergröße bestimmt, die für die Daten erforderlich ist, die das Dekomprimierungsformat mithilfe des [**ICDecompressGetFormatSize-Makros**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformatsize) angeben, einen Puffer der entsprechenden Größe mithilfe der [GlobalAlloc-Funktion](/windows/win32/api/winbase/nf-winbase-globalalloc) zuordnet und die Dekomprimierungsformatinformationen mithilfe des [**ICDecompressGetFormat-Makros**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformat) abruft.


```C++
LPBITMAPINFOHEADER lpbiIn, lpbiOut; 
 
// Assume *lpbiIn points to the input (compressed) format. 
dwFormatSize = ICDecompressGetFormatSize(hIC, lpbiIn); 
h = GlobalAlloc(GHND, dwFormatSize); 
lpbiOut = (LPBITMAPINFOHEADER)GlobalLock(h); 
ICDecompressGetFormat(hIC, lpbiIn, lpbiOut); 
 
```



Das folgende Beispiel zeigt, wie eine Anwendung das [**ICDecompressQuery-Makro**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery) verwenden kann, um zu bestimmen, ob ein Dekomprimierer die Eingabe- und Ausgabeformate verarbeiten kann.


```C++
LPBITMAPINFOHEADER lpbiIn, lpbiOut; 
// Assume *lpbiIn & *lpbiOut are initialized to the respective 
// formats.
 
if (ICDecompressQuery(hIC, lpbiIn, lpbiOut) == ICERR_OK)
{ 
    
    // Format is supported - use the decompressor. 
    
} 
 
```



Das folgende Codefragment zeigt, wie Sie die Paletteninformationen mithilfe des [**IcDecompressGetPalette-Makros**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetpalette) abrufen.


```C++
ICDecompressGetPalette(hIC, lpbiIn, lpbiOut); 
 
// Move up to the palette. 
lpPalette = (LPBYTE)lpbiOut + lpbi->biSize;
 
 
```



 

 