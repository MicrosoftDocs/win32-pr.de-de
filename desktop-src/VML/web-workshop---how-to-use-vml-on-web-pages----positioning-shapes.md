---
title: Positionieren von Formen
description: In diesem Artikel wird die Positionierung von Formen in VML beschrieben, einem Feature, das seit Windows Internet Explorer 9 veraltet ist.
ms.assetid: dbd68f54-201a-48dc-a3a9-a8dd42178c11
keywords:
- Web-Workshop,Positionieren von Formen
- Entwerfen von Webseiten, Positionieren von Formen
- Vector Markup Language (VML), Positionieren von Formen
- VML (Vector Markup Language),Positionieren von Formen
- Vektorgrafiken,Positionieren von Formen
- VML-Formen, Positionierung
- Positionieren von Formen
- Vector Markup Language (VML), statischer Positionsstil
- VML (Vector Markup Language), statischer Positionsstil
- Vektorgrafiken, statischer Positionsstil
- Statischer Positionsstil
- Vector Markup Language (VML), relative Position
- VML (Vector Markup Language),relative Position
- Vektorgrafik, relative Position
- Relative Position
- Vector Markup Language (VML), absolute Position
- VML (Vector Markup Language),absoluter Positionsstil
- Vektorgrafiken, absolute Position
- Absoluter Positionsstil
- Vector Markup Language (VML), Z-Indexpositionsstil
- VML (Vector Markup Language),Z-Indexpositionsstil
- Vektorgrafiken, Z-Indexpositionsstil
- z-index position style
- Vector Markup Language (VML), Drehpositionsstil
- VML (Vector Markup Language), Drehpositionsstil
- Vektorgrafik, Drehpositionsstil
- Drehpositionsstil
- Vector Markup Language (VML), Kipppositionsstil
- VML (Vector Markup Language),FlipPosition Style
- Vektorgrafiken, Kipppositionsstil
- Kipppositionsstil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c96a8de891ed1bbd1b9bfee9eff52ede946247b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407713"
---
# <a name="positioning-shapes"></a><span data-ttu-id="e21cf-134">Positionieren von Formen</span><span class="sxs-lookup"><span data-stu-id="e21cf-134">Positioning Shapes</span></span>

<span data-ttu-id="e21cf-135">In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="e21cf-135">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e21cf-136">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="e21cf-136">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e21cf-137">Seit Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="e21cf-137">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e21cf-138">Daher wird sie nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="e21cf-138">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e21cf-139">Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/)</span><span class="sxs-lookup"><span data-stu-id="e21cf-139">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e21cf-140">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)</span><span class="sxs-lookup"><span data-stu-id="e21cf-140">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e21cf-141">Sie haben gelernt, wie Sie mithilfe von VML Formen auf einer Webseite zeichnen und färben.</span><span class="sxs-lookup"><span data-stu-id="e21cf-141">You've learned how to draw and color shapes on a Web page using VML.</span></span> <span data-ttu-id="e21cf-142">In diesem Thema verwenden Sie VML, um Grafiken genau auf einer Webseite zu positionieren.</span><span class="sxs-lookup"><span data-stu-id="e21cf-142">In this topic, you'll use VML to precisely position graphics on a Web page.</span></span>

