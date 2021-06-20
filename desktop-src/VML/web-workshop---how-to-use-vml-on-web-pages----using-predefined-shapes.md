---
title: Verwenden vordefinierter Formen
description: In diesem Artikel wird die Verwendung vordefinierter Formen in VML beschrieben, einem Feature, das ab Windows Internet Explorer 9 veraltet ist.
ms.assetid: 9a2e8b5a-b1d0-4a73-b058-24dac1f0b655
keywords:
- Web-Workshop, vordefinierte Formen
- Entwerfen von Webseiten, vordefinierte Formen
- Vector Markup Language (VML), vordefinierte Formen
- VML (Vector Markup Language), vordefinierte Formen
- Vektorgrafiken, vordefinierte Formen
- VML-Formen, vordefiniert
- Vordefinierte Formen
- Vector Markup Language (VML),rect-Element
- VML (Vector Markup Language),rect-Element
- Vektorgrafik, rect-Element
- rect-Element
- VML-Elemente, rect
- Vector Markup Language (VML),Roundrect-Element
- VML (Vector Markup Language),Roundrect-Element
- Vektorgrafik, Roundrect-Element
- roundrect-Element
- VML-Elemente, roundrect
- Vector Markup Language (VML),Line-Element
- VML (Vector Markup Language),Line-Element
- Vektorgrafik, Linienelement
- line-Element
- VML-Elemente, Zeile
- Vector Markup Language (VML),Polylinienelement
- VML (Vector Markup Language),Polylinienelement
- Vektorgrafik, Polylinienelement
- polyline-Element
- VML-Elemente, Polylinie
- Vector Markup Language (VML),Curve-Element
- VML (Vector Markup Language),Curve-Element
- Vektorgrafik, Kurvenelement
- curve-Element
- VML-Elemente, Kurve
- Vector Markup Language (VML),Arc-Element
- VML (Vector Markup Language),Arc-Element
- Vektorgrafik, Arc-Element
- Arc-Element
- VML-Elemente, Arc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b410cf288a3ba63e4c1d745fd962a445b0b220b8
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407683"
---
# <a name="using-predefined-shapes"></a><span data-ttu-id="343ec-140">Verwenden vordefinierter Formen</span><span class="sxs-lookup"><span data-stu-id="343ec-140">Using Predefined Shapes</span></span>

<span data-ttu-id="343ec-141">In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="343ec-141">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="343ec-142">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="343ec-142">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="343ec-143">Seit Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="343ec-143">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="343ec-144">Daher wird sie nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="343ec-144">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="343ec-145">Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/)</span><span class="sxs-lookup"><span data-stu-id="343ec-145">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="343ec-146">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)</span><span class="sxs-lookup"><span data-stu-id="343ec-146">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="343ec-147">Wie Sie gelernt haben, können Sie das `<oval>` -Element von VML verwenden, um ein einfaches Oval zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="343ec-147">As you've learned, you can use the `<oval>` element of VML to create a simple oval.</span></span> <span data-ttu-id="343ec-148">VML stellt mehrere andere vordefinierte Elemente bereit.</span><span class="sxs-lookup"><span data-stu-id="343ec-148">VML provides several other predefined elements.</span></span> <span data-ttu-id="343ec-149">In diesem Thema wird veranschaulicht, wie Mithilfe dieser Elemente Grafiken gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="343ec-149">In this topic, we will illustrate how to draw graphics by using these elements.</span></span>

<span data-ttu-id="343ec-150">In diesem Thema:</span><span class="sxs-lookup"><span data-stu-id="343ec-150">In this topic:</span></span>

