---
description: Windows GDI+ stellt mehrere Bindestrichstile zur Liste der DashStyle-Enumerationen. Wenn diese standardmäßigen Bindestrichstile nicht Ihren Anforderungen entsprechen, können Sie ein benutzerdefiniertes Bindestrichmuster erstellen.
ms.assetid: 0e75de3b-1006-4c8f-875c-eeb0782f24b0
title: Zeichnen einer benutzerdefinierten gestrichelten Linie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aad7bb415ff4f7b1cbde4637ab184c9ab05e4a707e0bce8328500d39ee2b840d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120115080"
---
# <a name="drawing-a-custom-dashed-line"></a>Zeichnen einer benutzerdefinierten gestrichelten Linie

Windows GDI+ stellt mehrere Bindestrichstile zur Liste der [**DashStyle-Enumerationen.**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-dashstyle) Wenn diese standardmäßigen Bindestrichstile nicht Ihren Anforderungen entsprechen, können Sie ein benutzerdefiniertes Bindestrichmuster erstellen.

Um eine benutzerdefinierte gestrichelte Linie zu zeichnen, legen Sie die Längen der Bindestriche und Leerzeichen in einem Array ab und übergeben die Adresse des Arrays als Argument an die [**Pen::SetDashPattern-Methode**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setdashpattern) eines [**Stiftobjekts.**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) Im folgenden Beispiel wird eine benutzerdefinierte gestrichelte Linie basierend auf dem Array {5, 2, 15, 4} ge zeichnet. Wenn Sie die Elemente des Arrays mit der Stiftbreite von 5 multiplizieren, erhalten Sie {25, 10, 75, 20}. Die angezeigten Bindestriche liegen zwischen 25 und 75 und die Länge der Leerzeichen zwischen 10 und 20.


```
REAL dashValues[4] = {5, 2, 15, 4};
Pen blackPen(Color(255, 0, 0, 0), 5);
blackPen.SetDashPattern(dashValues, 4);
stat = graphics.DrawLine(&blackPen, Point(5, 5), Point(405, 5));
```



Die folgende Abbildung zeigt die resultierende gestrichelte Linie. Beachten Sie, dass der letzte Bindestrich kürzer als 25 Einheiten sein muss, damit die Linie bei (405, 5) enden kann.

![Abbildung, die eine gestrichelte Linie zeigt; Jedes Segment ist eine kurze Zeile gefolgt von einer langen.](images/pens6.png)

 

 



