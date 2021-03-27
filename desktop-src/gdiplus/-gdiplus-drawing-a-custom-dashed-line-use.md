---
description: Windows GDI+ bietet mehrere Dash-Stile, die in der Enumeration des Dashboards aufgelistet sind. Wenn diese standardmäßigen Dash-Stile nicht Ihren Anforderungen entsprechen, können Sie ein benutzerdefiniertes Bindestrich Muster erstellen.
ms.assetid: 0e75de3b-1006-4c8f-875c-eeb0782f24b0
title: Zeichnen einer benutzerdefinierten gestrichelten Linie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e108dcd6b32a47befcdd99d1f23e90c33d08446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988035"
---
# <a name="drawing-a-custom-dashed-line"></a>Zeichnen einer benutzerdefinierten gestrichelten Linie

Windows GDI+ bietet mehrere Dash-Stile, die in der Enumeration des [**Dashboards**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-dashstyle) aufgelistet sind. Wenn diese standardmäßigen Dash-Stile nicht Ihren Anforderungen entsprechen, können Sie ein benutzerdefiniertes Bindestrich Muster erstellen.

Fügen Sie zum Zeichnen einer benutzerdefinierten gestrichelten Linie die Längen der Bindestriche und Leerzeichen in ein Array ein, und übergeben Sie die Adresse des Arrays als Argument an die Methode [**Pen:: setdashpattern**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setdashpattern) eines [**Stift**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) Objekts. Im folgenden Beispiel wird eine benutzerdefinierte gestrichelte Linie basierend auf dem Array {5, 2, 15, 4} gezeichnet. Wenn Sie die Elemente des Arrays mit der Stift Breite 5 multiplizieren, erhalten Sie {25, 10, 75, 20}. Die angezeigten Bindestriche wechseln in eine Länge zwischen 25 und 75 und die Leerzeichen sind in der Länge zwischen 10 und 20.


```
REAL dashValues[4] = {5, 2, 15, 4};
Pen blackPen(Color(255, 0, 0, 0), 5);
blackPen.SetDashPattern(dashValues, 4);
stat = graphics.DrawLine(&blackPen, Point(5, 5), Point(405, 5));
```



In der folgenden Abbildung ist die resultierende gestrichelte Linie dargestellt. Beachten Sie, dass der abschließende Bindestrich kürzer als 25 Einheiten sein muss, damit die Zeile auf (405, 5) enden kann.

![Abbildung mit einer gestrichelten Linie jedes Segment ist eine kurze Zeile gefolgt von einem langen.](images/pens6.png)

 

 



