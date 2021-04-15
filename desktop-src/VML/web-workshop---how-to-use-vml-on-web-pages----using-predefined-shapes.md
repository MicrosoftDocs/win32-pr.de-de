---
title: Verwenden von vordefinierten Formen
description: In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.
ms.assetid: 9a2e8b5a-b1d0-4a73-b058-24dac1f0b655
keywords:
- Webworkshop, vordefinierte Formen
- Entwerfen von Webseiten, vordefinierte Formen
- Vector Markup Language (VML), vordefinierte Formen
- VML (Vector Markup Language), vordefinierte Formen
- Vektorgrafiken, vordefinierte Formen
- VML-Formen, vordefiniert
- vordefinierte Formen
- Vector Markup Language (VML), Rect-Element
- VML (Vector Markup Language), Rect-Element
- Vektorgrafiken, Rect-Element
- Rect-Element
- VML-Elemente, Rect
- Vector Markup Language (VML), roundRect-Element
- VML (Vector Markup Language), roundRect-Element
- Vektorgrafiken, roundRect-Element
- roundRect-Element
- VML-Elemente, roundRect
- Vector Markup Language (VML), Zeilen Element
- VML (Vector Markup Language), Zeilen Element
- Vektorgrafiken, Zeilen Element
- Line-Element
- VML-Elemente, Zeile
- Vector Markup Language (VML), polylinienelement
- VML (Vector Markup Language), polylinienelement
- Vektorgrafiken, polylinienelement
- Polylinie-Element
- VML-Elemente, Polyline
- Vector Markup Language (VML), Kurven Element
- VML (Vector Markup Language), Kurven Element
- Vektorgrafiken, Kurven Element
- Kurven Element
- VML-Elemente, Kurve
- Vector Markup Language (VML), Bogen Element
- VML (Vector Markup Language), Bogen Element
- Vektorgrafiken, Bogen Element
- Arc-Element
- VML-Elemente, Bogen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c1cafacf00f6f3f9129c29c56837f3f485aa3a3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516883"
---
# <a name="using-predefined-shapes"></a><span data-ttu-id="ad9af-141">Verwenden von vordefinierten Formen</span><span class="sxs-lookup"><span data-stu-id="ad9af-141">Using Predefined Shapes</span></span>

<span data-ttu-id="ad9af-142">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="ad9af-142">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ad9af-143">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="ad9af-143">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ad9af-144">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="ad9af-144">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ad9af-145">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="ad9af-145">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ad9af-146">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="ad9af-146">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ad9af-147">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="ad9af-147">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ad9af-148">Wie Sie gelernt haben, können Sie das- `<oval>` Element von VML verwenden, um ein einfaches Oval zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ad9af-148">As you've learned, you can use the `<oval>` element of VML to create a simple oval.</span></span> <span data-ttu-id="ad9af-149">VML bietet mehrere weitere vordefinierte Elemente.</span><span class="sxs-lookup"><span data-stu-id="ad9af-149">VML provides several other predefined elements.</span></span> <span data-ttu-id="ad9af-150">In diesem Thema wird veranschaulicht, wie Grafiken mithilfe dieser Elemente gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="ad9af-150">In this topic, we will illustrate how to draw graphics by using these elements.</span></span>

<span data-ttu-id="ad9af-151">In diesem Thema:</span><span class="sxs-lookup"><span data-stu-id="ad9af-151">In this topic:</span></span>

