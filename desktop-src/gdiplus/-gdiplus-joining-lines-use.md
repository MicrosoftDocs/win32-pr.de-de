---
description: Ein Zeilen Beitritt ist der gemeinsame Bereich, der durch zwei Zeilen gebildet wird, deren enden sich überlappen.
ms.assetid: 4ec3e76a-2531-4869-a5b0-c595198e8345
title: Joinlinien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b2ab0bc53239b9a0d9327a26e25eed1c93c685b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104554421"
---
# <a name="joining-lines"></a>Joinlinien

Ein Zeilen Beitritt ist der gemeinsame Bereich, der durch zwei Zeilen gebildet wird, deren enden sich überlappen. Windows GDI+ bietet vier Zeilen Verknüpfungs Stile: Gehrungs, Abschrägung, Round und Gehrungs clipped. Der linienjoinstil ist eine Eigenschaft der [**Stift**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) -Klasse. Wenn Sie einen linienjoinstil für einen Stift angeben und diesen Stift zum Zeichnen eines Pfads verwenden, wird der angegebene joinstil auf alle verbundenen Zeilen im Pfad angewendet.

Sie können den linienjoinstil mithilfe der [**Pen:: setlinejoin**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) -Methode der [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) -Klasse angeben. Das folgende Beispiel veranschaulicht einen gevelten Zeilen Beitritt zwischen einer horizontalen Linie und einer vertikalen Linie:


```
GraphicsPath path;
Pen penJoin(Color(255, 0, 0, 255), 8);

path.StartFigure();
path.AddLine(Point(50, 200), Point(100, 200));
path.AddLine(Point(100, 200), Point(100, 250));

penJoin.SetLineJoin(LineJoinBevel);
graphics.DrawPath(&penJoin, &path);
```



In der folgenden Abbildung wird die resultierende Zeilen Verknüpfung dargestellt.

![Abbildung, die anzeigt, dass zwei Zeilen im rechten Winkel mit einem abgeschrägten Join angezeigt werden](images/pens5.png)

Im vorherigen Beispiel ist der Wert (**linejoinbevel**), der an die Methode [**Pen:: setlinejoin**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) übermittelt wurde, ein Element der [**LineJoin**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-linejoin) -Enumeration.

 

 



