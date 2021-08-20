---
description: Eine Linienverknappung ist der allgemeine Bereich, der aus zwei Linien besteht, deren Enden sich überschneiden oder überlappen.
ms.assetid: 4ec3e76a-2531-4869-a5b0-c595198e8345
title: Verbinden von Linien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2aa93eac405bd77f6d87b2a8b86edc8a4043a57de3e4c4d5f31fb45acecc955
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118066974"
---
# <a name="joining-lines"></a>Verbinden von Linien

Eine Linienverknappung ist der allgemeine Bereich, der aus zwei Linien besteht, deren Enden sich überschneiden oder überlappen. Windows GDI+ bietet vier Linien join-Stile: miter, bevel, round und miter clipped. Der Linien join-Stil ist eine Eigenschaft der [**Pen-Klasse.**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) Wenn Sie einen Linien join-Stil für einen Stift angeben und diesen dann verwenden, um einen Pfad zu zeichnen, wird der angegebene Joinstil auf alle verbundenen Linien im Pfad angewendet.

Sie können den Linienjoinstil mithilfe der [**Pen::SetLineJoin-Methode**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) der [**Pen-Klasse**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) angeben. Im folgenden Beispiel wird eine abschrägte Linienlinie zwischen einer horizontalen und einer vertikalen Linie veranschaulicht:


```
GraphicsPath path;
Pen penJoin(Color(255, 0, 0, 255), 8);

path.StartFigure();
path.AddLine(Point(50, 200), Point(100, 200));
path.AddLine(Point(100, 200), Point(100, 250));

penJoin.SetLineJoin(LineJoinBevel);
graphics.DrawPath(&penJoin, &path);
```



Die folgende Abbildung zeigt die resultierende abschrägte Zeilenumknung.

![Abbildung, die zwei Linien zeigt, die sich im rechten Winkel mit einem geschwenkten Join treffen](images/pens5.png)

Im vorherigen Beispiel ist der Wert (**LineJoinBevel**), der an die [**Pen::SetLineJoin-Methode**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) übergeben wird, ein Element der [**LineJoin-Enumeration.**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-linejoin)

 

 



