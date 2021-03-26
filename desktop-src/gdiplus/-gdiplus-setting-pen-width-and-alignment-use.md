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
# <a name="setting-pen-width-and-alignment"></a><span data-ttu-id="513d1-104">Festlegen der Stift Breite und-Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="513d1-104">Setting Pen Width and Alignment</span></span>

<span data-ttu-id="513d1-105">Wenn Sie ein [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) -Objekt erstellen, können Sie die Stift Breite als eines der Argumente für den Konstruktor angeben.</span><span class="sxs-lookup"><span data-stu-id="513d1-105">When you create a [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) object, you can supply the pen width as one of the arguments to the constructor.</span></span> <span data-ttu-id="513d1-106">Sie können auch die Stift Breite mithilfe der Methode [**Pen::**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setwidth) -Methode ändern.</span><span class="sxs-lookup"><span data-stu-id="513d1-106">You can also change the pen width by using the [**Pen::SetWidth**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setwidth) method.</span></span>

<span data-ttu-id="513d1-107">Eine theoretische Linie weist eine Breite von 0 (null) auf.</span><span class="sxs-lookup"><span data-stu-id="513d1-107">A theoretical line has a width of zero.</span></span> <span data-ttu-id="513d1-108">Wenn Sie eine Linie zeichnen, werden die Pixel auf der theoretischen Linie zentriert.</span><span class="sxs-lookup"><span data-stu-id="513d1-108">When you draw a line, the pixels are centered on the theoretical line.</span></span> <span data-ttu-id="513d1-109">Im folgenden Beispiel wird eine angegebene Zeile zweimal gezeichnet: einmal mit einem schwarzen Stift der Breite 1 und einmal mit einem grünen Stift der Breite 10.</span><span class="sxs-lookup"><span data-stu-id="513d1-109">The following example draws a specified line twice: once with a black pen of width 1 and once with a green pen of width 10.</span></span>


```
Pen blackPen(Color(255, 0, 0, 0), 1);
Pen greenPen(Color(255, 0, 255, 0), 10);
stat = greenPen.SetAlignment(PenAlignmentCenter);

// Draw the line with the wide green pen.
stat = graphics.DrawLine(&greenPen, 10, 100, 100, 50);

// Draw the same line with the thin black pen.
stat = graphics.DrawLine(&blackPen, 10, 100, 100, 50);
```



<span data-ttu-id="513d1-110">Die folgende Abbildung zeigt die Ausgabe des vorangehenden Codes.</span><span class="sxs-lookup"><span data-stu-id="513d1-110">The following illustration shows the output of the preceding code.</span></span> <span data-ttu-id="513d1-111">Die grünen Pixel und die schwarzen Pixel werden auf der theoretischen Linie zentriert.</span><span class="sxs-lookup"><span data-stu-id="513d1-111">The green pixels and the black pixels are centered on the theoretical line.</span></span>

![<span data-ttu-id="513d1-112">Abbildung: eine schlanke, Diagonale, schwarze Linie, die durch eine Breite, grüne Linie umgeben ist</span><span class="sxs-lookup"><span data-stu-id="513d1-112">illustration showing a thin, diagonal, black line surrounded by a wide, green line</span></span> ](images/pens1a.png)

<span data-ttu-id="513d1-113">Im folgenden Beispiel wird ein angegebenes Rechteck zweimal gezeichnet: einmal mit einem schwarzen Stift der Breite 1 und einmal mit einem grünen Stift der Breite 10.</span><span class="sxs-lookup"><span data-stu-id="513d1-113">The following example draws a specified rectangle twice: once with a black pen of width 1 and once with a green pen of width 10.</span></span> <span data-ttu-id="513d1-114">Der Code übergibt den Wert **penalignmentcenter** (ein Element der [**PenAlignment**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-penalignment) -Enumeration) an die [**Pen:: SetAlignment**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setalignment) -Methode, um anzugeben, dass die mit dem grünen Stift gezeichneten Pixel auf der Grenze des Rechtecks zentriert werden.</span><span class="sxs-lookup"><span data-stu-id="513d1-114">The code passes the value **PenAlignmentCenter** (an element of the [**PenAlignment**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-penalignment) enumeration) to the [**Pen::SetAlignment**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setalignment) method to specify that the pixels drawn with the green pen are centered on the boundary of the rectangle.</span></span>


```
Pen blackPen(Color(255, 0, 0, 0), 1);
Pen greenPen(Color(255, 0, 255, 0), 10);
stat = greenPen.SetAlignment(PenAlignmentCenter);

// Draw the rectangle with the wide green pen.
stat = graphics.DrawRectangle(&greenPen, 10, 100, 50, 50);

// Draw the same rectangle with the thin black pen.
stat = graphics.DrawRectangle(&blackPen, 10, 100, 50, 50);
```



<span data-ttu-id="513d1-115">Die folgende Abbildung zeigt die Ausgabe des vorangehenden Codes.</span><span class="sxs-lookup"><span data-stu-id="513d1-115">The following illustration shows the output of the preceding code.</span></span> <span data-ttu-id="513d1-116">Die grünen Pixel werden auf das theoretische Rechteck zentriert, das durch die schwarzen Pixel dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="513d1-116">The green pixels are centered on the theoretical rectangle, which is represented by the black pixels.</span></span>

![Abbildung, die eine schlanke schwarze Linie in der Form eines Rechtecks anzeigt, das von einer breiteren grünen Linie umgeben ist](images/pens2.png)

<span data-ttu-id="513d1-118">Sie können die Ausrichtung des grünen Stifts ändern, indem Sie die dritte Anweisung im vorangehenden Beispiel wie folgt ändern:</span><span class="sxs-lookup"><span data-stu-id="513d1-118">You can change the green pen's alignment by modifying the third statement in the preceding example as follows:</span></span>


```
stat = greenPen.SetAlignment(PenAlignmentInset);
```



<span data-ttu-id="513d1-119">Nun werden die Pixel in der Breite grünen Linie im Inneren des Rechtecks angezeigt, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="513d1-119">Now the pixels in the wide green line appear on the inside of the rectangle as shown in the following illustration.</span></span>

![die Abbildung zeigt eine schlanke schwarze Linie in der Form einer Rechnung, die eine breite grüne Linie derselben Form einschließt.](images/pens3.png)

 

 



