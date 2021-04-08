---
title: Bestimmen des Ausgabeformats eines Kompressors
description: Bestimmen des Ausgabeformats eines Kompressors
ms.assetid: 910bd77f-4c65-4ea2-bab2-96f42a2b6cf1
keywords:
- Videokomprimierungs-Manager (VCM), Ausgabeformat
- VCM (Videokomprimierungs-Manager), Ausgabeformat
- Iccompressgetformat-Makro
- Iccompressquery-Makro
- Iccompressgetsize-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c4356870598dc08ad84c4073be5ffa3c2ddbd5b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101631"
---
# <a name="determining-a-compressors-output-format"></a><span data-ttu-id="cbed7-108">Bestimmen des Ausgabeformats eines Kompressors</span><span class="sxs-lookup"><span data-stu-id="cbed7-108">Determining a Compressor's Output Format</span></span>

<span data-ttu-id="cbed7-109">Im folgenden Beispiel wird das [**iccompressgetformat**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformat) size-Makro verwendet, um die für die Daten, die das Komprimierungs Format angeben, benötigte Puffergröße zu ermitteln, einen Puffer der entsprechenden Größe mithilfe der [globalzuordc](/windows/win32/api/winbase/nf-winbase-globalalloc) -Funktion zuzuordnen und die Informationen zum Komprimierungs Format mithilfe des **iccompressgetformat** -Makros abzurufen.</span><span class="sxs-lookup"><span data-stu-id="cbed7-109">The following example uses the [**ICCompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformat) size macro to determine the buffer size needed for the data specifying the compression format, allocates a buffer of the appropriate size using the [GlobalAlloc](/windows/win32/api/winbase/nf-winbase-globalalloc) function, and retrieves the compression format information using the **ICCompressGetFormat** macro.</span></span>


```C++
LPBITMAPINFOHEADER   lpbiIn, lpbiOut; 
 
// *lpbiIn must be initialized to the input format. 
 
dwFormatSize = ICCompressGetFormatSize(hIC, lpbiIn); 
h = GlobalAlloc(GHND, dwFormatSize); 
lpbiOut = (LPBITMAPINFOHEADER)GlobalLock(h); 
ICCompressGetFormat(hIC, lpbiIn, lpbiOut); 
 
```



<span data-ttu-id="cbed7-110">Im folgenden Beispiel wird das [**iccompressquery**](/windows/desktop/api/Vfw/nf-vfw-iccompressquery) -Makro verwendet, um zu bestimmen, ob ein-Kompressor die Eingabe-und Ausgabeformate verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="cbed7-110">The following example uses the [**ICCompressQuery**](/windows/desktop/api/Vfw/nf-vfw-iccompressquery) macro to determine whether a compressor can handle the input and output formats.</span></span>


```C++
LPBITMAPINFOHEADER   lpbiIn, lpbiOut; 
 
// Both *lpbiIn and *lpbiOut must be initialized to the respective
// formats.
 

if (ICCompressQuery(hIC, lpbiIn, lpbiOut) == ICERR_OK)
{ 
 
    // Format is supported; use the compressor. 
 
}
 
 
```



<span data-ttu-id="cbed7-111">Im folgenden Beispiel wird das [**iccompressgetsize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize) -Makro zum Ermitteln der Puffergröße verwendet, und es wird ein Puffer dieser Größe mithilfe von [Globalzuweisung](/windows/win32/api/winbase/nf-winbase-globalalloc)zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="cbed7-111">The following example uses the [**ICCompressGetSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize) macro to determine the buffer size, and it allocates a buffer of that size using [GlobalAlloc](/windows/win32/api/winbase/nf-winbase-globalalloc).</span></span>


```C++
// Find the worst-case buffer size. 
dwCompressBufferSize = ICCompressGetSize(hIC, lpbiIn, lpbiOut); 
 
// Allocate a buffer and get lpOutput to point to it. 
h = GlobalAlloc(GHND, dwCompressBufferSize); 
lpOutput = (LPVOID)GlobalLock(h);
 
 
```



 

 