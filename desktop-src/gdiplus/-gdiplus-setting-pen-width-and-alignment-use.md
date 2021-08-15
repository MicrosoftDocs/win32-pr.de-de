---
description: Wenn Sie ein Stiftobjekt erstellen, können Sie die Stiftbreite als eines der Argumente für den Konstruktor bereitstellen. Sie können die Stiftbreite auch mithilfe der Pen::SetWidth-Methode ändern.
ms.assetid: b529ba0b-1786-4925-88bd-1a8369fc368c
title: Festlegen der Stiftbreite und -ausrichtung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe2a6bd5be00fde0f27657cef558365d857775a5b55f9f108074884906916b8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117885013"
---
# <a name="setting-pen-width-and-alignment"></a>Festlegen der Stiftbreite und -ausrichtung

Wenn Sie ein [**Stiftobjekt**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) erstellen, können Sie die Stiftbreite als eines der Argumente für den Konstruktor bereitstellen. Sie können die Stiftbreite auch mithilfe der [**Pen::SetWidth-Methode**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setwidth) ändern.

Eine theoretische Linie hat eine Breite von 0 (null). Wenn Sie eine Linie zeichnen, werden die Pixel auf der theoretischen Linie zentriert. Im folgenden Beispiel wird eine angegebene Zeile zweimal zeichnet: einmal mit einem schwarzen Stift der Breite 1 und einmal mit einem grünen Stift der Breite 10.


```
Pen blackPen(Color(255, 0, 0, 0), 1);
Pen greenPen(Color(255, 0, 255, 0), 10);
stat = greenPen.SetAlignment(PenAlignmentCenter);

// Draw the line with the wide green pen.
stat = graphics.DrawLine(&greenPen, 10, 100, 100, 50);

// Draw the same line with the thin black pen.
stat = graphics.DrawLine(&blackPen, 10, 100, 100, 50);
```



Die folgende Abbildung zeigt die Ausgabe des vorangehenden Codes. Die grünen und schwarzen Pixel werden auf der theoretischen Linie zentriert.

![Abbildung, die eine schlanke, diagonale, schwarze Linie zeigt, die von einer breiten, grünen Linie umgeben ist ](images/pens1a.png)

Das folgende Beispiel zeichnet ein angegebenes Rechteck zweimal: einmal mit einem schwarzen Stift der Breite 1 und einmal mit einem grünen Stift der Breite 10. Der Code übergibt den Wert **PenAlignmentCenter** (ein Element der [**PenAlignment-Enumeration)**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-penalignment) an die [**Pen::SetAlignment-Methode,**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setalignment) um anzugeben, dass die mit dem grünen Stift gezeichneten Pixel an der Begrenzung des Rechtecks zentriert sind.


```
Pen blackPen(Color(255, 0, 0, 0), 1);
Pen greenPen(Color(255, 0, 255, 0), 10);
stat = greenPen.SetAlignment(PenAlignmentCenter);

// Draw the rectangle with the wide green pen.
stat = graphics.DrawRectangle(&greenPen, 10, 100, 50, 50);

// Draw the same rectangle with the thin black pen.
stat = graphics.DrawRectangle(&blackPen, 10, 100, 50, 50);
```



Die folgende Abbildung zeigt die Ausgabe des vorangehenden Codes. Die grünen Pixel werden auf dem theoretischen Rechteck zentriert, das durch die schwarzen Pixel dargestellt wird.

![Abbildung einer schlanken schwarzen Linie in Form eines Rechtecks, umschlossen von einer breiteren grünen Linie](images/pens2.png)

Sie können die Ausrichtung des grünen Stifts ändern, indem Sie die dritte Anweisung im vorherigen Beispiel wie folgt ändern:


```
stat = greenPen.SetAlignment(PenAlignmentInset);
```



Nun werden die Pixel in der breiten grünen Linie im Inneren des Rechtecks angezeigt, wie in der folgenden Abbildung dargestellt.

![Abbildung, die eine schlanke schwarze Linie in der Form einer Rectange zeigt, die eine breite grüne Linie der gleichen Form umschließt](images/pens3.png)

 

 



