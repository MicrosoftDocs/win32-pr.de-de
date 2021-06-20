---
title: Verwenden des Stroke-Elements
description: In diesem Artikel wird die Verwendung des Stroke-Elements von VML beschrieben, einem Feature, das ab Windows Internet Explorer 9 veraltet ist.
ms.assetid: e3d9dbe5-e087-4b6f-8318-c7d4485cd502
keywords:
- Web workshop,stroke-Element
- Entwerfen von Webseiten, Strichelement
- Vector Markup Language (VML),Strichelement
- VML (Vector Markup Language),Strichelement
- Vektorgrafik, Strichelement
- stroke-Element
- VML-Elemente, Strich
- VML-Formen, Strichelement
- Vector Markup Language (VML),Dashstyle-Eigenschaftsattribut
- VML (Vector Markup Language),Dashstyle-Eigenschaftsattribut
- Vektorgrafik, Dashstyle-Eigenschaftsattribut
- dashstyle-Eigenschaftsattribut
- Vector Markup Language (VML),Opacity-Eigenschaftsattribut
- VML-Eigenschaftsattribut (Vector Markup Language),Deckkrafteigenschaft
- Vektorgrafik, Opacity-Eigenschaftsattribut
- Opacity-Eigenschaftsattribut
- Vector Markup Language (VML),Linestyle-Eigenschaftsattribut
- VML (Vector Markup Language),Linestyle-Eigenschaftsattribut
- Vektorgrafik, Eigenschaftenattribut "linestyle"
- linestyle-Eigenschaftsattribut
- Vector Markup Language (VML),Joinstyle-Eigenschaftsattribut
- VML (Vector Markup Language),Joinstyle-Eigenschaftsattribut
- Vektorgrafik, Joinstyle-Eigenschaftsattribut
- joinstyle-Eigenschaftsattribut
- Vector Markup Language (VML), Filltype-Eigenschaftsattribut
- VML (Vector Markup Language),Filltype-Eigenschaftsattribut
- Vektorgrafiken, Filltype-Eigenschaftsattribut
- filltype-Eigenschaftsattribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dff7a4b3bc654063fe8156476cc9c52453247a0b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407843"
---
# <a name="using-the-stroke-element"></a><span data-ttu-id="d25f1-131">Verwenden des Stroke-Elements</span><span class="sxs-lookup"><span data-stu-id="d25f1-131">Using the Stroke Element</span></span>

<span data-ttu-id="d25f1-132">In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="d25f1-132">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d25f1-133">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="d25f1-133">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d25f1-134">Seit Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="d25f1-134">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d25f1-135">Daher wird sie nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="d25f1-135">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d25f1-136">Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/)</span><span class="sxs-lookup"><span data-stu-id="d25f1-136">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d25f1-137">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)</span><span class="sxs-lookup"><span data-stu-id="d25f1-137">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d25f1-138">Verwenden von `<stroke>`</span><span class="sxs-lookup"><span data-stu-id="d25f1-138">Using `<stroke>`</span></span>

<span data-ttu-id="d25f1-139">Wie Sie gelernt haben, können Sie die **Strokecolor-** und **Strokeweight-Eigenschaftsattribute** einer vordefinierten Form wie , , , , , , `<oval>` `<line>` `<polyline>` `<curve>` `<rect>` `<roundrect>` `<arc>` verwenden, um die Farbe und Gewichtung der Kontur einer Form anzugeben.</span><span class="sxs-lookup"><span data-stu-id="d25f1-139">As you've learned, you can use the **strokecolor** and **strokeweight** property attributes of a predefined shape -- such as `<oval>` , `<line>`, `<polyline>`, `<curve>`, `<rect>`, `<roundrect>`, `<arc>` -- to specify the color and weight of a shape's outline.</span></span> <span data-ttu-id="d25f1-140">In diesem Thema wird veranschaulicht, wie eine Form mit einer erweiterten Kontur gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="d25f1-140">In this topic, we will illustrate how to draw a shape that has a more advanced outline.</span></span>

