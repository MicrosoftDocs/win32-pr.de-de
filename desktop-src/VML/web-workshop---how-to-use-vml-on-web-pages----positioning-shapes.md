---
title: Positionieren von Formen
description: In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.
ms.assetid: dbd68f54-201a-48dc-a3a9-a8dd42178c11
keywords:
- Webworkshop, Positionieren von Formen
- Entwerfen von Webseiten, Positionieren von Formen
- Vector Markup Language (VML), Positionieren von Formen
- VML (Vector Markup Language), Positionieren von Formen
- Vektorgrafiken, Positionierungs Formen
- VML-Formen, positionieren
- Positionieren von Formen
- Vector Markup Language (VML), statischer Positions Stil
- VML (Vector Markup Language), statischer Positions Stil
- Vektorgrafiken, statischer Positions Stil
- statischer Positions Stil
- Vector Markup Language (VML), relativer Positions Stil
- VML (Vector Markup Language), relativer Positions Stil
- Vektorgrafiken, relativer Positions Stil
- relativer Positions Stil
- Vector Markup Language (VML), absoluter Positions Stil
- VML (Vector Markup Language), absoluter Positions Stil
- Vektorgrafiken, absoluter Positions Stil
- absoluter Positions Stil
- Vector Markup Language (VML), z-Index-Positions Stil
- VML (Vector Markup Language), z-Index-Positions Stil
- Vektorgrafiken, z-Index Positions Stil
- z-Index-Positions Stil
- Vector Markup Language (VML), Drehungs Positions Stil
- VML (Vector Markup Language), Drehungs Positions Stil
- Vektorgrafiken, Drehungs Positions Stil
- Stil der Drehungs Position
- Vector Markup Language (VML), drehpositions Stil
- VML (Vector Markup Language), Flip-Positions Stil
- Vektorgrafiken, drehpositions Stil
- Positions Stil kippen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd8e01d0c7962467b1894f0f4c2c6cd1f6b01509
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039147"
---
# <a name="positioning-shapes"></a><span data-ttu-id="55ce3-135">Positionieren von Formen</span><span class="sxs-lookup"><span data-stu-id="55ce3-135">Positioning Shapes</span></span>

<span data-ttu-id="55ce3-136">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="55ce3-136">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="55ce3-137">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="55ce3-137">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="55ce3-138">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="55ce3-138">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="55ce3-139">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="55ce3-139">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="55ce3-140">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="55ce3-140">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="55ce3-141">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="55ce3-141">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="55ce3-142">Sie haben gelernt, wie Formen mithilfe von VML auf einer Webseite gezeichnet werden können.</span><span class="sxs-lookup"><span data-stu-id="55ce3-142">You've learned how to draw and color shapes on a Web page using VML.</span></span> <span data-ttu-id="55ce3-143">In diesem Thema verwenden Sie VML zum genauen Positionieren von Grafiken auf einer Webseite.</span><span class="sxs-lookup"><span data-stu-id="55ce3-143">In this topic, you'll use VML to precisely position graphics on a Web page.</span></span>

