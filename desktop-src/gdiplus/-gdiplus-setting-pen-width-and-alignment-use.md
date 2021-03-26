---
description: Wenn Sie ein Pen-Objekt erstellen, können Sie die Stift Breite als eines der Argumente für den Konstruktor angeben. Sie können auch die Stift Breite mithilfe der Methode Pen::-Methode ändern.
ms.assetid: b529ba0b-1786-4925-88bd-1a8369fc368c
title: Festlegen der Stift Breite und-Ausrichtung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca59895cc73480b054302091342c8f8f4f410b34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104567349"
---
# <a name="setting-pen-width-and-alignment"></a>Festlegen der Stift Breite und-Ausrichtung

Wenn Sie ein [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) -Objekt erstellen, können Sie die Stift Breite als eines der Argumente für den Konstruktor angeben. Sie können auch die Stift Breite mithilfe der Methode [**Pen::**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setwidth) -Methode ändern.

Eine theoretische Linie weist eine Breite von 0 (null) auf. Wenn Sie eine Linie zeichnen, werden die Pixel auf der theoretischen Linie zentriert. Im folgenden Beispiel wird eine angegebene Zeile zweimal gezeichnet: einmal mit einem schwarzen Stift der Breite 1 und einmal mit einem grünen Stift der Breite 10.


```
Pen blackPen(Color(255, 0, 0, 0), 1);
Pen greenPen(Color(255, 0, 255, 0), 10);
stat = greenPen.SetAlignment(PenAlignmentCenter);

// Draw the line with the wide green pen.
stat = graphics.DrawLine(&greenPen, 10, 100, 100, 50);

// Draw the same line with the thin black pen.
stat = graphics.DrawLine(&blackPen, 10, 100, 100, 50);
```



Die folgende Abbildung zeigt die Ausgabe des vorangehenden Codes. Die grünen Pixel und die schwarzen Pixel werden auf der theoretischen Linie zentriert.

![Abbildung: eine schlanke, Diagonale, schwarze Linie, die durch eine Breite, grüne Linie umgeben ist ](images/pens1a.png)

Im folgenden Beispiel wird ein angegebenes Rechteck zweimal gezeichnet: einmal mit einem schwarzen Stift der Breite 1 und einmal mit einem grünen Stift der Breite 10. Der Code übergibt den Wert **penalignmentcenter** (ein Element der [**PenAlignment**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-penalignment) -Enumeration) an die [**Pen:: SetAlignment**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setalignment) -Methode, um anzugeben, dass die mit dem grünen Stift gezeichneten Pixel auf der Grenze des Rechtecks zentriert werden.


```
Pen blackPen(Color(255, 0, 0, 0), 1);
Pen greenPen(Color(255, 0, 255, 0), 10);
stat = greenPen.SetAlignment(PenAlignmentCenter);

// Draw the rectangle with the wide green pen.
stat = graphics.DrawRectangle(&greenPen, 10, 100, 50, 50);

// Draw the same rectangle with the thin black pen.
stat = graphics.DrawRectangle(&blackPen, 10, 100, 50, 50);
```



Die folgende Abbildung zeigt die Ausgabe des vorangehenden Codes. Die grünen Pixel werden auf das theoretische Rechteck zentriert, das durch die schwarzen Pixel dargestellt wird.

![Abbildung, die eine schlanke schwarze Linie in der Form eines Rechtecks anzeigt, das von einer breiteren grünen Linie umgeben ist](images/pens2.png)

Sie können die Ausrichtung des grünen Stifts ändern, indem Sie die dritte Anweisung im vorangehenden Beispiel wie folgt ändern:


```
stat = greenPen.SetAlignment(PenAlignmentInset);
```



Nun werden die Pixel in der Breite grünen Linie im Inneren des Rechtecks angezeigt, wie in der folgenden Abbildung dargestellt.

![die Abbildung zeigt eine schlanke schwarze Linie in der Form einer Rechnung, die eine breite grüne Linie derselben Form einschließt.](images/pens3.png)

 

 



