---
title: Verwenden des Stroke-Elements
description: In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.
ms.assetid: e3d9dbe5-e087-4b6f-8318-c7d4485cd502
keywords:
- Webworkshop, Stroke-Element
- Entwerfen von Webseiten, Stroke-Element
- Vector Markup Language (VML), Stroke-Element
- VML (Vector Markup Language), Stroke-Element
- Vektorgrafiken, Stroke-Element
- Stroke-Element
- VML-Elemente, Strich
- VML-Formen, Stroke-Element
- Vector Markup Language (VML), Eigenschafts Attribut für dashstile
- VML (Vector Markup Language), Eigenschafts Attribut für dashstile
- Vektorgrafiken, Eigenschafts Attribut für dashstile
- DashStyle-Eigenschafts Attribut
- Vector Markup Language (VML), Opacity-Eigenschafts Attribut
- VML (Vector Markup Language), Opacity-Eigenschafts Attribut
- Vektorgrafiken, Opacity-Eigenschafts Attribut
- Deck Kraft-Eigenschafts Attribut
- Vector Markup Language (VML), LineStyle-Eigenschafts Attribut
- VML (Vector Markup Language), LineStyle-Eigenschafts Attribut
- Vektorgrafiken, LineStyle-Eigenschafts Attribut
- LineStyle-Eigenschafts Attribut
- Vector Markup Language (VML), JOINSTYLE-Eigenschafts Attribut
- VML (Vector Markup Language), JOINSTYLE-Eigenschafts Attribut
- Vektorgrafiken, JOINSTYLE-Eigenschafts Attribut
- JOINSTYLE-Eigenschafts Attribut
- Vector Markup Language (VML), FillType-Eigenschafts Attribut
- VML (Vector Markup Language), FillType-Eigenschafts Attribut
- Vektorgrafiken, FillType-Eigenschafts Attribut
- FillType-Eigenschafts Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b58e02945884ea63ad1be01e67cfc156951cd5e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316353"
---
# <a name="using-the-stroke-element"></a><span data-ttu-id="73bd8-132">Verwenden des Stroke-Elements</span><span class="sxs-lookup"><span data-stu-id="73bd8-132">Using the Stroke Element</span></span>

<span data-ttu-id="73bd8-133">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="73bd8-133">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="73bd8-134">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="73bd8-134">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="73bd8-135">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="73bd8-135">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="73bd8-136">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="73bd8-136">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="73bd8-137">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="73bd8-137">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="73bd8-138">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="73bd8-138">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="73bd8-139">Verwenden von `<stroke>`</span><span class="sxs-lookup"><span data-stu-id="73bd8-139">Using `<stroke>`</span></span>

<span data-ttu-id="73bd8-140">Wie Sie gelernt haben, können Sie die Eigenschaften Attribute **strokeColor** und **strokeweight** einer vordefinierten Form (z. b. `<oval>` ,, `<line>` , `<polyline>` `<curve>` , `<rect>` ,,--) verwenden, `<roundrect>` `<arc>` um die Farbe und Gewichtung der Kontur einer Form anzugeben.</span><span class="sxs-lookup"><span data-stu-id="73bd8-140">As you've learned, you can use the **strokecolor** and **strokeweight** property attributes of a predefined shape -- such as `<oval>` , `<line>`, `<polyline>`, `<curve>`, `<rect>`, `<roundrect>`, `<arc>` -- to specify the color and weight of a shape's outline.</span></span> <span data-ttu-id="73bd8-141">In diesem Thema wird veranschaulicht, wie Sie eine Form mit einer erweiterten Gliederung zeichnen.</span><span class="sxs-lookup"><span data-stu-id="73bd8-141">In this topic, we will illustrate how to draw a shape that has a more advanced outline.</span></span>

