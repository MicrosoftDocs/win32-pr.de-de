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
# <a name="retrieving-the-capabilities-of-a-printer"></a>Abrufen der Funktionen eines Druckers

Nicht jedes Ausgabegerät unterstützt den gesamten Satz von Grafikfunktionen. Beispielsweise unterstützen die meisten Vektor Zeichnungs Blöcke aufgrund von Hardware Einschränkungen keine Bitblock Übertragungen. Eine Anwendung kann ermitteln, ob ein Gerät eine bestimmte Grafik Funktion unterstützt, indem Sie die [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) -Funktion aufrufen, den entsprechenden Index angibt und den Rückgabewert untersucht.

Das folgende Beispiel zeigt, wie eine Anwendung einen Drucker testet, um zu bestimmen, ob Bitblock Übertragungen unterstützt werden.


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



 

 



