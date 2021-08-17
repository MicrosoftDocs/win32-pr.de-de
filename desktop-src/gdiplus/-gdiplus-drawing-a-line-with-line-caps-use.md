---
description: Sie können den Anfang oder das Ende einer Linie in einer von mehreren Formen zeichnen, die als Linienende bezeichnet werden. Windows GDI+ unterstützt mehrere Linienoberungen, z. B. Runde, Quadrat, Raute und Pfeilspitze.
ms.assetid: c9d90114-3913-486c-a808-b08dd473d9a1
title: Zeichnen einer Linie mit Linienoberungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33e72e4e1c9c36a7233688378852dfda73196cd7e7131cf7def587ad29a70e82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117696162"
---
# <a name="drawing-a-line-with-line-caps"></a>Zeichnen einer Linie mit Linienoberungen

Sie können den Anfang oder das Ende einer Linie in einer von mehreren Formen zeichnen, die als Linienende bezeichnet werden. Windows GDI+ unterstützt mehrere Linienoberungen, z. B. Runde, Quadrat, Raute und Pfeilspitze.

Sie können Linienendes für den Anfang einer Zeile (Startende), das Ende einer Zeile (Endende) oder die Bindestriche einer gestrichelten Linie (Bindestrich) angeben.

Im folgenden Beispiel wird eine Linie mit einer Pfeilspitze an einem Ende und einem runden Ende am anderen Ende ge zeichnet:


```
Pen pen(Color(255, 0, 0, 255), 8);
stat = pen.SetStartCap(LineCapArrowAnchor);
stat = pen.SetEndCap(LineCapRoundAnchor);
stat = graphics.DrawLine(&pen, 20, 175, 300, 175);
```



Die folgende Abbildung zeigt die resultierende Zeile.

![Abbildung, die eine horizontale Linie mit einem Pfeil am linken Ende und einem Kreis am rechten Ende zeigt](images/pens4.png)

**LineCapArrowAnchor** und **LineCapRoundAnchor** sind Elemente der [**LineCap-Enumeration.**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-linecap)

 

 