<span data-ttu-id="55ce3-144">VML verwendet dieselbe Syntax, die in den Abschnitten " [Box Model](https://www.w3.org/TR/PR-CSS2/box.mdl) " und " [Visual Rendering Model](https://www.w3.org/TR/PR-CSS2/visuren.mdl) " von [CSS2](https://www.w3.org/TR/PR-CSS2/) definiert ist, um Formen auf einer Webseite zu positionieren.</span><span class="sxs-lookup"><span data-stu-id="55ce3-144">VML uses the same syntax defined in the [Box Model](https://www.w3.org/TR/PR-CSS2/box.mdl) and [Visual Rendering Model](https://www.w3.org/TR/PR-CSS2/visuren.mdl) sections of [CSS2](https://www.w3.org/TR/PR-CSS2/) to position shapes on a Web page.</span></span> <span data-ttu-id="55ce3-145">Sie können " [static](#static)", " [relative](#relative)" oder " [absolute](#absolute) " verwenden, um zu bestimmen, wo sich der Basispunkt auf einer Webseite befindet.</span><span class="sxs-lookup"><span data-stu-id="55ce3-145">You can use [static](#static), [relative](#relative), or [absolute](#absolute) to determine where the base point is located on a Web page.</span></span> <span data-ttu-id="55ce3-146">Anschließend können Sie die Attribute **Top** und **left** Style verwenden, um den Offset von dem Basispunkt anzugeben, an dem das enthaltende Feld für die Form positioniert wird.</span><span class="sxs-lookup"><span data-stu-id="55ce3-146">You can then use the **top** and **left** style attributes to specify the offset from the base point at which the containing box for the shape will be positioned.</span></span>

<span data-ttu-id="55ce3-147">Sie können [z-Index](#z-index) auch verwenden, um die z-Reihenfolge von Formen auf einer Webseite anzugeben.</span><span class="sxs-lookup"><span data-stu-id="55ce3-147">You can also use [z-index](#z-index) to specify the z-order of shapes on a Web page.</span></span>

<span data-ttu-id="55ce3-148">Außerdem bietet VML [Drehung](#rotation) und [kippen](#flip) zum Drehen und Kippen von Formen.</span><span class="sxs-lookup"><span data-stu-id="55ce3-148">In addition, VML provides [rotation](#rotation) and [flip](#flip) to rotate or flip shapes.</span></span>

<span data-ttu-id="55ce3-149">In diesem Thema:</span><span class="sxs-lookup"><span data-stu-id="55ce3-149">In this topic:</span></span>

-   [<span data-ttu-id="55ce3-150">static</span><span class="sxs-lookup"><span data-stu-id="55ce3-150">static</span></span>](#static)
-   [<span data-ttu-id="55ce3-151">relative</span><span class="sxs-lookup"><span data-stu-id="55ce3-151">relative</span></span>](#relative)
-   [<span data-ttu-id="55ce3-152">absolute</span><span class="sxs-lookup"><span data-stu-id="55ce3-152">absolute</span></span>](#absolute)
-   [<span data-ttu-id="55ce3-153">z-index</span><span class="sxs-lookup"><span data-stu-id="55ce3-153">z-index</span></span>](#z-index)
-   [<span data-ttu-id="55ce3-154">Rotations</span><span class="sxs-lookup"><span data-stu-id="55ce3-154">rotation</span></span>](#rotation)
-   [<span data-ttu-id="55ce3-155">flip</span><span class="sxs-lookup"><span data-stu-id="55ce3-155">flip</span></span>](#flip)
-   [<span data-ttu-id="55ce3-156">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="55ce3-156">Summary</span></span>](#summary)

## <a name="static"></a><span data-ttu-id="55ce3-157">static</span><span class="sxs-lookup"><span data-stu-id="55ce3-157">static</span></span>

<span data-ttu-id="55ce3-158">Der Standard Positions Stil ist statisch, wodurch Browser angewiesen werden, die Form am aktuellen Punkt (dem Basispunkt) im Text Fluss zu positionieren und die Einstellungen in den Attributen **Top** und **left** Style zu ignorieren.</span><span class="sxs-lookup"><span data-stu-id="55ce3-158">The default position style is static, which instructs browsers to position the shape at the current point (the base point) in the text flow and ignore the settings in the **top** and **left** style attributes.</span></span>

<span data-ttu-id="55ce3-159">In der folgenden VML-Darstellung wird das rote Oval z. b. unmittelbar nach dem Text "Anfang der Form:" positioniert, wie in der folgenden Abbildung dargestellt:</span><span class="sxs-lookup"><span data-stu-id="55ce3-159">For example, in the following VML representation, the red oval is positioned immediately after the text "Beginning of the shape:", as shown in the following picture:</span></span>

![shape1 \-ps.gif (2123 Bytes)](images/shape1-ps.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='width:80pt;height:90pt' fillcolor="red" />
End.
</body>
```





<span data-ttu-id="55ce3-161">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="55ce3-161">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="relative"></a><span data-ttu-id="55ce3-162">relative</span><span class="sxs-lookup"><span data-stu-id="55ce3-162">relative</span></span>

<span data-ttu-id="55ce3-163">Wenn Sie das Positions Stil Attribut auf "relative" festlegen, können Sie das enthaltende Feld mit einem Offset vom aktuellen Punkt (dem Basispunkt) im Text Fluss platzieren.</span><span class="sxs-lookup"><span data-stu-id="55ce3-163">Setting the position style attribute to "relative" allows you to place the containing box with an offset from the current point (the base point) in the text flow.</span></span> <span data-ttu-id="55ce3-164">Der Offset wird durch die Einstellungen in den Attributen **Top** und **left** Style festgelegt.</span><span class="sxs-lookup"><span data-stu-id="55ce3-164">The offset is determined by the settings in the **top** and **left** style attributes.</span></span> <span data-ttu-id="55ce3-165">Beachten Sie, dass das als relativ positionierte enthaltende Feld Speicherplatz im Text Fluss einnimmt.</span><span class="sxs-lookup"><span data-stu-id="55ce3-165">Be aware that the containing box that is positioned as relative takes up space in the text flow.</span></span>

<span data-ttu-id="55ce3-166">Beispielsweise wird in der folgenden VML-Darstellung das rote Oval 20 Punkte von Links und 10 Punkte vom oberen Rand bis zum aktuellen Punkt im Text Fluss positioniert, wie in der folgenden Abbildung dargestellt:</span><span class="sxs-lookup"><span data-stu-id="55ce3-166">For example, in the following VML representation, the red oval is positioned 20 points from the left and 10 points from the top relative to the current point in the text flow, as shown in the following picture:</span></span>

![shape3.gif (2048 Bytes)](images/shape3.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt;width:80pt;
height:90pt;' fillcolor="red" />
End.
</body>
```





<span data-ttu-id="55ce3-168">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="55ce3-168">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="absolute"></a><span data-ttu-id="55ce3-169">absolute</span><span class="sxs-lookup"><span data-stu-id="55ce3-169">absolute</span></span>

<span data-ttu-id="55ce3-170">Wenn Sie das Positions Format Attribut auf "absolute" festlegen, können Sie das enthaltende Feld mit einer exakten Entfernung von der oberen linken Ecke (dem Basispunkt) des übergeordneten Elements (dem positionierten Element, das die Form enthält) platzieren.</span><span class="sxs-lookup"><span data-stu-id="55ce3-170">Setting the position style attribute to "absolute" allows you to place the containing box an exact distance from the top left corner (the base point) of its parent element (the positioned element that contains the shape).</span></span> <span data-ttu-id="55ce3-171">Beachten Sie, dass das als absolut positionierte enthaltende Feld keinen Speicherplatz im Text Fluss belegt.</span><span class="sxs-lookup"><span data-stu-id="55ce3-171">Be aware that the containing box that is positioned as absolute doesn't take up space in the text flow.</span></span>

<span data-ttu-id="55ce3-172">In der folgenden VML-Darstellung ist das rote Oval z. b. im- `<body>` Element (der gesamten Webseite) enthalten. Daher befindet sich der Basispunkt in der linken oberen Ecke der Webseite.</span><span class="sxs-lookup"><span data-stu-id="55ce3-172">For example, in the following VML representation, the red oval is contained within the `<body>` element (the entire Web page); therefore, the base point is at the top left corner of the Web page.</span></span> <span data-ttu-id="55ce3-173">Das enthaltende Feld für das Oval ist genau 20 Punkte von der linken Seite und 10 Punkte von oben, relativ zur oberen linken Ecke der Webseite positioniert, wie in der folgenden Abbildung dargestellt:</span><span class="sxs-lookup"><span data-stu-id="55ce3-173">The containing box for the oval is positioned exactly 20 points from the left and 10 points from the top, relative to the top left corner of the Web page, as shown in the following picture:</span></span>

![shape2.gif (2006 Bytes)](images/shape2.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt
width:80pt; height:90pt;' fillcolor="red" />
End.
</body>
```





<span data-ttu-id="55ce3-175">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="55ce3-175">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="z-index"></a><span data-ttu-id="55ce3-176">z-index</span><span class="sxs-lookup"><span data-stu-id="55ce3-176">z-index</span></span>

<span data-ttu-id="55ce3-177">Es ist möglich, eine Form zu positionieren, die eine andere Form überlappt.</span><span class="sxs-lookup"><span data-stu-id="55ce3-177">It is possible to position a shape that overlaps another shape.</span></span> <span data-ttu-id="55ce3-178">Normalerweise wird die im HTML-Code zuletzt aufgeführte Grafik im oberen Bereich angezeigt.</span><span class="sxs-lookup"><span data-stu-id="55ce3-178">Normally, the graphic that is listed last in the HTML code appears on top.</span></span>

<span data-ttu-id="55ce3-179">In VML können Sie die z-Reihenfolge steuern, indem Sie das **z-Index-** Format Attribut verwenden.</span><span class="sxs-lookup"><span data-stu-id="55ce3-179">In VML, you can control the z-order by using the **z-index** style attribute.</span></span> <span data-ttu-id="55ce3-180">Der Wert dieses Attributs kann 0 (null), eine positive Ganzzahl oder eine negative Ganzzahl sein.</span><span class="sxs-lookup"><span data-stu-id="55ce3-180">The value of this attribute can be zero, a positive integer, or a negative integer.</span></span> <span data-ttu-id="55ce3-181">Die Grafik mit einem größeren z-index-Wert wird auf der Grafik mit einem kleineren z-index-Wert angezeigt.</span><span class="sxs-lookup"><span data-stu-id="55ce3-181">The graphic that has a larger z-index value is displayed on top of the graphic that has a smaller z-index value.</span></span> <span data-ttu-id="55ce3-182">Wenn beide Grafiken denselben z-index-Wert aufweisen, wird die Grafik, die zuletzt im HTML-Code aufgeführt ist, oben angezeigt.</span><span class="sxs-lookup"><span data-stu-id="55ce3-182">When both graphics have the same z-index value, the graphic that is listed last in the HTML code appears on top.</span></span>

<span data-ttu-id="55ce3-183">In der folgenden VML-Darstellung wird das rote Oval beispielsweise oberhalb des blauen Rechtecks angezeigt.</span><span class="sxs-lookup"><span data-stu-id="55ce3-183">For example, in the following VML representation, the red oval is displayed on top of the blue rectangle.</span></span> <span data-ttu-id="55ce3-184">Dies liegt daran, dass der z-index-Wert des roten Oval größer ist als der z-index-Wert des blauen Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="55ce3-184">This is because the z-index value of the red oval is greater than the z-index value of the blue rectangle.</span></span>

![shape4.gif (572 Bytes)](images/shape4.gif)


```HTML
<v:oval
style='position:relative;left:10pt;top:20pt;width:100pt; height:80pt;z-index: 1'
fillcolor="red" />
<v:rect style='position:relative;left:10pt;top:45pt;width:100pt; height:80pt; z-index:0' fillcolor="blue" />
```





<span data-ttu-id="55ce3-186">Wenn Sie den z-Index ändern, wie in der folgenden VML-Darstellung gezeigt, würde sich das rote Oval hinter das blaue Rechteck bewegen.</span><span class="sxs-lookup"><span data-stu-id="55ce3-186">If you change the z-index, as shown in the following VML representation, the red oval would move behind the blue rectangle.</span></span>

![shape5.gif (469 bytes)](images/shape5.gif)


```HTML
<v:oval
style='position:relative;left:10pt;top:20pt;width:100pt; height:80pt;z-index:0'
fillcolor="red" />
<v:rect style='position:relative;left:10pt;top:45pt;width:100pt; height:80pt;z-index:1'
fillcolor="blue" />
```





<span data-ttu-id="55ce3-188">Wenn Sie eine negative ganze Zahl angeben, können Sie z-Index verwenden, um Grafiken hinter dem normalen Text Fluss zu positionieren, wie in der folgenden VML-Darstellung gezeigt.</span><span class="sxs-lookup"><span data-stu-id="55ce3-188">If you supply a negative integer, you can use z-index to position graphics behind the normal text flow, as shown in the following VML representation.</span></span>

![shape6.gif (2125 Bytes)](images/shape6.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt;z-index:-1;
width:80pt;height:90pt;' fillcolor="red" />
End.
</body>
```





<span data-ttu-id="55ce3-190">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="55ce3-190">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="rotation"></a><span data-ttu-id="55ce3-191">Drehung</span><span class="sxs-lookup"><span data-stu-id="55ce3-191">rotation</span></span>

<span data-ttu-id="55ce3-192">Mithilfe des Attributs " **Rotation** " können Sie angeben, wie viele Grad eine Form auf der Achse aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="55ce3-192">You can use the **rotation** style attribute to specify how many degrees you want a shape to turn on its axis.</span></span> <span data-ttu-id="55ce3-193">Ein positiver Wert weist auf eine Drehung im Uhrzeigersinn hin. ein negativer Wert gibt eine Drehung gegen den Uhrzeigersinn an.</span><span class="sxs-lookup"><span data-stu-id="55ce3-193">A positive value indicates a clockwise rotation; a negative value indicates a counter-clockwise rotation.</span></span>

<span data-ttu-id="55ce3-194">Wenn Sie z. b. **Style**= '... Rotation: 90 ' Sie können die Form 90 Grad im Uhrzeigersinn drehen.</span><span class="sxs-lookup"><span data-stu-id="55ce3-194">For example, if you specify **style**='... rotation:90', you can rotate the shape 90 degrees clockwise.</span></span>

<span data-ttu-id="55ce3-195">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="55ce3-195">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="flip"></a><span data-ttu-id="55ce3-196">flip</span><span class="sxs-lookup"><span data-stu-id="55ce3-196">flip</span></span>

<span data-ttu-id="55ce3-197">Sie können das Attribut " **Flip** Style" verwenden, um eine Form auf der x-oder y-Achse entsprechend der folgenden Tabelle zu kippen:</span><span class="sxs-lookup"><span data-stu-id="55ce3-197">You can use the **flip** style attribute to flip a shape on its x or y axis according to the following table:</span></span>



| <span data-ttu-id="55ce3-198">Wert</span><span class="sxs-lookup"><span data-stu-id="55ce3-198">Value</span></span> | <span data-ttu-id="55ce3-199">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="55ce3-199">Description</span></span>                                                  |
|-------|--------------------------------------------------------------|
| <span data-ttu-id="55ce3-200">x</span><span class="sxs-lookup"><span data-stu-id="55ce3-200">x</span></span>     | <span data-ttu-id="55ce3-201">Drehen der gedrehten Form um die y-Achse (Umkehrung der x-Ordinate)</span><span class="sxs-lookup"><span data-stu-id="55ce3-201">Flip the rotated shape about the y axis (invert x ordinates)</span></span> |
| <span data-ttu-id="55ce3-202">Y</span><span class="sxs-lookup"><span data-stu-id="55ce3-202">y</span></span>     | <span data-ttu-id="55ce3-203">Drehen der gedrehten Form um die x-Achse (y-Ordinate umkehren)</span><span class="sxs-lookup"><span data-stu-id="55ce3-203">Flip the rotated shape about the x axis (invert y ordinates)</span></span> |



 

<span data-ttu-id="55ce3-204">In der Flip-Eigenschaft können sowohl x als auch y angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="55ce3-204">Both x and y may be specified in the flip property.</span></span>

<span data-ttu-id="55ce3-205">Wenn Sie z. b. **Style**= '... Flip: x y ", Sie kippen die Form auf der x-und der y-Achse.</span><span class="sxs-lookup"><span data-stu-id="55ce3-205">For example, if you type **style**='... flip:x y', you will flip the shape on both its x and y axis.</span></span>

<span data-ttu-id="55ce3-206">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="55ce3-206">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="55ce3-207">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="55ce3-207">Summary</span></span>

<span data-ttu-id="55ce3-208">Je nachdem, was Sie gelernt haben, können Sie eine Form genau auf einer Webseite positionieren, indem Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="55ce3-208">Based on what you've learned, you can precisely position a shape on a Web page by following these steps:</span></span>

1.  <span data-ttu-id="55ce3-209">Legen Sie fest, wo die Form auf einer Webseite angezeigt werden soll, und wählen Sie die Größe der Form aus.</span><span class="sxs-lookup"><span data-stu-id="55ce3-209">Decide where you want the shape to appear on a Web page, and the size of the shape.</span></span>
2.  <span data-ttu-id="55ce3-210">Geben Sie **Style**= ' Position: relative (oder relative) ' an, um den Basispunkt zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="55ce3-210">Specify **style**='position:relative (or relative)' to determine the base point.</span></span>
3.  <span data-ttu-id="55ce3-211">Verwenden Sie **Links** und **oben** , um den Offset vom Basispunkt anzugeben.</span><span class="sxs-lookup"><span data-stu-id="55ce3-211">Use **left** and **top** to specify the offset from the base point.</span></span>
4.  <span data-ttu-id="55ce3-212">Verwenden Sie **Width** und **height** , um die Größe des enthaltenden Felds für die Form anzugeben.</span><span class="sxs-lookup"><span data-stu-id="55ce3-212">Use **width** and **height** to specify the size of the containing box for the shape.</span></span>
5.  <span data-ttu-id="55ce3-213">Verwenden Sie **z-Index** , um die z-Reihenfolge der Form anzugeben.</span><span class="sxs-lookup"><span data-stu-id="55ce3-213">Use **z-index** to specify the z-order of the shape.</span></span>

 

 