-   [<span data-ttu-id="ad9af-152">Rect</span><span class="sxs-lookup"><span data-stu-id="ad9af-152">rect</span></span>](#roundrect)
-   [<span data-ttu-id="ad9af-153">roundRect</span><span class="sxs-lookup"><span data-stu-id="ad9af-153">roundrect</span></span>](#roundrect)
-   [<span data-ttu-id="ad9af-154">line</span><span class="sxs-lookup"><span data-stu-id="ad9af-154">line</span></span>](#polyline)
-   [<span data-ttu-id="ad9af-155">Polylinie</span><span class="sxs-lookup"><span data-stu-id="ad9af-155">polyline</span></span>](#polyline)
-   [<span data-ttu-id="ad9af-156">Kurve</span><span class="sxs-lookup"><span data-stu-id="ad9af-156">curve</span></span>](#curve)
-   [<span data-ttu-id="ad9af-157">Bogen</span><span class="sxs-lookup"><span data-stu-id="ad9af-157">arc</span></span>](#arc)
-   [<span data-ttu-id="ad9af-158">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="ad9af-158">Summary</span></span>](#summary)

## <a name="rect"></a><span data-ttu-id="ad9af-159">rect</span><span class="sxs-lookup"><span data-stu-id="ad9af-159">rect</span></span>

<span data-ttu-id="ad9af-160">Sie können das- `<rect>` Element verwenden, um ein Rechteck zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="ad9af-160">You can use the `<rect>` element to draw a rectangle.</span></span> <span data-ttu-id="ad9af-161">Anschließend können Sie das Rechteck anpassen, indem Sie unterschiedliche Eigenschafts Attribute angeben.</span><span class="sxs-lookup"><span data-stu-id="ad9af-161">You can then customize the rectangle by specifying different property attributes.</span></span>

<span data-ttu-id="ad9af-162">Beispielsweise können Sie ein Rechteck zeichnen, das mit blau gefüllt ist, indem Sie **FillColor**= "Blue" angeben und ihm eine rote Gliederung mit 3,5 Punkten geben, indem Sie " **strokeColor**=" Red " **strokeweight**=" 3.5 pt "angeben, wie in der folgenden VML-Darstellung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="ad9af-162">For example, you can draw a rectangle that is filled with blue by specifying **fillcolor**="blue", and give it a 3.5-point red outline by specifying **strokecolor**="red" **strokeweight**="3.5pt", as shown in the following VML representation:</span></span>

![rect1.gif (485 bytes)](images/rect1.gif)


```HTML
<v:rect style='width:100pt;height:75pt' fillcolor="blue"
strokecolor="red" strokeweight="3.5pt"/>
```





<span data-ttu-id="ad9af-164">Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) .</span><span class="sxs-lookup"><span data-stu-id="ad9af-164">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) .</span></span> <span data-ttu-id="ad9af-165">(Hinweis: die VML-Spezifikation weist kein Lesezeichen für das `<rect>` Element auf.)</span><span class="sxs-lookup"><span data-stu-id="ad9af-165">(Note: The VML specification doesn't have a bookmark for the `<rect>` element.)</span></span>

<span data-ttu-id="ad9af-166">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="ad9af-166">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="roundrect"></a><span data-ttu-id="ad9af-167">roundRect</span><span class="sxs-lookup"><span data-stu-id="ad9af-167">roundrect</span></span>

<span data-ttu-id="ad9af-168">Sie können das- `<roundrect>` Element verwenden, um ein Rechteck mit abgerundeten Ecken zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="ad9af-168">You can use the `<roundrect>` element to draw a rectangle with rounded corners.</span></span> <span data-ttu-id="ad9af-169">Anschließend können Sie das abgerundete Rechteck anpassen, indem Sie unterschiedliche Eigenschafts Attribute angeben.</span><span class="sxs-lookup"><span data-stu-id="ad9af-169">You can then customize the rounded rectangle by specifying different property attributes.</span></span>

<span data-ttu-id="ad9af-170">Sie können z. b. ein Rechteck mit gerundeten Ecken von 30% der Hälfte der kleineren Dimension des Rechtecks zeichnen, indem Sie **arcsize**= "0,3" angeben, geben Sie den Wert gelb durch Angabe von **FillColor**= "Yellow" ein, und weisen Sie ihm einen zwei-Punkt-roten Umriss zu, indem Sie " **strokeColor**=" Red " **strokeweight**=" 2pt "angeben, wie in der folgenden VML-Darstellung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="ad9af-170">For example, you can draw a rectangle that has rounded corners 30% of half the smaller dimension of the rectangle by specifying **arcsize**="0.3", fill it with yellow by specifying **fillcolor**="yellow", and give it a 2-point red outline by specifying **strokecolor**="red" **strokeweight**="2pt", as shown in the following VML representation:</span></span>

![roundrect1.gif (622 Bytes)](images/roundrect1.gif)


```HTML
<v:roundrect style='width:100pt;height:75pt"
arcsize="0.3" fillcolor="yellow"
strokecolor="red" strokeweight="2pt"/>
```





<span data-ttu-id="ad9af-172">Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) .</span><span class="sxs-lookup"><span data-stu-id="ad9af-172">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) .</span></span>

<span data-ttu-id="ad9af-173">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="ad9af-173">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="line"></a><span data-ttu-id="ad9af-174">line</span><span class="sxs-lookup"><span data-stu-id="ad9af-174">line</span></span>

<span data-ttu-id="ad9af-175">Sie können das- `<line>` Element verwenden, um eine gerade Linie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ad9af-175">You can use the `<line>` element to create a straight line.</span></span> <span data-ttu-id="ad9af-176">Anschließend können Sie die Zeile anpassen, indem Sie unterschiedliche Eigenschafts Attribute angeben.</span><span class="sxs-lookup"><span data-stu-id="ad9af-176">You can then customize the line by specifying different property attributes.</span></span>

<span data-ttu-id="ad9af-177">Sie können z. b. eine horizontale Linie zeichnen, indem Sie **from**= "20pt, 20pt" **to**= "100pt, 20pt" angeben und Sie durch Angabe von " **strokeColor**=" Red " **strokeweight**=" 2pt "in der folgenden VML-Darstellung als 2-Punkt und Rot festlegen</span><span class="sxs-lookup"><span data-stu-id="ad9af-177">For example, you can draw a horizontal line by specifying **from**="20pt,20pt" **to**="100pt,20pt", and make it 2-point and red by specifying **strokecolor**="red" **strokeweight**="2pt", as shown in the following VML representation:</span></span>

![line1.gif (88 Bytes)](images/line1.gif)


```HTML
<v:line from="20pt,20pt" to="100pt,20pt" '
strokecolor="red" strokeweight="2pt">
```





<span data-ttu-id="ad9af-179">Sie können eine vertikale oder diagonal Linie zeichnen, indem Sie einfach unterschiedliche Werte für die Attribute **from** und **to** Property angeben, wie in der folgenden VML-Darstellung dargestellt:</span><span class="sxs-lookup"><span data-stu-id="ad9af-179">You can draw a vertical or diagonal line by simply specifying different values for the **from** and **to** property attributes, as shown in the following VML representation:</span></span>

![line2.gif (86 Bytes)](images/line2.gif)


```HTML
<v:line from="20pt,20pt" to="20pt,100pt"
strokecolor="red" strokeweight="2pt">
```





<span data-ttu-id="ad9af-181">Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation](https://WWW.w3.org/TR/NOTE-VML#-toc416858402) .</span><span class="sxs-lookup"><span data-stu-id="ad9af-181">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858402) .</span></span>

<span data-ttu-id="ad9af-182">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="ad9af-182">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="polyline"></a><span data-ttu-id="ad9af-183">Polylinie</span><span class="sxs-lookup"><span data-stu-id="ad9af-183">polyline</span></span>

<span data-ttu-id="ad9af-184">Sie können das- `<polyline>` Element verwenden, um Formen zu definieren, die aus verbundenen Liniensegmenten erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="ad9af-184">You can use the `<polyline>` element to define shapes that are created from connected line segments.</span></span> <span data-ttu-id="ad9af-185">Anschließend können Sie die Form anpassen, indem Sie verschiedene Eigenschafts Attribute angeben.</span><span class="sxs-lookup"><span data-stu-id="ad9af-185">You can then customize the shape by specifying different property attributes.</span></span>

<span data-ttu-id="ad9af-186">Wenn Sie z. b. die in der folgenden Abbildung gezeigte Form zeichnen möchten, können Sie die folgende VML-Darstellung eingeben:</span><span class="sxs-lookup"><span data-stu-id="ad9af-186">For example, to draw the shape shown in the following picture, you can type the following VML representation:</span></span>

![polyline1.gif (957 bytes)](images/polyline1.gif)


```HTML
<v:polyline points="18pt,54pt,90pt,-9pt,180pt,63pt,261pt,27pt"
strokecolor="red" strokeweight="2pt"/>
```





<span data-ttu-id="ad9af-188">Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation](https://WWW.w3.org/TR/NOTE-VML#-toc416858403) .</span><span class="sxs-lookup"><span data-stu-id="ad9af-188">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858403) .</span></span>

<span data-ttu-id="ad9af-189">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="ad9af-189">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="curve"></a><span data-ttu-id="ad9af-190">Kurve</span><span class="sxs-lookup"><span data-stu-id="ad9af-190">curve</span></span>

<span data-ttu-id="ad9af-191">Sie können das- `<curve>` Element verwenden, um eine kubische Bézier-Kurve zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="ad9af-191">You can use the `<curve>` element to draw a cubic bézier curve.</span></span> <span data-ttu-id="ad9af-192">Sie können dann die Kurve anpassen, indem Sie verschiedene Eigenschafts Attribute angeben.</span><span class="sxs-lookup"><span data-stu-id="ad9af-192">You can then customize the curve by specifying different property attributes.</span></span>

<span data-ttu-id="ad9af-193">Wenn Sie z. b. eine Kurve zeichnen möchten, wie in der folgenden Abbildung dargestellt, können Sie die folgende VML-Darstellung eingeben:</span><span class="sxs-lookup"><span data-stu-id="ad9af-193">For example, to draw a curve as shown in the following picture, you can type the following VML representation:</span></span>

![curve1.gif (992 bytes)](images/curve1.gif)


```HTML
<v:curve style='position:relative'
from="0,0" control1="100pt,100pt" control2="200pt,100pt"
to="300pt,0" strokecolor="red" strokeweight="3pt"/>
```





<span data-ttu-id="ad9af-195">Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation](https://WWW.w3.org/TR/NOTE-VML#-toc416858404) .</span><span class="sxs-lookup"><span data-stu-id="ad9af-195">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858404) .</span></span>

<span data-ttu-id="ad9af-196">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="ad9af-196">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="arc"></a><span data-ttu-id="ad9af-197">Bogen</span><span class="sxs-lookup"><span data-stu-id="ad9af-197">arc</span></span>

<span data-ttu-id="ad9af-198">Sie können das- `<arc>` Element verwenden, um einen Bogen zu zeichnen, der als Segment eines Oval definiert ist.</span><span class="sxs-lookup"><span data-stu-id="ad9af-198">You can use the `<arc>` element to draw an arc that is defined as a segment of an oval.</span></span> <span data-ttu-id="ad9af-199">Der Bogen wird durch die Schnittmenge des Oval mit den Anfangs-und EndRadius-Vektoren definiert, die von den Winkeln angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ad9af-199">The arc is defined by the intersection of the oval with the start and end radius vectors given by the angles.</span></span> <span data-ttu-id="ad9af-200">Die Winkel werden mithilfe der Eigenschaften eines Kreises (Breite gleich Höhe) berechnet und dann auf die gewünschte Breite und Höhe zentral skaliert.</span><span class="sxs-lookup"><span data-stu-id="ad9af-200">The angles are calculated by using the properties of a circle (width equal to height), then scaled anisotropically to the desired width and height.</span></span>

<span data-ttu-id="ad9af-201">Beispielsweise können Sie einen Bogen zeichnen, der bei 0 Grad beginnt und um 90 Grad endet, indem Sie **Start Angle**= "0" **EndAngle**= "90" angeben, wie in der folgenden VML-Darstellung dargestellt:</span><span class="sxs-lookup"><span data-stu-id="ad9af-201">For example, you can draw an arc that starts at 0 degrees and ends at 90 degrees by specifying **startangle**="0" **endangle**="90", as shown in the following VML representation:</span></span>

![arc1.gif (410 Bytes)](images/arc1.gif)


```HTML
<v:arc style='width:100pt;height:100pt'
startangle="0" endangle="90"
strokecolor="red" strokeweight="2pt"/>
```





<span data-ttu-id="ad9af-203">Sie können den Bogen ändern, indem Sie unterschiedliche **Start Angle** **-und** -Werte angeben, wie in der folgenden VML-Darstellung dargestellt:</span><span class="sxs-lookup"><span data-stu-id="ad9af-203">You can change the arc by specifying different **startangle** and **endangle** values, as shown in the following VML representation:</span></span>

![arc2.gif (608 bytes)](images/arc2.gif)


```HTML
<v:arc style='width:100pt;height:100pt'
startangle="0" endangle="180"
strokecolor="red" strokeweight="2pt"/>
```





![arc3.gif (807 bytes)](images/arc3.gif)


```HTML
<v:arc style='width:100pt;height:100pt'
startangle="0" endangle="270"
strokecolor="red" strokeweight="2pt"/>
```





<span data-ttu-id="ad9af-206">Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation](https://WWW.w3.org/TR/NOTE-VML#-toc416858407) .</span><span class="sxs-lookup"><span data-stu-id="ad9af-206">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858407) .</span></span>

<span data-ttu-id="ad9af-207">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="ad9af-207">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="ad9af-208">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="ad9af-208">Summary</span></span>

<span data-ttu-id="ad9af-209">Sie können vordefinierte VML-Elemente, wie z. b. `<oval>` , `<line>` , `<polyline>` , `<curve>` , `<rect>` , `<roundrect>` und verwenden `<arc>` , um auf einfache Weise Grafiken auf einer Webseite zu zeichnen und diese Grafiken dann anzupassen, indem Sie einfach Ihre Eigenschafts Attribute ändern.</span><span class="sxs-lookup"><span data-stu-id="ad9af-209">You can use VML predefined elements such as `<oval>`, `<line>`, `<polyline>`, `<curve>`, `<rect>`, `<roundrect>`, and `<arc>` to easily draw graphics on a Web page, and then customize those graphics by simply changing their property attributes.</span></span>

 

 