-   [<span data-ttu-id="343ec-151">Rect</span><span class="sxs-lookup"><span data-stu-id="343ec-151">rect</span></span>](#roundrect)
-   [<span data-ttu-id="343ec-152">roundrect</span><span class="sxs-lookup"><span data-stu-id="343ec-152">roundrect</span></span>](#roundrect)
-   [<span data-ttu-id="343ec-153">line</span><span class="sxs-lookup"><span data-stu-id="343ec-153">line</span></span>](#polyline)
-   [<span data-ttu-id="343ec-154">Polylinie</span><span class="sxs-lookup"><span data-stu-id="343ec-154">polyline</span></span>](#polyline)
-   [<span data-ttu-id="343ec-155">Kurve</span><span class="sxs-lookup"><span data-stu-id="343ec-155">curve</span></span>](#curve)
-   [<span data-ttu-id="343ec-156">Arc</span><span class="sxs-lookup"><span data-stu-id="343ec-156">arc</span></span>](#arc)
-   [<span data-ttu-id="343ec-157">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="343ec-157">Summary</span></span>](#summary)

## <a name="rect"></a><span data-ttu-id="343ec-158">rect</span><span class="sxs-lookup"><span data-stu-id="343ec-158">rect</span></span>

<span data-ttu-id="343ec-159">Sie können das `<rect>` -Element verwenden, um ein Rechteck zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="343ec-159">You can use the `<rect>` element to draw a rectangle.</span></span> <span data-ttu-id="343ec-160">Anschließend können Sie das Rechteck anpassen, indem Sie verschiedene Eigenschaftsattribute angeben.</span><span class="sxs-lookup"><span data-stu-id="343ec-160">You can then customize the rectangle by specifying different property attributes.</span></span>

<span data-ttu-id="343ec-161">Sie können z. B. ein Rechteck zeichnen, das mit Blau gefüllt ist, indem Sie **fillcolor**="blue" angeben und ihm eine rote 3,5-Punkt-Kontur geben, indem Sie **strokecolor**="red" **strokeweight**="3.5pt" angeben, wie in der folgenden VML-Darstellung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="343ec-161">For example, you can draw a rectangle that is filled with blue by specifying **fillcolor**="blue", and give it a 3.5-point red outline by specifying **strokecolor**="red" **strokeweight**="3.5pt", as shown in the following VML representation:</span></span>

![rect1.gif (485 Bytes)](images/rect1.gif)


```HTML
<v:rect style='width:100pt;height:75pt' fillcolor="blue"
strokecolor="red" strokeweight="3.5pt"/>
```





<span data-ttu-id="343ec-163">Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation.](https://WWW.w3.org/TR/NOTE-VML#-toc416858405)</span><span class="sxs-lookup"><span data-stu-id="343ec-163">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) .</span></span> <span data-ttu-id="343ec-164">(Hinweis: Die VML-Spezifikation enthält kein Lesezeichen für das `<rect>` Element.)</span><span class="sxs-lookup"><span data-stu-id="343ec-164">(Note: The VML specification doesn't have a bookmark for the `<rect>` element.)</span></span>

<span data-ttu-id="343ec-165">[![Zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="343ec-165">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="roundrect"></a><span data-ttu-id="343ec-166">roundrect</span><span class="sxs-lookup"><span data-stu-id="343ec-166">roundrect</span></span>

<span data-ttu-id="343ec-167">Sie können das `<roundrect>` -Element verwenden, um ein Rechteck mit abgerundeten Ecken zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="343ec-167">You can use the `<roundrect>` element to draw a rectangle with rounded corners.</span></span> <span data-ttu-id="343ec-168">Anschließend können Sie das abgerundete Rechteck anpassen, indem Sie verschiedene Eigenschaftsattribute angeben.</span><span class="sxs-lookup"><span data-stu-id="343ec-168">You can then customize the rounded rectangle by specifying different property attributes.</span></span>

<span data-ttu-id="343ec-169">Sie können z. B. ein Rechteck zeichnen, das 30 % der Hälfte der kleineren Dimension des Rechtecks abgerundete Ecken aufweist, indem Sie **arcsize**="0.3" angeben, es mit Gelb füllen, indem Sie **fillcolor**="yellow" angeben, und ihm eine zweipunktige rote Kontur geben, indem Sie **strokecolor**="red" **strokeweight**="2pt" angeben, wie in der folgenden VML-Darstellung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="343ec-169">For example, you can draw a rectangle that has rounded corners 30% of half the smaller dimension of the rectangle by specifying **arcsize**="0.3", fill it with yellow by specifying **fillcolor**="yellow", and give it a 2-point red outline by specifying **strokecolor**="red" **strokeweight**="2pt", as shown in the following VML representation:</span></span>

![roundrect1.gif (622 Bytes)](images/roundrect1.gif)


```HTML
<v:roundrect style='width:100pt;height:75pt"
arcsize="0.3" fillcolor="yellow"
strokecolor="red" strokeweight="2pt"/>
```





<span data-ttu-id="343ec-171">Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation.](https://WWW.w3.org/TR/NOTE-VML#-toc416858405)</span><span class="sxs-lookup"><span data-stu-id="343ec-171">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) .</span></span>

<span data-ttu-id="343ec-172">[![Zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="343ec-172">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="line"></a><span data-ttu-id="343ec-173">line</span><span class="sxs-lookup"><span data-stu-id="343ec-173">line</span></span>

<span data-ttu-id="343ec-174">Sie können das `<line>` -Element verwenden, um eine gerade Linie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="343ec-174">You can use the `<line>` element to create a straight line.</span></span> <span data-ttu-id="343ec-175">Anschließend können Sie die Zeile anpassen, indem Sie verschiedene Eigenschaftsattribute angeben.</span><span class="sxs-lookup"><span data-stu-id="343ec-175">You can then customize the line by specifying different property attributes.</span></span>

<span data-ttu-id="343ec-176">Sie können z. B. eine horizontale Linie zeichnen, indem Sie **von**="20pt,20pt" **bis**="100pt,20pt" angeben und sie 2 Punkt und Rot machen, indem Sie **strokecolor**="red" **strokeweight**="2pt" angeben, wie in der folgenden VML-Darstellung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="343ec-176">For example, you can draw a horizontal line by specifying **from**="20pt,20pt" **to**="100pt,20pt", and make it 2-point and red by specifying **strokecolor**="red" **strokeweight**="2pt", as shown in the following VML representation:</span></span>

![line1.gif (88 Byte)](images/line1.gif)


```HTML
<v:line from="20pt,20pt" to="100pt,20pt" '
strokecolor="red" strokeweight="2pt">
```





<span data-ttu-id="343ec-178">Sie können eine vertikale oder diagonale Linie zeichnen, indem Sie einfach unterschiedliche Werte für die Eigenschaftenattribute **from** und **to** angeben, wie in der folgenden VML-Darstellung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="343ec-178">You can draw a vertical or diagonal line by simply specifying different values for the **from** and **to** property attributes, as shown in the following VML representation:</span></span>

![line2.gif (86 Bytes)](images/line2.gif)


```HTML
<v:line from="20pt,20pt" to="20pt,100pt"
strokecolor="red" strokeweight="2pt">
```





<span data-ttu-id="343ec-180">Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation.](https://WWW.w3.org/TR/NOTE-VML#-toc416858402)</span><span class="sxs-lookup"><span data-stu-id="343ec-180">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858402) .</span></span>

<span data-ttu-id="343ec-181">[![Zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="343ec-181">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="polyline"></a><span data-ttu-id="343ec-182">Polylinie</span><span class="sxs-lookup"><span data-stu-id="343ec-182">polyline</span></span>

<span data-ttu-id="343ec-183">Sie können das `<polyline>` -Element verwenden, um Formen zu definieren, die aus verbundenen Liniensegmenten erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="343ec-183">You can use the `<polyline>` element to define shapes that are created from connected line segments.</span></span> <span data-ttu-id="343ec-184">Anschließend können Sie die Form anpassen, indem Sie verschiedene Eigenschaftsattribute angeben.</span><span class="sxs-lookup"><span data-stu-id="343ec-184">You can then customize the shape by specifying different property attributes.</span></span>

<span data-ttu-id="343ec-185">Um beispielsweise die in der folgenden Abbildung dargestellte Form zu zeichnen, können Sie die folgende VML-Darstellung eingeben:</span><span class="sxs-lookup"><span data-stu-id="343ec-185">For example, to draw the shape shown in the following picture, you can type the following VML representation:</span></span>

![polyline1.gif (957 Bytes)](images/polyline1.gif)


```HTML
<v:polyline points="18pt,54pt,90pt,-9pt,180pt,63pt,261pt,27pt"
strokecolor="red" strokeweight="2pt"/>
```





<span data-ttu-id="343ec-187">Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation.](https://WWW.w3.org/TR/NOTE-VML#-toc416858403)</span><span class="sxs-lookup"><span data-stu-id="343ec-187">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858403) .</span></span>

<span data-ttu-id="343ec-188">[![Zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="343ec-188">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="curve"></a><span data-ttu-id="343ec-189">Kurve</span><span class="sxs-lookup"><span data-stu-id="343ec-189">curve</span></span>

<span data-ttu-id="343ec-190">Sie können das `<curve>` -Element verwenden, um eine kubische Bézierkurve zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="343ec-190">You can use the `<curve>` element to draw a cubic bézier curve.</span></span> <span data-ttu-id="343ec-191">Anschließend können Sie die Kurve anpassen, indem Sie verschiedene Eigenschaftsattribute angeben.</span><span class="sxs-lookup"><span data-stu-id="343ec-191">You can then customize the curve by specifying different property attributes.</span></span>

<span data-ttu-id="343ec-192">Um z. B. eine Kurve wie in der folgenden Abbildung zu zeichnen, können Sie die folgende VML-Darstellung eingeben:</span><span class="sxs-lookup"><span data-stu-id="343ec-192">For example, to draw a curve as shown in the following picture, you can type the following VML representation:</span></span>

![curve1.gif (992 Bytes)](images/curve1.gif)


```HTML
<v:curve style='position:relative'
from="0,0" control1="100pt,100pt" control2="200pt,100pt"
to="300pt,0" strokecolor="red" strokeweight="3pt"/>
```





<span data-ttu-id="343ec-194">Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation.](https://WWW.w3.org/TR/NOTE-VML#-toc416858404)</span><span class="sxs-lookup"><span data-stu-id="343ec-194">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858404) .</span></span>

<span data-ttu-id="343ec-195">[![Zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="343ec-195">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="arc"></a><span data-ttu-id="343ec-196">Bogen</span><span class="sxs-lookup"><span data-stu-id="343ec-196">arc</span></span>

<span data-ttu-id="343ec-197">Sie können das `<arc>` -Element verwenden, um einen Bogen zu zeichnen, der als Segment eines Ovals definiert ist.</span><span class="sxs-lookup"><span data-stu-id="343ec-197">You can use the `<arc>` element to draw an arc that is defined as a segment of an oval.</span></span> <span data-ttu-id="343ec-198">Der Bogen wird durch die Schnittmenge des Ovals mit den durch die Winkel angegebenen Start- und Endradiusvektoren definiert.</span><span class="sxs-lookup"><span data-stu-id="343ec-198">The arc is defined by the intersection of the oval with the start and end radius vectors given by the angles.</span></span> <span data-ttu-id="343ec-199">Die Winkel werden mithilfe der Eigenschaften eines Kreises (Breite gleich Höhe) berechnet und dann anisotrop auf die gewünschte Breite und Höhe skaliert.</span><span class="sxs-lookup"><span data-stu-id="343ec-199">The angles are calculated by using the properties of a circle (width equal to height), then scaled anisotropically to the desired width and height.</span></span>

<span data-ttu-id="343ec-200">Beispielsweise können Sie einen Bogen zeichnen, der bei 0 Grad beginnt und bei 90 Grad endet, indem Sie **startangle**="0" **endangle**="90" angeben, wie in der folgenden VML-Darstellung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="343ec-200">For example, you can draw an arc that starts at 0 degrees and ends at 90 degrees by specifying **startangle**="0" **endangle**="90", as shown in the following VML representation:</span></span>

![arc1.gif (410 Bytes)](images/arc1.gif)


```HTML
<v:arc style='width:100pt;height:100pt'
startangle="0" endangle="90"
strokecolor="red" strokeweight="2pt"/>
```





<span data-ttu-id="343ec-202">Sie können den Bogen ändern, indem Sie verschiedene **Startangle-** und **Endangle-Werte** angeben, wie in der folgenden VML-Darstellung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="343ec-202">You can change the arc by specifying different **startangle** and **endangle** values, as shown in the following VML representation:</span></span>

![arc2.gif (608 Bytes)](images/arc2.gif)


```HTML
<v:arc style='width:100pt;height:100pt'
startangle="0" endangle="180"
strokecolor="red" strokeweight="2pt"/>
```





![arc3.gif (807 Bytes)](images/arc3.gif)


```HTML
<v:arc style='width:100pt;height:100pt'
startangle="0" endangle="270"
strokecolor="red" strokeweight="2pt"/>
```





<span data-ttu-id="343ec-205">Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation.](https://WWW.w3.org/TR/NOTE-VML#-toc416858407)</span><span class="sxs-lookup"><span data-stu-id="343ec-205">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858407) .</span></span>

<span data-ttu-id="343ec-206">[![Zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="343ec-206">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="343ec-207">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="343ec-207">Summary</span></span>

<span data-ttu-id="343ec-208">Sie können vordefinierte VML-Elemente wie `<oval>` , , , , , und `<line>` `<polyline>` `<curve>` `<rect>` `<roundrect>` `<arc>` verwenden, um Grafiken einfach auf einer Webseite zu zeichnen und diese Grafiken dann anzupassen, indem Sie einfach ihre Eigenschaftenattribute ändern.</span><span class="sxs-lookup"><span data-stu-id="343ec-208">You can use VML predefined elements such as `<oval>`, `<line>`, `<polyline>`, `<curve>`, `<rect>`, `<roundrect>`, and `<arc>` to easily draw graphics on a Web page, and then customize those graphics by simply changing their property attributes.</span></span>

 

 