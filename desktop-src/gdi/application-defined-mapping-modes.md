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
# <a name="application-defined-mapping-modes"></a>Application-Defined-Karten Modi

Die beiden Anwendungs definierten Karten Modi (mm \_ ISOTROPIC und mm \_ anisotrope) werden für anwendungsspezifische Mapping-Modi bereitgestellt. Der \_ Modus "x-isotrope" gewährleistet, dass logische Einheiten in der x-Richtung und in der y-Richtung gleich sind, während der mm- \_ anisotrope Modus die Einheiten unterscheiden kann. Eine CAD-oder Zeichnungsanwendung kann vom Modus für die x \_ -isotrope Zuordnung profitieren, muss jedoch möglicherweise logische Einheiten angeben, die den Inkrementen auf der Skala eines Technikers (1/64 Zoll) entsprechen. Diese Einheiten sind mit den vordefinierten Zustellungs Modi (mm \_ hienglish oder mm \_ HIMETRIC) schwer zu erreichen. Sie können jedoch problemlos abgerufen werden, indem Sie den Modus "x \_ isotrope" (oder "mm \_ anisotrope") auswählen. Im folgenden Beispiel wird gezeigt, wie logische Einheiten auf 1/64 Zoll festgelegt werden:


```C++
SetMapMode(hDC, MM_ISOTROPIC); 
SetWindowExtEx(hDC, 64, 64, NULL); 
SetViewportExtEx(hDC, GetDeviceCaps(hDC, LOGPIXELSX), 
                      GetDeviceCaps(hDC, LOGPIXELSY), NULL); 
```



 

 



