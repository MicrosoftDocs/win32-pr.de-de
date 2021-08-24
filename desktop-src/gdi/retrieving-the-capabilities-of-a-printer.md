---
description: Nicht jedes Ausgabegerät unterstützt den gesamten Satz von Grafikfunktionen.
ms.assetid: 7989d393-7be4-47fc-af8d-26dd549c48be
title: Abrufen der Funktionen eines Druckers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c332832efc62f28ee77a5476ef12f706eb2e97a2cd5e86877e4a71a48feb907
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779060"
---
# <a name="retrieving-the-capabilities-of-a-printer"></a>Abrufen der Funktionen eines Druckers

Nicht jedes Ausgabegerät unterstützt den gesamten Satz von Grafikfunktionen. Beispielsweise unterstützen die meisten Vektorplotierer aufgrund von Hardwareeinschränkungen keine Bitblockübertragungen. Eine Anwendung kann ermitteln, ob ein Gerät eine bestimmte Grafikfunktion unterstützt, indem sie die [**GetDeviceCaps-Funktion aufruft,**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) den entsprechenden Index angibt und den Rückgabewert untersucht.

Das folgende Beispiel zeigt, wie eine Anwendung einen Drucker testet, um zu bestimmen, ob er Bitblockübertragungen unterstützt.


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



 

 



