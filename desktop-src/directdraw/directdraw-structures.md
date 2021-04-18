---
title: DirectDraw-Strukturen
description: Dieser Abschnitt enthält Informationen zu den folgenden in DirectDraw verwendeten Strukturen.
ms.assetid: 36424B41-B179-414A-ACFF-E63DA7B27043
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52cf24c71da3f022833c6ecf9843e996df2c514b
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "106340743"
---
# <a name="directdraw-structures"></a>DirectDraw-Strukturen

Dieser Abschnitt enthält Informationen zu den folgenden Strukturen, die mit DirectDraw verwendet werden:

-   [**Ddbltbatch**](/windows/desktop/api/Ddraw/ns-ddraw-ddbltbatch)
-   [**Ddbltfx**](/windows/desktop/api/Ddraw/ns-ddraw-ddbltfx)
-   [**Ddcaps**](/windows/desktop/api/Ddraw/ns-ddraw-ddcaps_dx3)
-   [**Ddcolorcontrol**](/windows/win32/api/ddraw/nn-ddraw-idirectdrawcolorcontrol)
-   [**Ddcolorkey**](/windows/desktop/api/Ddraw/ns-ddraw-ddcolorkey)
-   [**DDDEVICEIDENTIFIER2**](/windows/win32/api/ddraw/ns-ddraw-dddeviceidentifier2)
-   [**Ddgammaramp**](/windows/desktop/api/Ddraw/ns-ddraw-ddgammaramp)
-   [**Ddoverlayfx**](/windows/desktop/api/Ddraw/ns-ddraw-ddoverlayfx)
-   [**Ddpixelformat**](/windows/desktop/api/Ddraw/ns-ddraw-ddpixelformat)
-   [**DDSCAPS**](/previous-versions/ms783271(v=vs.85))
-   [**DDSCAPS2**](/previous-versions/bb943980(v=vs.85))
-   [**Ddsurfacede SC**](/previous-versions/ms783272(v=vs.85))
-   [**DDSURFACEDESC2**](/previous-versions/bb943981(v=vs.85))

> [!Note]  
> Sie sollten den Arbeitsspeicher für jede DirectX-Struktur mit 0 initialisieren, bevor Sie die-Struktur verwenden. Außerdem sollten Sie für alle Strukturen, die ein **dwSize** -Element enthalten, den-Member auf die Größe der-Struktur in Bytes festlegen, bevor die-Struktur verwendet wird. Im folgenden Beispiel werden diese Aufgaben für eine gemeinsame Struktur, [**ddcaps**](/windows/desktop/api/Ddraw/ns-ddraw-ddcaps_dx3), ausgeführt:

 


```
DDCAPS ddcaps; // You cannot use this yet.
 
ZeroMemory(&ddcaps, sizeof(DDCAPS));
ddcaps.dwSize = sizeof(DDCAPS);
 
// Now you can use the structure.
.
.
```



 

 




