---
title: Farbformen
description: In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.
ms.assetid: f528f0c7-1351-4bca-b309-67511431b711
keywords:
- Webworkshop, Farbformen
- Entwerfen von Webseiten, Farbformen
- Vector Markup Language (VML), Farbformen
- VML (Vector Markup Language), Farbformen
- Vektorgrafiken, Farbformen
- VML-Formen, Farben
- Farbformen
- Vector Markup Language (VML), Schlüsselwort Farben Namen
- VML (Vector Markup Language), Name der Schlüsselwort Farbe
- Vektorgrafiken, Schlüsselwort Farben Namen
- Farbnamen für Schlüsselwort
- Vector Markup Language (VML), RGB-dreier
- VML (Vector Markup Language), RGB-drei
- Vektorgrafiken, RGB-dreier
- RGB-dreier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1257c5f5b0cf8021658820f09de6e87099f0a52b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039293"
---
# <a name="coloring-shapes"></a><span data-ttu-id="d62ed-119">Farbformen</span><span class="sxs-lookup"><span data-stu-id="d62ed-119">Coloring Shapes</span></span>

<span data-ttu-id="d62ed-120">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="d62ed-120">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d62ed-121">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="d62ed-121">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d62ed-122">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="d62ed-122">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d62ed-123">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="d62ed-123">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d62ed-124">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="d62ed-124">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d62ed-125">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="d62ed-125">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d62ed-126">Wie in den vorherigen Abschnitten erwähnt, können Sie "Red" verwenden, um eine Farbe in rot darzustellen, "blau", um eine Farbe in blau darzustellen usw.</span><span class="sxs-lookup"><span data-stu-id="d62ed-126">As we mentioned in earlier sections, you can use "red" to represent a color in red, "blue" to represent a color in blue, and so on.</span></span> <span data-ttu-id="d62ed-127">In diesem Thema wird veranschaulicht, wie Formen in einer beliebigen Farbe gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="d62ed-127">In this topic, we will illustrate how to draw shapes in any color you want.</span></span>

