---
description: Beim Clipping wird das Zeichnen auf eine bestimmte Region eingeschränkt. Die folgende Abbildung zeigt die Zeichenfolge &\# 0034; Hello&\# 0034; abgeschnitten auf einen herzförmigen Bereich.
ms.assetid: 58cc052d-31af-4410-81b9-defbad08a1dc
title: Clipping (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 156ae2209a3b7135cde2804103531eaf7b519d73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042111"
---
# <a name="clipping-gdi"></a><span data-ttu-id="08872-104">Clipping (GDI+)</span><span class="sxs-lookup"><span data-stu-id="08872-104">Clipping (GDI+)</span></span>

<span data-ttu-id="08872-105">Beim Clipping wird das Zeichnen auf eine bestimmte Region eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="08872-105">Clipping involves restricting drawing to a certain region.</span></span> <span data-ttu-id="08872-106">Die folgende Abbildung zeigt die Zeichenfolge "Hello", die auf einen herzförmigen Bereich zugeschnitten ist.</span><span class="sxs-lookup"><span data-stu-id="08872-106">The following illustration shows the string "Hello" clipped to a heart-shaped region.</span></span>

![Abbildung, die Teile der Zeichenfolge "Hello" innerhalb eines roten Herzens anzeigt](images/aboutgdip02-art30.png)

<span data-ttu-id="08872-108">Bereiche können aus Pfaden erstellt werden, und Pfade können die Gliederungen von Zeichen folgen enthalten, sodass Sie den Text für das Clipping verwenden können.</span><span class="sxs-lookup"><span data-stu-id="08872-108">Regions can be constructed from paths, and paths can contain the outlines of strings, so you can use outlined text for clipping.</span></span> <span data-ttu-id="08872-109">Die folgende Abbildung zeigt einen Satz konzentrischer Ellipsen, die auf das Innere einer Text Zeichenfolge zugeschnitten sind.</span><span class="sxs-lookup"><span data-stu-id="08872-109">The following illustration shows a set of concentric ellipses clipped to the interior of a string of text.</span></span>

![Abbildung zur Darstellung der Zeichenfolge "Hello", die durch ein Muster von konzentrischen Kreisen gefüllt ist](images/aboutgdip02-art31.png)

<span data-ttu-id="08872-111">Um mit Clipping zu zeichnen, erstellen Sie ein [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt, rufen Sie seine [SetClip](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode)) -Methode auf, und rufen Sie dann die Zeichnungs Methoden desselben **Grafik** Objekts auf.</span><span class="sxs-lookup"><span data-stu-id="08872-111">To draw with clipping, create a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object, call its [SetClip](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode)) method, and then call the drawing methods of that same **Graphics** object.</span></span> <span data-ttu-id="08872-112">Im folgenden Beispiel wird eine Linie gezeichnet, die auf einen rechteckigen Bereich zugeschnitten ist.</span><span class="sxs-lookup"><span data-stu-id="08872-112">The following example draws a line that is clipped to a rectangular region.</span></span>


```
Region myRegion(Rect(20, 30, 100, 50));
myGraphics.DrawRectangle(&myPen, 20, 30, 100, 50);  
myGraphics.SetClip(&myRegion, CombineModeReplace);
myGraphics.DrawLine(&myPen, 0, 0, 200, 200);
```



<span data-ttu-id="08872-113">In der folgenden Abbildung wird der rechteckige Bereich zusammen mit der ausgeschnittenen Linie dargestellt.</span><span class="sxs-lookup"><span data-stu-id="08872-113">The following illustration shows the rectangular region along with the clipped line.</span></span>

![Abbildung mit einem Rechteck, das eine diagonal Linie von oben nach unten anzeigt](images/aboutgdip02-art31a.png)

 

 



