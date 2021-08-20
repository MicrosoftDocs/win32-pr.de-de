---
description: Clipping umfasst das Einschränken des Zeichnens auf einen bestimmten Bereich. Die folgende Abbildung zeigt die Zeichenfolge &\# 0034; Hello&\# 0034; auf einen heartförmigen Bereich abgeschnitten.
ms.assetid: 58cc052d-31af-4410-81b9-defbad08a1dc
title: Clipping (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a57534c5934270374af356956285ad13838630666795d9f06a2623cbd3b453ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118067634"
---
# <a name="clipping-gdi"></a>Clipping (GDI+)

Clipping umfasst das Einschränken des Zeichnens auf einen bestimmten Bereich. Die folgende Abbildung zeigt die Zeichenfolge "Hello", die auf einen heartförmigen Bereich abgeschnitten ist.

![Abbildung mit Teilen der Zeichenfolge "hello" in einem roten Heart](images/aboutgdip02-art30.png)

Bereiche können aus Pfaden erstellt werden, und Pfade können die Konturen von Zeichenfolgen enthalten, sodass Sie umrissenen Text zum Ausschneiden verwenden können. Die folgende Abbildung zeigt eine Reihe von verketteten Ellipsen, die am Inneren einer Textzeichenfolge abgeschnitten sind.

![Abbildung der Zeichenfolge "hello", die durch ein Muster von konzentrischen Kreisen gefüllt ist](images/aboutgdip02-art31.png)

Erstellen Sie zum Zeichnen mit Clipping ein [**Graphics-Objekt,**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) rufen Sie dessen [SetClip-Methode](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode)) auf, und rufen Sie dann die Zeichnungsmethoden desselben **Grafikobjekts** auf. Im folgenden Beispiel wird eine Linie gezogen, die auf einen rechteckigen Bereich abgeschnitten wird.


```
Region myRegion(Rect(20, 30, 100, 50));
myGraphics.DrawRectangle(&myPen, 20, 30, 100, 50);  
myGraphics.SetClip(&myRegion, CombineModeReplace);
myGraphics.DrawLine(&myPen, 0, 0, 200, 200);
```



Die folgende Abbildung zeigt den rechteckigen Bereich zusammen mit der abgeschnittenen Linie.

![Abbildung eines Rechtecks mit einer diagonalen Linie von oben nach unten](images/aboutgdip02-art31a.png)

 

 



