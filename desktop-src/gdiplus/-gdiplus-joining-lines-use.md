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
# <a name="joining-lines"></a><span data-ttu-id="2955b-103">Joinlinien</span><span class="sxs-lookup"><span data-stu-id="2955b-103">Joining Lines</span></span>

<span data-ttu-id="2955b-104">Ein Zeilen Beitritt ist der gemeinsame Bereich, der durch zwei Zeilen gebildet wird, deren enden sich überlappen.</span><span class="sxs-lookup"><span data-stu-id="2955b-104">A line join is the common area that is formed by two lines whose ends meet or overlap.</span></span> <span data-ttu-id="2955b-105">Windows GDI+ bietet vier Zeilen Verknüpfungs Stile: Gehrungs, Abschrägung, Round und Gehrungs clipped.</span><span class="sxs-lookup"><span data-stu-id="2955b-105">Windows GDI+ provides four line join styles: miter, bevel, round, and miter clipped.</span></span> <span data-ttu-id="2955b-106">Der linienjoinstil ist eine Eigenschaft der [**Stift**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="2955b-106">Line join style is a property of the [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) class.</span></span> <span data-ttu-id="2955b-107">Wenn Sie einen linienjoinstil für einen Stift angeben und diesen Stift zum Zeichnen eines Pfads verwenden, wird der angegebene joinstil auf alle verbundenen Zeilen im Pfad angewendet.</span><span class="sxs-lookup"><span data-stu-id="2955b-107">When you specify a line join style for a pen and then use that pen to draw a path, the specified join style is applied to all the connected lines in the path.</span></span>

<span data-ttu-id="2955b-108">Sie können den linienjoinstil mithilfe der [**Pen:: setlinejoin**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) -Methode der [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) -Klasse angeben.</span><span class="sxs-lookup"><span data-stu-id="2955b-108">You can specify the line join style by using the [**Pen::SetLineJoin**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) method of the [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) class.</span></span> <span data-ttu-id="2955b-109">Das folgende Beispiel veranschaulicht einen gevelten Zeilen Beitritt zwischen einer horizontalen Linie und einer vertikalen Linie:</span><span class="sxs-lookup"><span data-stu-id="2955b-109">The following example demonstrates a beveled line join between a horizontal line and a vertical line:</span></span>


```
GraphicsPath path;
Pen penJoin(Color(255, 0, 0, 255), 8);

path.StartFigure();
path.AddLine(Point(50, 200), Point(100, 200));
path.AddLine(Point(100, 200), Point(100, 250));

penJoin.SetLineJoin(LineJoinBevel);
graphics.DrawPath(&penJoin, &path);
```



<span data-ttu-id="2955b-110">In der folgenden Abbildung wird die resultierende Zeilen Verknüpfung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="2955b-110">The following illustration shows the resulting beveled line join.</span></span>

![Abbildung, die anzeigt, dass zwei Zeilen im rechten Winkel mit einem abgeschrägten Join angezeigt werden](images/pens5.png)

<span data-ttu-id="2955b-112">Im vorherigen Beispiel ist der Wert (**linejoinbevel**), der an die Methode [**Pen:: setlinejoin**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) übermittelt wurde, ein Element der [**LineJoin**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-linejoin) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="2955b-112">In the preceding example, the value (**LineJoinBevel**) passed to the [**Pen::SetLineJoin**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) method is an element of the [**LineJoin**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-linejoin) enumeration.</span></span>

 

 



