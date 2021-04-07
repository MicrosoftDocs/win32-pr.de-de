---
title: Verwenden des Path-Elements
description: Verwenden des Path-Elements
ms.assetid: fd7924e7-f94f-4bc9-aa45-02cf8f9bac9b
keywords:
- Webworkshop, Pfad Element
- Entwerfen von Webseiten, Path-Element
- Vector Markup Language (VML), Pfad Element
- VML (Vector Markup Language), Pfad Element
- Vektorgrafiken, Pfad Element
- Path-Element
- VML-Elemente, Pfad
- VML-Formen, Pfad Element
- Vector Markup Language (VML), Anpassen von Form umrissen
- VML (Vector Markup Language), Anpassen von Form umrissen
- Vektorgrafiken, Anpassen von Form umrissen
- VML-Formen, Anpassen von umrissen
- Anpassen von Form umrissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba82d0ab946ef8937b68b4934f9c4d928bd25225
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729752"
---
# <a name="using-the-path-element"></a><span data-ttu-id="87918-116">Verwenden des Path-Elements</span><span class="sxs-lookup"><span data-stu-id="87918-116">Using the Path Element</span></span>

<span data-ttu-id="87918-117">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="87918-117">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="87918-118">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="87918-118">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="87918-119">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="87918-119">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="87918-120">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="87918-120">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="87918-121">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="87918-121">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="87918-122">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="87918-122">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="87918-123">Sie haben gelernt, dass Sie die vordefinierten VML-Shape-Elemente, wie z `<oval>` . b., `<line>` ,, `<polyline>` `<curve>` , `<rect>` , `<roundrect>` und--verwenden können `<arc>` , um eine Form zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="87918-123">You've learned that you can use the VML predefined shape elements -- such as `<oval>` , `<line>`, `<polyline>`, `<curve>`, `<rect>`, `<roundrect>`, and `<arc>` -- to draw a shape.</span></span> <span data-ttu-id="87918-124">In diesem Thema wird veranschaulicht, wie das `<path>` -Unterelement verwendet wird, um die Kontur einer Form anzupassen.</span><span class="sxs-lookup"><span data-stu-id="87918-124">In this topic, we will illustrate how to use the `<path>` sub-element to customize the outline of a shape.</span></span>

<span data-ttu-id="87918-125">Sie können das `<path>` untergeordnete Element innerhalb des- `<shape>` Elements oder des- `<shapetype>` Elements platzieren.</span><span class="sxs-lookup"><span data-stu-id="87918-125">You can place the `<path>` sub-element inside the `<shape>` or `<shapetype>` element.</span></span> <span data-ttu-id="87918-126">Anschließend können Sie die Eigenschafts Attribute des `<path>` unter Elements verwenden, um die Kontur der Form anzupassen.</span><span class="sxs-lookup"><span data-stu-id="87918-126">You can then use the property attributes of the `<path>` sub-element to customize the outline of the shape.</span></span>

<span data-ttu-id="87918-127">Um z. b. die in der folgenden Abbildung gezeigte angepasste Form zu zeichnen, können Sie mit dem `<path>` -Unterelement die Gliederung der Form definieren, wie in der folgenden VML-Darstellung dargestellt:</span><span class="sxs-lookup"><span data-stu-id="87918-127">For example, to draw the customized shape illustrated in the following picture, you can use the `<path>` sub-element to define the outline of the shape, as shown in the following VML representation:</span></span>

![shape1.gif (1301 Bytes)](images/shape1p.gif)


```HTML
<body>
<v:shape style='width:250;height:250' strokecolor="red" strokeweight="1.5pt"
fillcolor="blue" coordorigin="0 0" coordsize="200 200">
<v:path v="m 8,65 l 72,65, 92,11, 112,65, 174,65, 122,100, 142,155,
92,121, 42,155, 60,100 x e"/>
</v:shape>
</body>
```





-   <span data-ttu-id="87918-129">Die Werte `m 8,65` geben an, dass die Zeichnung am Punkt (8, 65) beginnt.</span><span class="sxs-lookup"><span data-stu-id="87918-129">The values `m 8,65` indicate that the drawing starts at the point (8,65).</span></span>
-   <span data-ttu-id="87918-130">Die Werte `l 72,65, 92,11, 112,65, 174,65, 122,100, 142,155, 92,121, 42,155, 60,100` geben an, dass eine gerade Linie an der aktuellen Stelle beginnt (8, 65) und am angegebenen Punkt (72, 65) endet, der zum neuen aktuellen Punkt wird.</span><span class="sxs-lookup"><span data-stu-id="87918-130">The values `l 72,65, 92,11, 112,65, 174,65, 122,100, 142,155, 92,121, 42,155, 60,100` indicate that a straight line begins at the current point (8, 65) and ends at the given point (72, 65), which becomes the new current point.</span></span> <span data-ttu-id="87918-131">Eine neue Zeile beginnt am aktuellen Punkt (72, 65) und endet am angegebenen Punkt, der zum neuen aktuellen Punkt wird usw., bis zum letzten Punkt (60, 100).</span><span class="sxs-lookup"><span data-stu-id="87918-131">A new line begins at the current point (72, 65) and ends at the given point, which becomes the new current point, and so on, to the final point (60, 100).</span></span>
-   <span data-ttu-id="87918-132">`x` Gibt an, dass der Pfad mit einer geraden Linie geschlossen wird, die am aktuellen Punkt (60, 100) beginnt und am ursprünglichen Punkt endet (8, 65).</span><span class="sxs-lookup"><span data-stu-id="87918-132">`x` indicates that the path will close by a straight line that starts at the current point (60, 100) and ends at the original point (8, 65).</span></span>
-   <span data-ttu-id="87918-133">`e` Gibt die Zeichnung zum Ende an.</span><span class="sxs-lookup"><span data-stu-id="87918-133">`e` indicates stop drawing.</span></span>

<span data-ttu-id="87918-134">Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation](https://www.w3.org/TR/NOTE-VML#-toc416858391) .</span><span class="sxs-lookup"><span data-stu-id="87918-134">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858391) .</span></span>

 

 