<span data-ttu-id="d25f1-141">Sie können das `<stroke>` Unterelement innerhalb von `<shape>` oder oder in `<shapetype>` einem beliebigen vordefinierten Formelement platzieren, um zu beschreiben, wie die Kontur der Form gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="d25f1-141">You can place the `<stroke>` sub-element inside the `<shape>`, or `<shapetype>`, or any predefined shape element to describe how to draw the outline of the shape.</span></span> <span data-ttu-id="d25f1-142">Anschließend können Sie die Eigenschaftsattribute (z. [B. Dashstyle,](#dashstyle) [Deckkraft,](#opacity) [Linestyle,](#linestyle) [Joinstyle,](#joinstyle) [Filltype)](#filltype) des `<stroke>` Unterelements verwenden, um die Kontur anzupassen.</span><span class="sxs-lookup"><span data-stu-id="d25f1-142">You can then use the property attributes -- for example, [dashstyle](#dashstyle), [opacity](#opacity), [linestyle](#linestyle), [joinstyle](#joinstyle), [filltype](#filltype) -- of the `<stroke>` sub-element to customize the outline.</span></span>

<span data-ttu-id="d25f1-143">[![Zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="d25f1-143">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="dashstyle"></a><span data-ttu-id="d25f1-144">Dashstyle</span><span class="sxs-lookup"><span data-stu-id="d25f1-144">dashstyle</span></span>

<span data-ttu-id="d25f1-145">Sie können das **Dashstyle-Eigenschaftsattribut** des `<stroke>` Unterelements verwenden, um eine Kontur mit verschiedenen Bindestrichen zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="d25f1-145">You can use the **dashstyle** property attribute of the `<stroke>` sub-element to draw an outline with various dash styles.</span></span>

<span data-ttu-id="d25f1-146">**Beispiele:**</span><span class="sxs-lookup"><span data-stu-id="d25f1-146">**Examples:**</span></span>

<span data-ttu-id="d25f1-147">Wenn Sie `<v:stroke dashstyle="solid" />` innerhalb des `<line>` -Elements angeben, können Sie eine durchgezogene Linie erstellen, wie in der folgenden VML-Darstellung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="d25f1-147">If you specify `<v:stroke dashstyle="solid" />` inside the `<line>` element, you can create a solid line, as shown in the following VML representation:</span></span>

![solid.gif (96 Bytes)](images/solid.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="solid" />
</v:line>
```





<span data-ttu-id="d25f1-149">Wenn Sie das **Dashstyle-Eigenschaftsattribut** in "dot" ändern, können Sie eine gepunktete Linie erstellen, wie in der folgenden VML-Darstellung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="d25f1-149">If you change the **dashstyle** property attribute to "dot", you can create a dotted line, as shown in the following VML representation:</span></span>

![dot.gif (144 Byte)](images/dot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dot" />
</v:line>
```





<span data-ttu-id="d25f1-151">Wenn Sie das **Dashstyle-Eigenschaftsattribut** in "Bindestrich" ändern, können Sie eine Bindestrichlinie erstellen, wie in der folgenden VML-Darstellung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="d25f1-151">If you change the **dashstyle** property attribute to "dash", you can create a dash line, as shown in the following VML representation:</span></span>

![dash.gif (137 Bytes)](images/dash.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dash" />
</v:line>
```





<span data-ttu-id="d25f1-153">Wenn Sie das **Dashstyle-Eigenschaftsattribut** in "dashdot" ändern, können Sie eine Linie mit einem gestrichelten und gepunkteten Stil erstellen, wie in der folgenden VML-Darstellung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="d25f1-153">If you change the **dashstyle** property attribute to "dashdot", you can create a line with a dashed and dotted style, as shown in the following VML representation:</span></span>

![dashdot.gif (145 Bytes)](images/dashdot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dashdot" />
</v:line>
```





<span data-ttu-id="d25f1-155">Wenn Sie das **Dashstyle-Eigenschaftsattribut** in "longdash" ändern, können Sie eine Linie mit einem langen gestrichelten Stil erstellen, wie in der folgenden VML-Darstellung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="d25f1-155">If you change the **dashstyle** property attribute to "longdash", you can create a line with a long dashed style, as shown in the following VML representation:</span></span>

![longdash.gif (123 Bytes)](images/longdash.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="longdash" />
</v:line>
```





<span data-ttu-id="d25f1-157">Wenn Sie das **Dashstyle-Eigenschaftsattribut** in "longdashdot" ändern, können Sie eine Linie mit einem langen gestrichelten und gepunkteten Stil erstellen, wie in der folgenden VML-Darstellung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="d25f1-157">If you change the **dashstyle** property attribute to "longdashdot", you can create a line with a long dashed and dotted style, as shown in the following VML representation:</span></span>

![longdashdot.gif (135 Byte)](images/longdashdot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="longdashdot" />
</v:line>
```





<span data-ttu-id="d25f1-159">Wenn Sie `<v:stroke dashstyle="dashdot" />` innerhalb des Elements `<rect>` platzieren, können Sie ein Rechteck mit gestrichelter und gepunkteter Kontur erstellen, wie in der folgenden VML-Darstellung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="d25f1-159">If you place `<v:stroke dashstyle="dashdot" />` inside the `<rect>` element, you can create a rectangle that has a dashed and dotted outline, as shown in the following VML representation:</span></span>

![rect.gif (615 Bytes)](images/rect.gif)


```HTML
<v:rect style='width:100pt;height:80pt' strokecolor="red" strokeweight="2pt"/>
<v:stroke dashstyle="dashdot" />
</v:rect>
```





<span data-ttu-id="d25f1-161">[![Zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="d25f1-161">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="opacity"></a><span data-ttu-id="d25f1-162">Durchlässigkeit</span><span class="sxs-lookup"><span data-stu-id="d25f1-162">opacity</span></span>

<span data-ttu-id="d25f1-163">Sie können das **Opacity-Eigenschaftsattribut** des `<stroke>` Unterelements verwenden, um eine Kontur mit verschiedenen Deckkraftstilen zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="d25f1-163">You can use the **opacity** property attribute of the `<stroke>` sub-element to draw an outline with various opacity styles.</span></span> <span data-ttu-id="d25f1-164">Der Wert für das **Opacity-Eigenschaftsattribut** kann eine beliebige Zahl zwischen 0 und 1 sein.</span><span class="sxs-lookup"><span data-stu-id="d25f1-164">The value for the **opacity** property attribute can be any number between 0 to 1.</span></span> <span data-ttu-id="d25f1-165">Standardmäßig ist es 1, was die vollständige Deckkraft angibt.</span><span class="sxs-lookup"><span data-stu-id="d25f1-165">By default, it is 1, indicating full opacity.</span></span>

<span data-ttu-id="d25f1-166">**Beispiele:**</span><span class="sxs-lookup"><span data-stu-id="d25f1-166">**Examples:**</span></span>

<span data-ttu-id="d25f1-167">Die folgende VML-Darstellung erstellt eine Linie mit vollständiger Deckkraft:</span><span class="sxs-lookup"><span data-stu-id="d25f1-167">The following VML representation creates a line with full opacity:</span></span>

![line1.gif (96 Bytes)](images/line1.gif)


```HTML
<v:line style='position:relative;' from="20pt,50pt" to="200pt,50pt" strokecolor="red"
strokeweight="2pt">
</v:line>
```





<span data-ttu-id="d25f1-169">Wenn Sie `<v:stroke opacity="0.5" />` innerhalb des `<line>` -Elements hinzufügen, können Sie eine Linie mit einer Deckkraft von 50 % erstellen, wie in der folgenden VML-Darstellung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="d25f1-169">If you add `<v:stroke opacity="0.5" />` inside the `<line>` element, you can create a line with 50% opacity, as shown in the following VML representation:</span></span>

![line2.gif (108 Bytes)](images/line2.gif)


```HTML
<v:line style='position:relative;' from="20pt,50pt" to="200pt,50pt" strokecolor="red"
strokeweight="2pt">
<v:stroke opacity="0.5" />
</v:line>
```





<span data-ttu-id="d25f1-171">[![Zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="d25f1-171">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="linestyle"></a><span data-ttu-id="d25f1-172">Linestyle</span><span class="sxs-lookup"><span data-stu-id="d25f1-172">linestyle</span></span>

<span data-ttu-id="d25f1-173">Sie können das Eigenschaftenattribut **linestyle** des `<stroke>` Unterelements verwenden, um eine Kontur mit verschiedenen Linienstilen zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="d25f1-173">You can use the **linestyle** property attribute of the `<stroke>` sub-element to draw an outline with various line styles.</span></span>

<span data-ttu-id="d25f1-174">**Beispiele:**</span><span class="sxs-lookup"><span data-stu-id="d25f1-174">**Examples:**</span></span>

<span data-ttu-id="d25f1-175">Wenn Sie `<v:stroke linestyle="single" />` im `<rect>` -Element angeben, können Sie ein Rechteck mit einer einzelnen Kontur erstellen, wie in der folgenden VML-Darstellung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="d25f1-175">If you specify `<v:stroke linestyle="single" />` inside the `<rect>` element, you can create a rectangle with a single outline, as shown in the following VML representation:</span></span>

![single.gif (537 Bytes)](images/single.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red" strokeweight="10pt">
<v:stroke linestyle="single" />
</v:rect>
```





<span data-ttu-id="d25f1-177">Wenn Sie  das Linestyle-Eigenschaftsattribut in "thinthin" ändern, können Sie ein Rechteck mit der Kontur (1:1:1) erstellen, wie in der folgenden VML-Darstellung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="d25f1-177">If you change the **linestyle** property attribute to "thinthin", you can create a rectangle with the outline (1:1:1), as shown in the following VML representation:</span></span>

![thinthin.gif (642 Byte)](images/thinthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thinthin" />
</v:rect>
```





<span data-ttu-id="d25f1-179">Wenn Sie  das Linestyle-Eigenschaftsattribut in "thinthick" ändern, können Sie ein Rechteck mit der Kontur (1:1:2) erstellen, wie in der folgenden VML-Darstellung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="d25f1-179">If you change the **linestyle** property attribute to "thinthick", you can create a rectangle with the outline (1:1:2), as shown in the following VML representation:</span></span>

![thinthick.gif (646 Bytes)](images/thinthick.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thinthick" />
</v:rect>
```





<span data-ttu-id="d25f1-181">Wenn Sie das Eigenschaftenattribut **linestyle** in "thickthin" ändern, können Sie ein Rechteck mit der Kontur (2:1:1) erstellen, wie in der folgenden VML-Darstellung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="d25f1-181">If you change the **linestyle** property attribute to "thickthin", you can create a rectangle with the outline (2:1:1), as shown in the following VML representation:</span></span>

![thickthin.gif (676 Bytes)](images/thickthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thickthin" />
</v:rect>
```





<span data-ttu-id="d25f1-183">Wenn Sie  das Linestyle-Eigenschaftsattribut in "thickbetweenthin" ändern, können Sie ein Rechteck mit der Kontur (1:1:2:1:1) erstellen, wie in der folgenden VML-Darstellung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="d25f1-183">If you change the **linestyle** property attribute to "thickbetweenthin", you can create a rectangle with the outline (1:1:2:1:1), as shown in the following VML representation:</span></span>

![thickbthin.gif (669 Bytes)](images/thickbthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thickbetweenthin" />
</v:rect>
```





<span data-ttu-id="d25f1-185">[![Zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="d25f1-185">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="joinstyle"></a><span data-ttu-id="d25f1-186">joinstyle</span><span class="sxs-lookup"><span data-stu-id="d25f1-186">joinstyle</span></span>

<span data-ttu-id="d25f1-187">Sie können das **joinstyle-Attribut** des `<stroke>` Unterelements verwenden, um zu definieren, wie Zeilen miteinander verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="d25f1-187">You can use the **joinstyle** attribute of the `<stroke>` sub-element to define how lines are joined together.</span></span>

<span data-ttu-id="d25f1-188">Um z. B. eine Form mit der Rundungsverknüpfungsgliederung zu erstellen, wie in der folgenden Abbildung gezeigt, können Sie `<v:stroke joinstyle="round" />` innerhalb des `<polyline>` -Elements angeben, wie in der folgenden VML-Darstellung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="d25f1-188">For example, to create a shape that has the round-join outline, as shown in the following illustration, you can specify `<v:stroke joinstyle="round" />` inside the `<polyline>` element, as shown in the following VML representation:</span></span>

![round.gif (660 Bytes)](images/round.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="round" />
</v:polyline>
```





<span data-ttu-id="d25f1-190">Wenn Sie  das Joinstyle-Eigenschaftsattribut in "abschrägung" ändern, können Sie eine Form mit der Abschrägungsverknüpfungsgliederung erstellen, wie in der folgenden VML-Darstellung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="d25f1-190">If you change the **joinstyle** property attribute to "bevel", you can create a shape that has the bevel-join outline, as shown in the following VML representation:</span></span>

![bevel.gif (650 Byte)](images/bevel.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="bevel" />
</v:polyline>
```





<span data-ttu-id="d25f1-192">Wenn Sie  das joinstyle-Eigenschaftsattribut in "miter" ändern, können Sie eine Form mit der Kontur "miter-join" erstellen, wie in der folgenden VML-Darstellung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="d25f1-192">If you change the **joinstyle** property attribute to "miter", you can create a shape that has the miter-join outline, as shown in the following VML representation:</span></span>

![miter.gif (702 Bytes)](images/miter.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="miter" />
</v:polyline>
```





<span data-ttu-id="d25f1-194">[![Zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="d25f1-194">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="filltype"></a><span data-ttu-id="d25f1-195">filltype</span><span class="sxs-lookup"><span data-stu-id="d25f1-195">filltype</span></span>

<span data-ttu-id="d25f1-196">Sie können  das filltype-Eigenschaftsattribut des `<stroke>` Unterelements verwenden, um eine Kontur mit verschiedenen Fülleffekten zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="d25f1-196">You can use the **filltype** property attribute of the `<stroke>` sub-element to draw an outline with various fill effects.</span></span>

<span data-ttu-id="d25f1-197">**Beispiele:**</span><span class="sxs-lookup"><span data-stu-id="d25f1-197">**Examples:**</span></span>

<span data-ttu-id="d25f1-198">Wenn Sie `<v:stroke filltype="solid" />` im `<roundrect>` -Element angeben, können Sie ein abgerundetes Rechteck mit der durchgezogenen Kontur erstellen, wie in der folgenden VML-Darstellung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="d25f1-198">If you specify `<v:stroke filltype="solid" />` inside the `<roundrect>` element, you can create a rounded rectangle with the solid-filled outline, as shown in the following VML representation:</span></span>

![solid.gif (701 Byte)](images/solidborder.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="solid" />
</v:roundrect>
```





<span data-ttu-id="d25f1-200">Wenn Sie  das filltype-Eigenschaftsattribut in "pattern" ändern, das src-Eigenschaftsattribut auf den Speicherort der Musterbilddatei verweisen und das **Color2-Eigenschaftsattribut** auf die zweite Musterfarbe festlegen, können Sie ein abgerundetes Rechteck mit einer Mustergliederung erstellen, wie in der folgenden VML-Darstellung gezeigt: </span><span class="sxs-lookup"><span data-stu-id="d25f1-200">If you change the **filltype** property attribute to "pattern", point the **src** property attribute to the location of the pattern image file, and set the **color2** property attribute to the second pattern color, you can create a rounded rectangle with a pattern outline, as shown in the following VML representation:</span></span>

![pattern.gif (1055 Bytes)](images/pattern.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="pattern" src="image.gif"
color2="green" />
</v:roundrect>
```





<span data-ttu-id="d25f1-202">Wenn Sie  das Filltype-Eigenschaftsattribut in "tile" ändern und das src-Eigenschaftsattribut auf den Speicherort der Bilddatei verweisen, können Sie ein abgerundetes Rechteck mit einer gekachelten Gliederung erstellen, wie in der folgenden VML-Darstellung gezeigt: </span><span class="sxs-lookup"><span data-stu-id="d25f1-202">If you change the **filltype** property attribute to "tile" and point the **src** property attribute to the location of the image file, you can create a rounded rectangle with a tiled outline, as shown in the following VML representation:</span></span>

![tile.gif (6617 Bytes)](images/tile.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="tile" src="image2.gif" />
</v:roundrect>
```





<span data-ttu-id="d25f1-204">Wenn Sie  das filltype-Eigenschaftsattribut in "frame" ändern und das src-Eigenschaftsattribut auf den Speicherort der Bilddatei verweisen, können Sie ein abgerundetes Rechteck mit einer Bildgliederung erstellen, wie in der folgenden VML-Darstellung gezeigt: </span><span class="sxs-lookup"><span data-stu-id="d25f1-204">If you change the **filltype** property attribute to "frame" and point the **src** property attribute to the location of the image file, you can create a rounded rectangle with a picture outline, as shown in the following VML representation:</span></span>

![frame.gif (6203 Bytes)](images/frame.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="frame" src="image2.gif" />
</v:roundrect>
```





<span data-ttu-id="d25f1-206">Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation.](https://www.w3.org/TR/NOTE-VML#-toc416858395)</span><span class="sxs-lookup"><span data-stu-id="d25f1-206">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858395) .</span></span>

 

 