<span data-ttu-id="e21cf-143">VML verwendet dieselbe Syntax, die in den Abschnitten [Box Model](https://www.w3.org/TR/PR-CSS2/box.mdl) und Visual [Rendering Model](https://www.w3.org/TR/PR-CSS2/visuren.mdl) von [CSS2](https://www.w3.org/TR/PR-CSS2/) definiert ist, um Formen auf einer Webseite zu positionieren.</span><span class="sxs-lookup"><span data-stu-id="e21cf-143">VML uses the same syntax defined in the [Box Model](https://www.w3.org/TR/PR-CSS2/box.mdl) and [Visual Rendering Model](https://www.w3.org/TR/PR-CSS2/visuren.mdl) sections of [CSS2](https://www.w3.org/TR/PR-CSS2/) to position shapes on a Web page.</span></span> <span data-ttu-id="e21cf-144">Sie können [statische](#static), [relative oder](#relative) [absolute](#absolute) Verwenden, um zu bestimmen, wo sich der Basispunkt auf einer Webseite befindet.</span><span class="sxs-lookup"><span data-stu-id="e21cf-144">You can use [static](#static), [relative](#relative), or [absolute](#absolute) to determine where the base point is located on a Web page.</span></span> <span data-ttu-id="e21cf-145">Sie können dann  die  Attribute oben und links verwenden, um den Offset von dem Basispunkt anzugeben, an dem das enthaltende Feld für die Form positioniert wird.</span><span class="sxs-lookup"><span data-stu-id="e21cf-145">You can then use the **top** and **left** style attributes to specify the offset from the base point at which the containing box for the shape will be positioned.</span></span>

<span data-ttu-id="e21cf-146">Sie können [z-index auch verwenden,](#z-index) um die Z-Reihenfolge von Formen auf einer Webseite anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e21cf-146">You can also use [z-index](#z-index) to specify the z-order of shapes on a Web page.</span></span>

<span data-ttu-id="e21cf-147">Darüber hinaus bietet VML [Drehung und](#rotation) Kippen, um Formen zu drehen oder zu kippen. [](#flip)</span><span class="sxs-lookup"><span data-stu-id="e21cf-147">In addition, VML provides [rotation](#rotation) and [flip](#flip) to rotate or flip shapes.</span></span>

<span data-ttu-id="e21cf-148">In diesem Thema:</span><span class="sxs-lookup"><span data-stu-id="e21cf-148">In this topic:</span></span>

-   [<span data-ttu-id="e21cf-149">static</span><span class="sxs-lookup"><span data-stu-id="e21cf-149">static</span></span>](#static)
-   [<span data-ttu-id="e21cf-150">relative</span><span class="sxs-lookup"><span data-stu-id="e21cf-150">relative</span></span>](#relative)
-   [<span data-ttu-id="e21cf-151">absolute</span><span class="sxs-lookup"><span data-stu-id="e21cf-151">absolute</span></span>](#absolute)
-   [<span data-ttu-id="e21cf-152">z-index</span><span class="sxs-lookup"><span data-stu-id="e21cf-152">z-index</span></span>](#z-index)
-   [<span data-ttu-id="e21cf-153">Drehung</span><span class="sxs-lookup"><span data-stu-id="e21cf-153">rotation</span></span>](#rotation)
-   [<span data-ttu-id="e21cf-154">flip</span><span class="sxs-lookup"><span data-stu-id="e21cf-154">flip</span></span>](#flip)
-   [<span data-ttu-id="e21cf-155">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="e21cf-155">Summary</span></span>](#summary)

## <a name="static"></a><span data-ttu-id="e21cf-156">static</span><span class="sxs-lookup"><span data-stu-id="e21cf-156">static</span></span>

<span data-ttu-id="e21cf-157">Der Standardpositionsstil ist statisch, wodurch Browser angewiesen werden, die Form am aktuellen Punkt (dem  Basispunkt) im Textfluss zu positionieren und die Einstellungen in den Formatattributen oben und links zu ignorieren. </span><span class="sxs-lookup"><span data-stu-id="e21cf-157">The default position style is static, which instructs browsers to position the shape at the current point (the base point) in the text flow and ignore the settings in the **top** and **left** style attributes.</span></span>

<span data-ttu-id="e21cf-158">In der folgenden VML-Darstellung wird das rote Oval beispielsweise direkt nach dem Text "Anfang der Form:" positioniert, wie in der folgenden Abbildung dargestellt:</span><span class="sxs-lookup"><span data-stu-id="e21cf-158">For example, in the following VML representation, the red oval is positioned immediately after the text "Beginning of the shape:", as shown in the following picture:</span></span>

![shape1 \-ps.gif (2123 Bytes)](images/shape1-ps.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='width:80pt;height:90pt' fillcolor="red" />
End.
</body>
```





<span data-ttu-id="e21cf-160">[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="e21cf-160">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="relative"></a><span data-ttu-id="e21cf-161">relative</span><span class="sxs-lookup"><span data-stu-id="e21cf-161">relative</span></span>

<span data-ttu-id="e21cf-162">Wenn Sie das Positionsformatattribut auf "relative" festlegen, können Sie das enthaltende Feld mit einem Offset vom aktuellen Punkt (dem Basispunkt) im Textfluss platzieren.</span><span class="sxs-lookup"><span data-stu-id="e21cf-162">Setting the position style attribute to "relative" allows you to place the containing box with an offset from the current point (the base point) in the text flow.</span></span> <span data-ttu-id="e21cf-163">Der Offset wird durch die Einstellungen in den **Formatattributen oben** und **links** bestimmt.</span><span class="sxs-lookup"><span data-stu-id="e21cf-163">The offset is determined by the settings in the **top** and **left** style attributes.</span></span> <span data-ttu-id="e21cf-164">Beachten Sie, dass das enthaltende Feld, das als relativ positioniert ist, Platz im Textfluss benötigt.</span><span class="sxs-lookup"><span data-stu-id="e21cf-164">Be aware that the containing box that is positioned as relative takes up space in the text flow.</span></span>

<span data-ttu-id="e21cf-165">In der folgenden VML-Darstellung ist das rote Oval z. B. 20 Punkte von links und 10 Punkte von oben relativ zum aktuellen Punkt im Textfluss positioniert, wie in der folgenden Abbildung dargestellt:</span><span class="sxs-lookup"><span data-stu-id="e21cf-165">For example, in the following VML representation, the red oval is positioned 20 points from the left and 10 points from the top relative to the current point in the text flow, as shown in the following picture:</span></span>

![shape3.gif (2048 Bytes)](images/shape3.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt;width:80pt;
height:90pt;' fillcolor="red" />
End.
</body>
```





<span data-ttu-id="e21cf-167">[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="e21cf-167">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="absolute"></a><span data-ttu-id="e21cf-168">absolute</span><span class="sxs-lookup"><span data-stu-id="e21cf-168">absolute</span></span>

<span data-ttu-id="e21cf-169">Wenn Sie das Positionsformatattribut auf "absolut" festlegen, können Sie den enthaltenden Feld genau in einen Abstand von der oberen linken Ecke (dem Basispunkt) des übergeordneten Elements (dem positionierten Element, das die Form enthält) platzieren.</span><span class="sxs-lookup"><span data-stu-id="e21cf-169">Setting the position style attribute to "absolute" allows you to place the containing box an exact distance from the top left corner (the base point) of its parent element (the positioned element that contains the shape).</span></span> <span data-ttu-id="e21cf-170">Beachten Sie, dass das enthaltende Feld, das als absolut positioniert ist, keinen Platz im Textfluss an sich nimmt.</span><span class="sxs-lookup"><span data-stu-id="e21cf-170">Be aware that the containing box that is positioned as absolute doesn't take up space in the text flow.</span></span>

<span data-ttu-id="e21cf-171">In der folgenden VML-Darstellung ist das rote Oval beispielsweise im -Element (die gesamte Webseite) enthalten. Daher befindet sich der Basispunkt in der oberen linken Ecke `<body>` der Webseite.</span><span class="sxs-lookup"><span data-stu-id="e21cf-171">For example, in the following VML representation, the red oval is contained within the `<body>` element (the entire Web page); therefore, the base point is at the top left corner of the Web page.</span></span> <span data-ttu-id="e21cf-172">Das enthaltende Feld für das Oval ist genau 20 Punkte von links und 10 Punkte von oben relativ zur oberen linken Ecke der Webseite positioniert, wie in der folgenden Abbildung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="e21cf-172">The containing box for the oval is positioned exactly 20 points from the left and 10 points from the top, relative to the top left corner of the Web page, as shown in the following picture:</span></span>

![shape2.gif (2006 Bytes)](images/shape2.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt
width:80pt; height:90pt;' fillcolor="red" />
End.
</body>
```





<span data-ttu-id="e21cf-174">[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="e21cf-174">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="z-index"></a><span data-ttu-id="e21cf-175">z-index</span><span class="sxs-lookup"><span data-stu-id="e21cf-175">z-index</span></span>

<span data-ttu-id="e21cf-176">Es ist möglich, eine Form zu positionieren, die eine andere Form überlappt.</span><span class="sxs-lookup"><span data-stu-id="e21cf-176">It is possible to position a shape that overlaps another shape.</span></span> <span data-ttu-id="e21cf-177">Normalerweise wird die Grafik, die zuletzt im HTML-Code aufgeführt ist, oben angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e21cf-177">Normally, the graphic that is listed last in the HTML code appears on top.</span></span>

<span data-ttu-id="e21cf-178">In VML können Sie die Z-Reihenfolge mithilfe des **Z-Index-Formatattributs** steuern.</span><span class="sxs-lookup"><span data-stu-id="e21cf-178">In VML, you can control the z-order by using the **z-index** style attribute.</span></span> <span data-ttu-id="e21cf-179">Der Wert dieses Attributs kann 0 (null), eine positive ganze Zahl oder eine negative ganze Zahl sein.</span><span class="sxs-lookup"><span data-stu-id="e21cf-179">The value of this attribute can be zero, a positive integer, or a negative integer.</span></span> <span data-ttu-id="e21cf-180">Die Grafik mit einem größeren Z-Index-Wert wird oben in der Grafik mit einem kleineren Z-Index-Wert angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e21cf-180">The graphic that has a larger z-index value is displayed on top of the graphic that has a smaller z-index value.</span></span> <span data-ttu-id="e21cf-181">Wenn beide Grafiken denselben Z-Index-Wert haben, wird oben die Grafik angezeigt, die zuletzt im HTML-Code aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="e21cf-181">When both graphics have the same z-index value, the graphic that is listed last in the HTML code appears on top.</span></span>

<span data-ttu-id="e21cf-182">In der folgenden VML-Darstellung wird beispielsweise das rote Oval über dem blauen Rechteck angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e21cf-182">For example, in the following VML representation, the red oval is displayed on top of the blue rectangle.</span></span> <span data-ttu-id="e21cf-183">Dies liegt daran, dass der Z-Index-Wert des roten Ovals größer als der Z-Index-Wert des blauen Rechtecks ist.</span><span class="sxs-lookup"><span data-stu-id="e21cf-183">This is because the z-index value of the red oval is greater than the z-index value of the blue rectangle.</span></span>

![shape4.gif (572 Bytes)](images/shape4.gif)


```HTML
<v:oval
style='position:relative;left:10pt;top:20pt;width:100pt; height:80pt;z-index: 1'
fillcolor="red" />
<v:rect style='position:relative;left:10pt;top:45pt;width:100pt; height:80pt; z-index:0' fillcolor="blue" />
```





<span data-ttu-id="e21cf-185">Wenn Sie den Z-Index ändern, wie in der folgenden VML-Darstellung gezeigt, würde sich das rote Oval hinter dem blauen Rechteck bewegen.</span><span class="sxs-lookup"><span data-stu-id="e21cf-185">If you change the z-index, as shown in the following VML representation, the red oval would move behind the blue rectangle.</span></span>

![shape5.gif (469 Bytes)](images/shape5.gif)


```HTML
<v:oval
style='position:relative;left:10pt;top:20pt;width:100pt; height:80pt;z-index:0'
fillcolor="red" />
<v:rect style='position:relative;left:10pt;top:45pt;width:100pt; height:80pt;z-index:1'
fillcolor="blue" />
```





<span data-ttu-id="e21cf-187">Wenn Sie eine negative ganze Zahl bereitstellen, können Sie z-index verwenden, um Grafiken hinter dem normalen Textfluss zu positionieren, wie in der folgenden VML-Darstellung gezeigt.</span><span class="sxs-lookup"><span data-stu-id="e21cf-187">If you supply a negative integer, you can use z-index to position graphics behind the normal text flow, as shown in the following VML representation.</span></span>

![shape6.gif (2125 Bytes)](images/shape6.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt;z-index:-1;
width:80pt;height:90pt;' fillcolor="red" />
End.
</body>
```





<span data-ttu-id="e21cf-189">[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="e21cf-189">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="rotation"></a><span data-ttu-id="e21cf-190">Drehung</span><span class="sxs-lookup"><span data-stu-id="e21cf-190">rotation</span></span>

<span data-ttu-id="e21cf-191">Sie können  das Rotationsformatattribut verwenden, um anzugeben, wie viele Grad eine Form auf der Achse drehen soll.</span><span class="sxs-lookup"><span data-stu-id="e21cf-191">You can use the **rotation** style attribute to specify how many degrees you want a shape to turn on its axis.</span></span> <span data-ttu-id="e21cf-192">Ein positiver Wert gibt eine Drehung im Uhrzeigersinn an. Ein negativer Wert gibt eine Drehung gegen den Uhrzeigersinn an.</span><span class="sxs-lookup"><span data-stu-id="e21cf-192">A positive value indicates a clockwise rotation; a negative value indicates a counter-clockwise rotation.</span></span>

<span data-ttu-id="e21cf-193">Wenn Sie z. B. **style**='... angeben rotation:90' können Sie die Form um 90 Grad im Uhrzeigersinn drehen.</span><span class="sxs-lookup"><span data-stu-id="e21cf-193">For example, if you specify **style**='... rotation:90', you can rotate the shape 90 degrees clockwise.</span></span>

<span data-ttu-id="e21cf-194">[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="e21cf-194">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="flip"></a><span data-ttu-id="e21cf-195">flip</span><span class="sxs-lookup"><span data-stu-id="e21cf-195">flip</span></span>

<span data-ttu-id="e21cf-196">Sie können das **Flip-Stilattribut** verwenden, um eine Form auf der x- oder y-Achse gemäß der folgenden Tabelle zu kippen:</span><span class="sxs-lookup"><span data-stu-id="e21cf-196">You can use the **flip** style attribute to flip a shape on its x or y axis according to the following table:</span></span>



| <span data-ttu-id="e21cf-197">Wert</span><span class="sxs-lookup"><span data-stu-id="e21cf-197">Value</span></span> | <span data-ttu-id="e21cf-198">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e21cf-198">Description</span></span>                                                  |
|-------|--------------------------------------------------------------|
| <span data-ttu-id="e21cf-199">x</span><span class="sxs-lookup"><span data-stu-id="e21cf-199">x</span></span>     | <span data-ttu-id="e21cf-200">Drehen der gedrehten Form um die y-Achse (X-Ordinate umkehren)</span><span class="sxs-lookup"><span data-stu-id="e21cf-200">Flip the rotated shape about the y axis (invert x ordinates)</span></span> |
| <span data-ttu-id="e21cf-201">j</span><span class="sxs-lookup"><span data-stu-id="e21cf-201">y</span></span>     | <span data-ttu-id="e21cf-202">Drehen Sie die gedrehte Form um die x-Achse (invertierte y-Koordinaten).</span><span class="sxs-lookup"><span data-stu-id="e21cf-202">Flip the rotated shape about the x axis (invert y ordinates)</span></span> |



 

<span data-ttu-id="e21cf-203">Sowohl x als auch y können in der Flip-Eigenschaft angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e21cf-203">Both x and y may be specified in the flip property.</span></span>

<span data-ttu-id="e21cf-204">Wenn Sie z. B. **style**='... eingeben, flip:x y' wird die Form sowohl auf der x- als auch auf der y-Achse gekippt.</span><span class="sxs-lookup"><span data-stu-id="e21cf-204">For example, if you type **style**='... flip:x y', you will flip the shape on both its x and y axis.</span></span>

<span data-ttu-id="e21cf-205">[![Zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="e21cf-205">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="e21cf-206">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="e21cf-206">Summary</span></span>

<span data-ttu-id="e21cf-207">Je nachdem, was Sie gelernt haben, können Sie eine Form auf einer Webseite genau positionieren, indem Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="e21cf-207">Based on what you've learned, you can precisely position a shape on a Web page by following these steps:</span></span>

1.  <span data-ttu-id="e21cf-208">Entscheiden Sie, wo die Form auf einer Webseite angezeigt werden soll, und legen Sie die Größe der Form fest.</span><span class="sxs-lookup"><span data-stu-id="e21cf-208">Decide where you want the shape to appear on a Web page, and the size of the shape.</span></span>
2.  <span data-ttu-id="e21cf-209">Geben Sie **style**='position:relative (or relative)' an, um den Basispunkt zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="e21cf-209">Specify **style**='position:relative (or relative)' to determine the base point.</span></span>
3.  <span data-ttu-id="e21cf-210">Verwenden Sie **links** und **oben,** um den Offset vom Basispunkt anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e21cf-210">Use **left** and **top** to specify the offset from the base point.</span></span>
4.  <span data-ttu-id="e21cf-211">Verwenden Sie **Breite** und **Höhe,** um die Größe des enthaltenden Felds für die Form anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e21cf-211">Use **width** and **height** to specify the size of the containing box for the shape.</span></span>
5.  <span data-ttu-id="e21cf-212">Verwenden Sie **z-index,** um die Z-Reihenfolge der Form anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e21cf-212">Use **z-index** to specify the z-order of the shape.</span></span>

 

 