---
description: Sie können den Anfang oder das Ende einer Linie in einer von mehreren Formen zeichnen, die als Linien Caps bezeichnet werden. Windows GDI+ unterstützt mehrere Linien Kappen, z. b. Round, Square, Diamond und Arrowhead.
ms.assetid: c9d90114-3913-486c-a808-b08dd473d9a1
title: Zeichnen einer Linie mit Linien Deckeln
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50ee4dd12a3068fe5200e0f1ae786765170ccba7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104987688"
---
# <a name="drawing-a-line-with-line-caps"></a>Zeichnen einer Linie mit Linien Deckeln

Sie können den Anfang oder das Ende einer Linie in einer von mehreren Formen zeichnen, die als Linien Caps bezeichnet werden. Windows GDI+ unterstützt mehrere Linien Kappen, z. b. Round, Square, Diamond und Arrowhead.

Sie können für den Anfang einer Linie (Start-Obergrenze), das Ende einer Linie (Ende) oder die Bindestriche einer gestrichelten Linie (Bindestrich) Zeilenenden angeben.

Im folgenden Beispiel wird eine Linie mit einem Pfeilspitzen an einem Ende und einem Rundenende am anderen Ende gezeichnet:


```
Pen pen(Color(255, 0, 0, 255), 8);
stat = pen.SetStartCap(LineCapArrowAnchor);
stat = pen.SetEndCap(LineCapRoundAnchor);
stat = graphics.DrawLine(&pen, 20, 175, 300, 175);
```



Die folgende Abbildung zeigt die resultierende Zeile.

![Abbildung, die eine horizontale Linie mit einem Pfeil am linken Ende und einem Kreis am rechten Ende zeigt](images/pens4.png)

**Linecaparrowanchor** und **linecaproundanchor** sind Elemente der [**LineCap**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-linecap) -Enumeration.

 

 



