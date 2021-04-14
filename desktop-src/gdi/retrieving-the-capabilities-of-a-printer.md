---
description: Nicht jedes Ausgabegerät unterstützt den gesamten Satz von Grafikfunktionen.
ms.assetid: 7989d393-7be4-47fc-af8d-26dd549c48be
title: Abrufen der Funktionen eines Druckers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29d84db8d46255f4dfd33ce62ab4ab6735b0f2a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978297"
---
# <a name="retrieving-the-capabilities-of-a-printer"></a><span data-ttu-id="3c36e-103">Abrufen der Funktionen eines Druckers</span><span class="sxs-lookup"><span data-stu-id="3c36e-103">Retrieving the Capabilities of a Printer</span></span>

<span data-ttu-id="3c36e-104">Nicht jedes Ausgabegerät unterstützt den gesamten Satz von Grafikfunktionen.</span><span class="sxs-lookup"><span data-stu-id="3c36e-104">Not every output device supports the entire set of graphics functions.</span></span> <span data-ttu-id="3c36e-105">Beispielsweise unterstützen die meisten Vektor Zeichnungs Blöcke aufgrund von Hardware Einschränkungen keine Bitblock Übertragungen.</span><span class="sxs-lookup"><span data-stu-id="3c36e-105">For example, because of hardware limitations, most vector plotters do not support bit-block transfers.</span></span> <span data-ttu-id="3c36e-106">Eine Anwendung kann ermitteln, ob ein Gerät eine bestimmte Grafik Funktion unterstützt, indem Sie die [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) -Funktion aufrufen, den entsprechenden Index angibt und den Rückgabewert untersucht.</span><span class="sxs-lookup"><span data-stu-id="3c36e-106">An application can determine whether a device supports a particular graphics function by calling the [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) function, specifying the appropriate index, and examining the return value.</span></span>

<span data-ttu-id="3c36e-107">Das folgende Beispiel zeigt, wie eine Anwendung einen Drucker testet, um zu bestimmen, ob Bitblock Übertragungen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="3c36e-107">The following example shows how an application tests a printer to determine whether it supports bit-block transfers.</span></span>


```C++
// Examine the raster capabilities of the device  
// identified by hdcPrint to verify that it supports  
// the BitBlt function.  
 
if ((GetDeviceCaps(hdcPrint, RASTERCAPS) 
       & RC_BITBLT) == 0) 
{ 
   DeleteDC(hdcPrint); 
   break; 
} 

else 
{ 
    // Print the bitmap using the printer DC.  
}
```



 

 