<span data-ttu-id="d62ed-128">VML erweitert die HTML-und CSS-Farb Syntax.</span><span class="sxs-lookup"><span data-stu-id="d62ed-128">VML extends HTML and CSS color syntax.</span></span> <span data-ttu-id="d62ed-129">Wenn der Attributtyp eines VML-Elements Farben ist (z. b. **FillColor** und **strokeColor** ), können Sie die Farbe entweder mithilfe eines [Schlüssel Worts-Farbnamens](#keyword-color-name) oder eines [RGB-Dreiecks](#rgb-triplet)Ausdrücken.</span><span class="sxs-lookup"><span data-stu-id="d62ed-129">When the attribute type of a VML element is color -- such as **fillcolor** and **strokecolor** -- you can express the color by using either a [keyword color name](#keyword-color-name) or an [RGB triplet](#rgb-triplet).</span></span>

<span data-ttu-id="d62ed-130">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="d62ed-130">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="keyword-color-name"></a><span data-ttu-id="d62ed-131">Name der Schlüsselwort Farbe</span><span class="sxs-lookup"><span data-stu-id="d62ed-131">Keyword Color Name</span></span>

<span data-ttu-id="d62ed-132">HTML 4,0 definiert eine Liste von Schlüsselwort Farben.</span><span class="sxs-lookup"><span data-stu-id="d62ed-132">HTML 4.0 defines a list of keyword color names.</span></span> <span data-ttu-id="d62ed-133">Dabei handelt es sich um Aqua, Black, Blue, Fuchsia, Gray, Green, Kalk, Maroon, Navy, Olive, lila, rot, Silber, Teal, weiß und gelb.</span><span class="sxs-lookup"><span data-stu-id="d62ed-133">They are aqua, black, blue, fuchsia, gray, green, lime, maroon, navy, olive, purple, red, silver, teal, white, and yellow.</span></span> <span data-ttu-id="d62ed-134">Der RGB-Wert für diese 16 Farben wird in der [Spezifikation von HTML 4,0](https://www.w3.org/TR/REC-html40/types.mdl#h-6-5) definiert.</span><span class="sxs-lookup"><span data-stu-id="d62ed-134">The RGB value for these 16 colors are defined in [HTML 4.0 specification](https://www.w3.org/TR/REC-html40/types.mdl#h-6-5) .</span></span>

<span data-ttu-id="d62ed-135">Sie können z. b. ein Rechteck mit gelb zeichnen, indem Sie angeben `fillcolor="yellow"` , und einen blauen Umriss angeben, indem Sie angeben `strokecolor="blue"` , wie in der folgenden VML-Darstellung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="d62ed-135">For example, you can draw a rectangle filled with yellow by specifying `fillcolor="yellow"`, and give it a blue outline by specifying `strokecolor="blue"`, as shown in the following VML representation:</span></span>

![color1.gif (305 Bytes)](images/color1.gif)


```HTML
<v:rect style='width:120pt;height:80pt;'
fillcolor="yellow" strokecolor="blue"/>
```





<span data-ttu-id="d62ed-137">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="d62ed-137">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="rgb-triplet"></a><span data-ttu-id="d62ed-138">RGB-dreier</span><span class="sxs-lookup"><span data-stu-id="d62ed-138">RGB Triplet</span></span>

<span data-ttu-id="d62ed-139">Wenn es sich bei der Farbe nicht um einen [Schlüsselwort Farbnamen](#keyword-color-name)handelt, können Sie die Farbe entweder als RGB-Dezimalzahl oder als RGB-hexadezimal Trennzeichen Ausdrücken.</span><span class="sxs-lookup"><span data-stu-id="d62ed-139">If the color is not a [keyword color name](#keyword-color-name), you can express the color as either an RGB decimal triplet or an RGB hexadecimal triplet.</span></span> <span data-ttu-id="d62ed-140">Mit RGB-Werten können Sie Werte für die roten, grünen und blauen Komponenten der Farbe angeben, wobei jede Komponente auf einen Wert zwischen 0 und 255 in Dezimalwert oder 00 bis FF im Hexadezimal Bereich festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="d62ed-140">With RGB triplets, you can specify values for the red, green, and blue components of the color, setting each component to a value ranging from 0 through 255 in decimal, or 00 through FF in hexadecimal.</span></span>

<span data-ttu-id="d62ed-141">Sie können z. b. ein Rechteck erstellen, das mit einer angepassten Farbe mit einem RGB-Wert von 253, 249, 186 in Dezimalform aufgefüllt ist, indem Sie entweder `fillcolor="rgb(253,249, 186)"` oder angeben `fillcolor="#FDF9BA"` , wie in der folgenden VML-Darstellung gezeigt.</span><span class="sxs-lookup"><span data-stu-id="d62ed-141">For example, you can create a rectangle that is filled with a customized color with an RGB value of 253, 249, 186 in decimal by specifying either `fillcolor="rgb(253,249, 186)"` or `fillcolor="#FDF9BA"`, as shown in the following VML representation.</span></span> <span data-ttu-id="d62ed-142">In Hexadezimal wird der Wert 253 zu FD, 249 wird zu F9, und 186 wird zu BA.</span><span class="sxs-lookup"><span data-stu-id="d62ed-142">In hexadecimal, the value 253 becomes FD, 249 becomes F9, and 186 becomes BA.</span></span>

![color2.gif (305 Bytes)](images/color2.gif)


```HTML
<v:rect style='width:120pt;height:80pt;'
fillcolor="#FDF9BA" strokecolor="blue"/>
```





<span data-ttu-id="d62ed-144">Wenn der RGB-Wert im Hexadezimal Format über ein Muster wie xxyyzz verfügt, können Sie es mit XYZ abkürzen.</span><span class="sxs-lookup"><span data-stu-id="d62ed-144">If the RGB in hexadecimal has a pattern such as XXYYZZ, you can abbreviate it to XYZ.</span></span> <span data-ttu-id="d62ed-145">Beispielsweise kann " \# 66ff99" als " \# 6f9" ausgeschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="d62ed-145">For example, "\#66FF99" can be written out as "\#6F9".</span></span>

<span data-ttu-id="d62ed-146">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="d62ed-146">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="d62ed-147">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="d62ed-147">Summary</span></span>

<span data-ttu-id="d62ed-148">In VML können Sie eine Farbe in einem der folgenden Formate darstellen:</span><span class="sxs-lookup"><span data-stu-id="d62ed-148">In VML, you can represent a color in one of the following formats:</span></span>

1.  <span data-ttu-id="d62ed-149">FillColor = "Blue"</span><span class="sxs-lookup"><span data-stu-id="d62ed-149">fillcolor="blue"</span></span>
2.  <span data-ttu-id="d62ed-150">FillColor = "RGB (0, RGB)"</span><span class="sxs-lookup"><span data-stu-id="d62ed-150">fillcolor="rgb(0,0,255)"</span></span>
3.  <span data-ttu-id="d62ed-151">FillColor = " \# 0000FF"</span><span class="sxs-lookup"><span data-stu-id="d62ed-151">fillcolor="\#0000ff"</span></span>

 

 