<span data-ttu-id="73bd8-142">Sie können das `<stroke>` untergeordnete Element innerhalb des- `<shape>` ,-oder-Elements `<shapetype>` oder eines beliebigen vordefinierten Shape-Elements platzieren, um zu beschreiben, wie der Umriss der Form gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="73bd8-142">You can place the `<stroke>` sub-element inside the `<shape>`, or `<shapetype>`, or any predefined shape element to describe how to draw the outline of the shape.</span></span> <span data-ttu-id="73bd8-143">Sie können dann die Eigenschafts Attribute (z. b. "Dashboard", " [Deck Kraft](#opacity)", " [LineStyle](#linestyle) [", "](#dashstyle) [JOINSTYLE](#joinstyle)", " [FillType](#filltype) ") des `<stroke>` unter Elements verwenden, um die Kontur anzupassen.</span><span class="sxs-lookup"><span data-stu-id="73bd8-143">You can then use the property attributes -- for example, [dashstyle](#dashstyle), [opacity](#opacity), [linestyle](#linestyle), [joinstyle](#joinstyle), [filltype](#filltype) -- of the `<stroke>` sub-element to customize the outline.</span></span>

<span data-ttu-id="73bd8-144">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="73bd8-144">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="dashstyle"></a><span data-ttu-id="73bd8-145">DashStyle</span><span class="sxs-lookup"><span data-stu-id="73bd8-145">dashstyle</span></span>

<span data-ttu-id="73bd8-146">Sie können **das Eigenschafts** Attribut "Dashboard" des `<stroke>` unter Elements verwenden, um einen Umriss mit verschiedenen Bindestrichen zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="73bd8-146">You can use the **dashstyle** property attribute of the `<stroke>` sub-element to draw an outline with various dash styles.</span></span>

<span data-ttu-id="73bd8-147">**Beispiele:**</span><span class="sxs-lookup"><span data-stu-id="73bd8-147">**Examples:**</span></span>

<span data-ttu-id="73bd8-148">Wenn Sie `<v:stroke dashstyle="solid" />` im- `<line>` Element angeben, können Sie eine vollständig erstellte Linie erstellen, wie in der folgenden VML-Darstellung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="73bd8-148">If you specify `<v:stroke dashstyle="solid" />` inside the `<line>` element, you can create a solid line, as shown in the following VML representation:</span></span>

![solid.gif (96 Bytes)](images/solid.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="solid" />
</v:line>
```





<span data-ttu-id="73bd8-150">Wenn Sie das Eigenschafts Attribut "Dashboard" in "Punkt" ändern, können Sie eine gepunktete Linie erstellen, wie **in der folgenden** VML-Darstellung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="73bd8-150">If you change the **dashstyle** property attribute to "dot", you can create a dotted line, as shown in the following VML representation:</span></span>

![dot.gif (144 Bytes)](images/dot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dot" />
</v:line>
```





<span data-ttu-id="73bd8-152">Wenn Sie das Eigenschafts Attribut "Dashboard" in "Dash" ändern, können Sie wie **in der folgenden** VML-Darstellung gezeigt eine Bindestrich Linie erstellen:</span><span class="sxs-lookup"><span data-stu-id="73bd8-152">If you change the **dashstyle** property attribute to "dash", you can create a dash line, as shown in the following VML representation:</span></span>

![dash.gif (137 bytes)](images/dash.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dash" />
</v:line>
```





<span data-ttu-id="73bd8-154">Wenn Sie das Eigenschafts Attribut " **DashStyle** " in "DashDot" ändern, können Sie eine Linie mit einem gestrichelten und gepunkteten Stil erstellen, wie in der folgenden VML-Darstellung dargestellt:</span><span class="sxs-lookup"><span data-stu-id="73bd8-154">If you change the **dashstyle** property attribute to "dashdot", you can create a line with a dashed and dotted style, as shown in the following VML representation:</span></span>

![dashdot.gif (145 bytes)](images/dashdot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dashdot" />
</v:line>
```





<span data-ttu-id="73bd8-156">Wenn Sie das Eigenschafts Attribut "Dashboard" in "longdash" ändern, können Sie eine Zeile mit einem langen gestrichelten Stil erstellen, wie **in der folgenden** VML-Darstellung dargestellt:</span><span class="sxs-lookup"><span data-stu-id="73bd8-156">If you change the **dashstyle** property attribute to "longdash", you can create a line with a long dashed style, as shown in the following VML representation:</span></span>

![longdash.gif (123 Bytes)](images/longdash.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="longdash" />
</v:line>
```





<span data-ttu-id="73bd8-158">Wenn **Sie das** Eigenschafts Attribut "Dashboard" in "longdashdot" ändern, können Sie eine Zeile mit einem langen gestrichelten und gepunkteten Stil erstellen, wie in der folgenden VML-Darstellung dargestellt:</span><span class="sxs-lookup"><span data-stu-id="73bd8-158">If you change the **dashstyle** property attribute to "longdashdot", you can create a line with a long dashed and dotted style, as shown in the following VML representation:</span></span>

![longdashdot.gif (135 bytes)](images/longdashdot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="longdashdot" />
</v:line>
```





<span data-ttu-id="73bd8-160">Wenn Sie im- `<v:stroke dashstyle="dashdot" />` `<rect>` Element platzieren, können Sie ein Rechteck mit einem gestrichelten und gepunkteten Umriss erstellen, wie in der folgenden VML-Darstellung dargestellt:</span><span class="sxs-lookup"><span data-stu-id="73bd8-160">If you place `<v:stroke dashstyle="dashdot" />` inside the `<rect>` element, you can create a rectangle that has a dashed and dotted outline, as shown in the following VML representation:</span></span>

![rect.gif (615 bytes)](images/rect.gif)


```HTML
<v:rect style='width:100pt;height:80pt' strokecolor="red" strokeweight="2pt"/>
<v:stroke dashstyle="dashdot" />
</v:rect>
```





<span data-ttu-id="73bd8-162">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="73bd8-162">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="opacity"></a><span data-ttu-id="73bd8-163">Durchlässigkeit</span><span class="sxs-lookup"><span data-stu-id="73bd8-163">opacity</span></span>

<span data-ttu-id="73bd8-164">Sie können das Attribut der **Deck Kraft** -Eigenschaft des `<stroke>` unter Elements verwenden, um eine Gliederung mit verschiedenen Deckkraft Stilen zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="73bd8-164">You can use the **opacity** property attribute of the `<stroke>` sub-element to draw an outline with various opacity styles.</span></span> <span data-ttu-id="73bd8-165">Der Wert für das Attribut für die **Deck Kraft** -Eigenschaft kann eine beliebige Zahl zwischen 0 und 1 sein.</span><span class="sxs-lookup"><span data-stu-id="73bd8-165">The value for the **opacity** property attribute can be any number between 0 to 1.</span></span> <span data-ttu-id="73bd8-166">Standardmäßig ist der Wert 1, was eine vollständige Deckkraft angibt.</span><span class="sxs-lookup"><span data-stu-id="73bd8-166">By default, it is 1, indicating full opacity.</span></span>

<span data-ttu-id="73bd8-167">**Beispiele:**</span><span class="sxs-lookup"><span data-stu-id="73bd8-167">**Examples:**</span></span>

<span data-ttu-id="73bd8-168">In der folgenden VML-Darstellung wird eine Zeile mit vollständiger Deckkraft erstellt:</span><span class="sxs-lookup"><span data-stu-id="73bd8-168">The following VML representation creates a line with full opacity:</span></span>

![line1.gif (96 Bytes)](images/line1.gif)


```HTML
<v:line style='position:relative;' from="20pt,50pt" to="200pt,50pt" strokecolor="red"
strokeweight="2pt">
</v:line>
```





<span data-ttu-id="73bd8-170">Wenn Sie `<v:stroke opacity="0.5" />` innerhalb des- `<line>` Elements hinzufügen, können Sie eine Zeile mit einer Deckkraft von 50% erstellen, wie in der folgenden VML-Darstellung dargestellt:</span><span class="sxs-lookup"><span data-stu-id="73bd8-170">If you add `<v:stroke opacity="0.5" />` inside the `<line>` element, you can create a line with 50% opacity, as shown in the following VML representation:</span></span>

![line2.gif (108 bytes)](images/line2.gif)


```HTML
<v:line style='position:relative;' from="20pt,50pt" to="200pt,50pt" strokecolor="red"
strokeweight="2pt">
<v:stroke opacity="0.5" />
</v:line>
```





<span data-ttu-id="73bd8-172">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="73bd8-172">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="linestyle"></a><span data-ttu-id="73bd8-173">LineStyle</span><span class="sxs-lookup"><span data-stu-id="73bd8-173">linestyle</span></span>

<span data-ttu-id="73bd8-174">Sie können das **LineStyle** -Eigenschafts Attribut des `<stroke>` untergeordneten-Elements verwenden, um eine Gliederung mit verschiedenen Linienstilen zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="73bd8-174">You can use the **linestyle** property attribute of the `<stroke>` sub-element to draw an outline with various line styles.</span></span>

<span data-ttu-id="73bd8-175">**Beispiele:**</span><span class="sxs-lookup"><span data-stu-id="73bd8-175">**Examples:**</span></span>

<span data-ttu-id="73bd8-176">Wenn Sie `<v:stroke linestyle="single" />` im- `<rect>` Element angeben, können Sie ein Rechteck mit einem einzelnen Umriss erstellen, wie in der folgenden VML-Darstellung dargestellt:</span><span class="sxs-lookup"><span data-stu-id="73bd8-176">If you specify `<v:stroke linestyle="single" />` inside the `<rect>` element, you can create a rectangle with a single outline, as shown in the following VML representation:</span></span>

![single.gif (537 Bytes)](images/single.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red" strokeweight="10pt">
<v:stroke linestyle="single" />
</v:rect>
```





<span data-ttu-id="73bd8-178">Wenn Sie das **LineStyle** -Eigenschafts Attribut in "Thin Thin" ändern, können Sie ein Rechteck mit der Kontur (1:1:1) erstellen, wie in der folgenden VML-Darstellung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="73bd8-178">If you change the **linestyle** property attribute to "thinthin", you can create a rectangle with the outline (1:1:1), as shown in the following VML representation:</span></span>

![thinthin.gif (642 bytes)](images/thinthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thinthin" />
</v:rect>
```





<span data-ttu-id="73bd8-180">Wenn Sie das **LineStyle** -Eigenschafts Attribut in "Thin Thick" ändern, können Sie ein Rechteck mit der Kontur (1:1:2) erstellen, wie in der folgenden VML-Darstellung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="73bd8-180">If you change the **linestyle** property attribute to "thinthick", you can create a rectangle with the outline (1:1:2), as shown in the following VML representation:</span></span>

![thinthick.gif (646 bytes)](images/thinthick.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thinthick" />
</v:rect>
```





<span data-ttu-id="73bd8-182">Wenn Sie das **LineStyle** -Eigenschafts Attribut in "Thick Thin" ändern, können Sie ein Rechteck mit der Kontur (2:1:1) erstellen, wie in der folgenden VML-Darstellung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="73bd8-182">If you change the **linestyle** property attribute to "thickthin", you can create a rectangle with the outline (2:1:1), as shown in the following VML representation:</span></span>

![thickthin.gif (676 bytes)](images/thickthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thickthin" />
</v:rect>
```





<span data-ttu-id="73bd8-184">Wenn Sie das **LineStyle** -Eigenschafts Attribut in "thickbetweenthin" ändern, können Sie ein Rechteck mit der Kontur (1:1:2:1:1) erstellen, wie in der folgenden VML-Darstellung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="73bd8-184">If you change the **linestyle** property attribute to "thickbetweenthin", you can create a rectangle with the outline (1:1:2:1:1), as shown in the following VML representation:</span></span>

![thickbthin.gif (669 bytes)](images/thickbthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thickbetweenthin" />
</v:rect>
```





<span data-ttu-id="73bd8-186">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="73bd8-186">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="joinstyle"></a><span data-ttu-id="73bd8-187">JOINSTYLE</span><span class="sxs-lookup"><span data-stu-id="73bd8-187">joinstyle</span></span>

<span data-ttu-id="73bd8-188">Sie können das **JOINSTYLE** -Attribut des `<stroke>` untergeordneten-Elements verwenden, um zu definieren, wie Linien verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="73bd8-188">You can use the **joinstyle** attribute of the `<stroke>` sub-element to define how lines are joined together.</span></span>

<span data-ttu-id="73bd8-189">Um z. b. eine Form zu erstellen, die die roundjoingliederung hat, wie in der folgenden Abbildung dargestellt, können Sie im- `<v:stroke joinstyle="round" />` `<polyline>` Element angeben, wie in der folgenden VML-Darstellung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="73bd8-189">For example, to create a shape that has the round-join outline, as shown in the following illustration, you can specify `<v:stroke joinstyle="round" />` inside the `<polyline>` element, as shown in the following VML representation:</span></span>

![round.gif (660 bytes)](images/round.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="round" />
</v:polyline>
```





<span data-ttu-id="73bd8-191">Wenn Sie das Attribut " **JOINSTYLE** Property" in "abvel" ändern, können Sie eine Form erstellen, die die Kontur für den Abschrägungs Join enthält, wie in der folgenden VML-Darstellung dargestellt:</span><span class="sxs-lookup"><span data-stu-id="73bd8-191">If you change the **joinstyle** property attribute to "bevel", you can create a shape that has the bevel-join outline, as shown in the following VML representation:</span></span>

![bevel.gif (650 bytes)](images/bevel.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="bevel" />
</v:polyline>
```





<span data-ttu-id="73bd8-193">Wenn Sie das Attribut " **JOINSTYLE** Property" in "Miter" ändern, können Sie wie in der folgenden VML-Darstellung gezeigt eine Form erstellen, die die Beschreibung des Miter-Joins hat:</span><span class="sxs-lookup"><span data-stu-id="73bd8-193">If you change the **joinstyle** property attribute to "miter", you can create a shape that has the miter-join outline, as shown in the following VML representation:</span></span>

![miter.gif (702 bytes)](images/miter.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="miter" />
</v:polyline>
```





<span data-ttu-id="73bd8-195">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="73bd8-195">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="filltype"></a><span data-ttu-id="73bd8-196">FillType</span><span class="sxs-lookup"><span data-stu-id="73bd8-196">filltype</span></span>

<span data-ttu-id="73bd8-197">Sie können das **FillType** -Eigenschafts Attribut des `<stroke>` unter Elements verwenden, um einen Umriss mit verschiedenen Füll Effekten zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="73bd8-197">You can use the **filltype** property attribute of the `<stroke>` sub-element to draw an outline with various fill effects.</span></span>

<span data-ttu-id="73bd8-198">**Beispiele:**</span><span class="sxs-lookup"><span data-stu-id="73bd8-198">**Examples:**</span></span>

<span data-ttu-id="73bd8-199">Wenn Sie `<v:stroke filltype="solid" />` im- `<roundrect>` Element angeben, können Sie ein abgerundetes Rechteck mit dem vollständig gefüllten Umriss erstellen, wie in der folgenden VML-Darstellung dargestellt:</span><span class="sxs-lookup"><span data-stu-id="73bd8-199">If you specify `<v:stroke filltype="solid" />` inside the `<roundrect>` element, you can create a rounded rectangle with the solid-filled outline, as shown in the following VML representation:</span></span>

![solid.gif (701 Bytes)](images/solidborder.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="solid" />
</v:roundrect>
```





<span data-ttu-id="73bd8-201">Wenn Sie das **FillType** -Eigenschafts Attribut in "Pattern" ändern, das **src** -Eigenschafts Attribut auf den Speicherort der Pattern-Bilddatei verweisen und das **color2** -Eigenschafts Attribut auf die zweite Muster Farbe festlegen, können Sie ein abgerundetes Rechteck mit einem Muster Umriss erstellen, wie in der folgenden VML-Darstellung dargestellt:</span><span class="sxs-lookup"><span data-stu-id="73bd8-201">If you change the **filltype** property attribute to "pattern", point the **src** property attribute to the location of the pattern image file, and set the **color2** property attribute to the second pattern color, you can create a rounded rectangle with a pattern outline, as shown in the following VML representation:</span></span>

![pattern.gif (1055 Bytes)](images/pattern.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="pattern" src="image.gif"
color2="green" />
</v:roundrect>
```





<span data-ttu-id="73bd8-203">Wenn Sie das **FillType** -Eigenschafts Attribut in "Tile" ändern und das **src** -Eigenschafts Attribut auf den Speicherort der Bilddatei verweisen, können Sie ein abgerundetes Rechteck mit einer gekachelten Gliederung erstellen, wie in der folgenden VML-Darstellung dargestellt:</span><span class="sxs-lookup"><span data-stu-id="73bd8-203">If you change the **filltype** property attribute to "tile" and point the **src** property attribute to the location of the image file, you can create a rounded rectangle with a tiled outline, as shown in the following VML representation:</span></span>

![tile.gif (6617 Bytes)](images/tile.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="tile" src="image2.gif" />
</v:roundrect>
```





<span data-ttu-id="73bd8-205">Wenn Sie das **FillType** -Eigenschafts Attribut in "Frame" ändern und das **src** -Eigenschafts Attribut auf den Speicherort der Bilddatei verweisen, können Sie ein abgerundetes Rechteck mit einer Bild Gliederung erstellen, wie in der folgenden VML-Darstellung dargestellt:</span><span class="sxs-lookup"><span data-stu-id="73bd8-205">If you change the **filltype** property attribute to "frame" and point the **src** property attribute to the location of the image file, you can create a rounded rectangle with a picture outline, as shown in the following VML representation:</span></span>

![frame.gif (6203 Bytes)](images/frame.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="frame" src="image2.gif" />
</v:roundrect>
```





<span data-ttu-id="73bd8-207">Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation](https://www.w3.org/TR/NOTE-VML#-toc416858395) .</span><span class="sxs-lookup"><span data-stu-id="73bd8-207">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858395) .</span></span>

 

 