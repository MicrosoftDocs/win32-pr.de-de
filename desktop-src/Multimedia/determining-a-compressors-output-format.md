---
title: Bestimmen des Ausgabeformats eines 1.
description: Bestimmen des Ausgabeformats eines 1.
ms.assetid: 910bd77f-4c65-4ea2-bab2-96f42a2b6cf1
keywords:
- Videokomprimierungs-Manager (VCM), Ausgabeformat
- VCM (Videokomprimierungs-Manager), Ausgabeformat
- ICCompressGetFormat-Makro
- ICCompressQuery-Makro
- ICCompressGetSize-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4160942c2b5524e57a3a7d7e4eb79128abd55bf5f62ea0926c1ba60e02ce70c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117989000"
---
# <a name="determining-a-compressors-output-format"></a>Bestimmen des Ausgabeformats eines 1.

Im folgenden Beispiel wird das [**Größenmakro ICCompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformat) verwendet, um die Puffergröße zu bestimmen, die für die Daten erforderlich ist, die das Komprimierungsformat angeben, ordnet einen Puffer der entsprechenden Größe mithilfe der [GlobalAlloc-Funktion](/windows/win32/api/winbase/nf-winbase-globalalloc) zu und ruft die Informationen zum Komprimierungsformat mithilfe des **ICCompressGetFormat-Makros** ab.


```C++
LPBITMAPINFOHEADER   lpbiIn, lpbiOut; 
 
// *lpbiIn must be initialized to the input format. 
 
dwFormatSize = ICCompressGetFormatSize(hIC, lpbiIn); 
h = GlobalAlloc(GHND, dwFormatSize); 
lpbiOut = (LPBITMAPINFOHEADER)GlobalLock(h); 
ICCompressGetFormat(hIC, lpbiIn, lpbiOut); 
 
```



Im folgenden Beispiel wird das [**ICCompressQuery-Makro**](/windows/desktop/api/Vfw/nf-vfw-iccompressquery) verwendet, um zu bestimmen, ob eine Maske die Eingabe- und Ausgabeformate verarbeiten kann.


```C++
LPBITMAPINFOHEADER   lpbiIn, lpbiOut; 
 
// Both *lpbiIn and *lpbiOut must be initialized to the respective
// formats.
 

if (ICCompressQuery(hIC, lpbiIn, lpbiOut) == ICERR_OK)
{ 
 
    // Format is supported; use the compressor. 
 
}
 
 
```



Im folgenden Beispiel wird das [**MAKRO ICCompressGetSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize) verwendet, um die Puffergröße zu bestimmen, und es ordnet einen Puffer dieser Größe mit [globalalloc zu.](/windows/win32/api/winbase/nf-winbase-globalalloc)


```C++
// Find the worst-case buffer size. 
dwCompressBufferSize = ICCompressGetSize(hIC, lpbiIn, lpbiOut); 
 
// Allocate a buffer and get lpOutput to point to it. 
h = GlobalAlloc(GHND, dwCompressBufferSize); 
lpOutput = (LPVOID)GlobalLock(h);
 
 
```



 

 