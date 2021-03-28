---
description: Die beiden Anwendungs definierten Karten Modi (mm \_ ISOTROPIC und mm \_ anisotrope) werden für anwendungsspezifische Mapping-Modi bereitgestellt.
ms.assetid: c4c4e352-63fc-4e97-a218-a1b7deac02e8
title: Application-Defined-Karten Modi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d800a3ce631ebffeef8223fc53ec505c10cb69f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994135"
---
# <a name="application-defined-mapping-modes"></a><span data-ttu-id="3c2ec-103">Application-Defined-Karten Modi</span><span class="sxs-lookup"><span data-stu-id="3c2ec-103">Application-Defined Mapping Modes</span></span>

<span data-ttu-id="3c2ec-104">Die beiden Anwendungs definierten Karten Modi (mm \_ ISOTROPIC und mm \_ anisotrope) werden für anwendungsspezifische Mapping-Modi bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="3c2ec-104">The two application-defined mapping modes (MM\_ISOTROPIC and MM\_ANISOTROPIC) are provided for application-specific mapping modes.</span></span> <span data-ttu-id="3c2ec-105">Der \_ Modus "x-isotrope" gewährleistet, dass logische Einheiten in der x-Richtung und in der y-Richtung gleich sind, während der mm- \_ anisotrope Modus die Einheiten unterscheiden kann.</span><span class="sxs-lookup"><span data-stu-id="3c2ec-105">The MM\_ISOTROPIC mode guarantees that logical units in the x-direction and in the y-direction are equal, while the MM\_ANISOTROPIC mode allows the units to differ.</span></span> <span data-ttu-id="3c2ec-106">Eine CAD-oder Zeichnungsanwendung kann vom Modus für die x \_ -isotrope Zuordnung profitieren, muss jedoch möglicherweise logische Einheiten angeben, die den Inkrementen auf der Skala eines Technikers (1/64 Zoll) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="3c2ec-106">A CAD or drawing application can benefit from the MM\_ISOTROPIC mapping mode but may need to specify logical units that correspond to the increments on an engineer's scale (1/64 inch).</span></span> <span data-ttu-id="3c2ec-107">Diese Einheiten sind mit den vordefinierten Zustellungs Modi (mm \_ hienglish oder mm \_ HIMETRIC) schwer zu erreichen. Sie können jedoch problemlos abgerufen werden, indem Sie den Modus "x \_ isotrope" (oder "mm \_ anisotrope") auswählen.</span><span class="sxs-lookup"><span data-stu-id="3c2ec-107">These units would be difficult to obtain with the predefined mapping modes (MM\_HIENGLISH or MM\_HIMETRIC); however, they can easily be obtained by selecting the MM\_ISOTROPIC (or MM\_ANISOTROPIC) mode.</span></span> <span data-ttu-id="3c2ec-108">Im folgenden Beispiel wird gezeigt, wie logische Einheiten auf 1/64 Zoll festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="3c2ec-108">The following example shows how to set logical units to 1/64 inch:</span></span>


```C++
SetMapMode(hDC, MM_ISOTROPIC); 
SetWindowExtEx(hDC, 64, 64, NULL); 
SetViewportExtEx(hDC, GetDeviceCaps(hDC, LOGPIXELSX), 
                      GetDeviceCaps(hDC, LOGPIXELSY), NULL); 
```



 

 



