---
title: Verwenden des lokalen Koordinaten Raums
description: Verwenden des lokalen Koordinaten Raums
ms.assetid: 8b5bc176-878f-4391-ab03-3f1c0e7713c3
keywords:
- Webworkshop, lokaler Koordinaten Bereich
- Entwerfen von Webseiten, lokaler Koordinaten Bereich
- Vector Markup Language (VML), lokaler Koordinaten Bereich
- VML (Vector Markup Language), lokaler Koordinaten Bereich
- Vektorgrafiken, lokaler Koordinatenraum
- lokaler Koordinaten Bereich
- VML-Formen, lokaler Koordinaten Bereich
- Vector Markup Language (VML), Gruppieren von Formen
- VML (Vector Markup Language), Gruppieren von Formen
- Vektorgrafiken, Gruppierungs Formen
- VML-Formen, gruppieren
- Gruppieren von Formen
- Vector Markup Language (VML), Skalieren von Formen
- VML (Vector Markup Language), Skalieren von Formen
- Vektorgrafiken, Skalierungs Formen
- VML-Formen, Skalierung
- Skalieren von Formen
- Vector Markup Language (VML), Größen Anpassungs Formen
- VML (Vector Markup Language), Größen Anpassungs Formen
- Vektorgrafiken, Größen Anpassungs Formen
- VML-Formen, Größenanpassung
- Größen Anpassungs Formen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c82d77ce16ae60bfc1249125d25b1139aeb8f44e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729736"
---
# <a name="using-local-coordinate-space"></a><span data-ttu-id="12086-125">Verwenden des lokalen Koordinaten Raums</span><span class="sxs-lookup"><span data-stu-id="12086-125">Using Local Coordinate Space</span></span>

<span data-ttu-id="12086-126">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="12086-126">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="12086-127">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="12086-127">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="12086-128">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="12086-128">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="12086-129">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="12086-129">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="12086-130">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="12086-130">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="12086-131">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="12086-131">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="12086-132">Wie Sie gelernt haben, können Sie die Attribute " **Width** " und " **height** " angeben, um die Größe eines enthaltenden Felds zu definieren, in dem der Inhalt einer Form oder Gruppe gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="12086-132">As you've learned, you can specify the **width** and **height** style attributes to define the size of a containing box within which the contents of a shape or group will be rendered.</span></span> <span data-ttu-id="12086-133">In diesem Thema wird erläutert, was der lokale Koordinaten Bereich ist und wie er in VML zum Skalieren von Formen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="12086-133">In this topic, we will explain what Local Coordinate Space is, and how it is used in VML to scale shapes.</span></span>

<span data-ttu-id="12086-134">Wenn Sie aufgefordert werden, ein 1-Zoll-Rechteck mit zwei Zoll in einem Raster Papier zu zeichnen, müssen Sie zunächst herausfinden, wo Sie beginnen sollen (der Ausgangspunkt).</span><span class="sxs-lookup"><span data-stu-id="12086-134">If you were asked to draw a one-inch by two-inch rectangle on a piece of grid paper, the first thing you would figure out is where to start (the originating point).</span></span> <span data-ttu-id="12086-135">Anschließend würden Sie herausfinden, wie Sie den Zellen des Raster Papiers (der Koordinate) einen Zoll zuordnen.</span><span class="sxs-lookup"><span data-stu-id="12086-135">Then, you would figure out how to map one inch to the cells of the grid paper (the coordinate).</span></span>

<span data-ttu-id="12086-136">Ebenso müssen, wenn der Inhalt einer Form oder Gruppe in das enthaltende Feld auf einer Webseite gerendert wird, der Ursprungs Punkt und die Koordinate definiert werden.</span><span class="sxs-lookup"><span data-stu-id="12086-136">Similarly, when the contents of a shape or group are rendered inside its containing box on a Web page, the originating point and the coordinate must be defined.</span></span> <span data-ttu-id="12086-137">VML bietet lokalen Koordinaten Bereich, damit jede Form oder Gruppe ihren eigenen Ausgangspunkt und ihre eigenen Koordinaten definieren kann.</span><span class="sxs-lookup"><span data-stu-id="12086-137">VML provides Local Coordinate Space to allow each shape or group to define its own originating point and coordinate.</span></span> <span data-ttu-id="12086-138">Wenn Sie keinen Koordinaten Bereich angeben, wird der Standardwert verwendet.</span><span class="sxs-lookup"><span data-stu-id="12086-138">If you don't specify a coordinate space, the default one will be used.</span></span> <span data-ttu-id="12086-139">Standardmäßig beginnt der Ursprung in der linken oberen Ecke des enthaltenden Felds.</span><span class="sxs-lookup"><span data-stu-id="12086-139">By default, the origination starts at the top-left corner of the containing box.</span></span>

<span data-ttu-id="12086-140">Die VML-Darstellung für das unten gezeigte rote Oval gibt z. b. nicht die **coordsize** -Eigenschaft und die **coordorigin** -Eigenschafts Attribute an.</span><span class="sxs-lookup"><span data-stu-id="12086-140">For example, the VML representation for the red oval shown below doesn't specify the **coordsize** and **coordorigin** property attributes.</span></span> <span data-ttu-id="12086-141">Daher wird ein lokaler Standard Koordinaten Bereich verwendet.</span><span class="sxs-lookup"><span data-stu-id="12086-141">Therefore, a default local coordinate space is used.</span></span> <span data-ttu-id="12086-142">Die Größe des Oval beträgt 100 Punkte (Breite) um 75 Punkte (Höhe).</span><span class="sxs-lookup"><span data-stu-id="12086-142">The size of the oval is 100 points (width) by 75 points (height).</span></span> <span data-ttu-id="12086-143">Sie können die Größe des Oval ändern, indem Sie eine andere Breite oder Höhe angeben, wie Sie im Thema [Skalierungs Formen](web-workshop---how-to-use-vml-on-web-pages----scaling-shapes.md) gelernt haben.</span><span class="sxs-lookup"><span data-stu-id="12086-143">You can resize the oval by specifying a different width or height, as you've learned in the [Scale Shapes](web-workshop---how-to-use-vml-on-web-pages----scaling-shapes.md) topic.</span></span>

![oval1.gif (627 Bytes)](images/oval1.gif)


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red">
</v:oval>
```





<span data-ttu-id="12086-145">Wenn die Form komplizierter wird, oder wenn Sie mehrere Formen gruppieren und diese zentral hochskalieren möchten, sollten Sie die in VML bereitgestellte lokale Koordinatenraum Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="12086-145">When the shape becomes more complicated, or when you would like to group several shapes and scale them together, you should use the Local Coordinate Space feature provided in VML.</span></span>

<span data-ttu-id="12086-146">Für jede Form oder Gruppe können Sie die Eigenschafts Attribute **coordsize** und **coordorigin** verwenden, um den lokalen Koordinaten Bereich der Form oder Gruppe zu definieren.</span><span class="sxs-lookup"><span data-stu-id="12086-146">For each shape or group, you can use the **coordsize** and **coordorigin** property attributes to define the shape's or group's local coordinate space.</span></span> <span data-ttu-id="12086-147">Das **coordsize** -Attribut gibt die Anzahl der Einheiten entlang der Breite und die Höhe des enthaltenden Felds an.</span><span class="sxs-lookup"><span data-stu-id="12086-147">The **coordsize** attribute specifies the number of units along the width and the height of the containing box.</span></span> <span data-ttu-id="12086-148">Das **coordorigin** -Attribut definiert die Koordinate in der oberen linken Ecke des enthaltenden Felds.</span><span class="sxs-lookup"><span data-stu-id="12086-148">The **coordorigin** attribute defines the coordinate at the top left corner of the containing box.</span></span> <span data-ttu-id="12086-149">Alle Positions bezogenen Informationen (z. b. "width", "Height", "Left", "Top", "Path" usw.) werden im Hinblick auf die Einheit im lokalen Koordinatenraum ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="12086-149">All position-related information (such as width, height, left, top, path, etc.) is expressed in terms of the unit in Local Coordinate Space.</span></span>

<span data-ttu-id="12086-150">So definiert z. b. wie in der folgenden VML-Darstellung gezeigt `width: 100pt; height: 100pt;` die Größe des enthaltenden Felds, sodass die Form 100 Punkte um 100 Punkte ist.</span><span class="sxs-lookup"><span data-stu-id="12086-150">For example, as shown in the following VML representation, `width: 100pt; height: 100pt;` defines the size of the containing box for the shape to be 100 points by 100 points.</span></span>

![cord1.gif (836 bytes)](images/cord1.gif)


```HTML
<v:shape style='position:relative;left:10pt;top:5pt; width:100pt; height:100pt;'
coordsize="21600,21600" path="m10800,0l0,10800,10800,21600,21600,10800xe"
fillcolor="red" strokecolor="blue" strokeweight="2pt">
</v:shape>
```





-   <span data-ttu-id="12086-152">`coordsize="21600,21600"` definiert die Größe des lokalen Koordinaten Raums für die Form von 21600 Einheiten um 21600 Einheiten.</span><span class="sxs-lookup"><span data-stu-id="12086-152">`coordsize="21600,21600"` defines the size of the Local Coordinate Space for the shape to be 21600 units by 21600 units.</span></span> <span data-ttu-id="12086-153">Aus diesem Grund ist eine Einheit im lokalen Koordinaten Bereich gleich dem 1/216-Punkt.</span><span class="sxs-lookup"><span data-stu-id="12086-153">Therefore, one unit in the Local Coordinate Space is equivalent to 1/216 point.</span></span>
-   <span data-ttu-id="12086-154">`path="m10800,0l0,10800,10800,21600,21600,10800xe"` definiert den Umriss der Form als Rautenform.</span><span class="sxs-lookup"><span data-stu-id="12086-154">`path="m10800,0l0,10800,10800,21600,21600,10800xe"` defines the outline of the shape as a diamond shape.</span></span> <span data-ttu-id="12086-155">Wir haben gelernt, dass alle Positions bezogenen Informationen (z. b. "width", "Height", "Left", "Top", "Path" usw.) im Hinblick auf die Einheit im lokalen Koordinatenraum ausgedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="12086-155">As we've learned, all position-related information (such as width, height, left, top, path, etc.) is expressed in terms of the unit in Local Coordinate Space.</span></span> <span data-ttu-id="12086-156">Daher bedeutet 10800 in der `<path>` 10800-Einheiten, was 50 Punkten entspricht.</span><span class="sxs-lookup"><span data-stu-id="12086-156">Therefore, 10800 in the `<path>` means 10800 units, which is equivalent to 50 points.</span></span>

<span data-ttu-id="12086-157">Wenn Sie die Größe dieser Rautenform ändern möchten, geben Sie einfach eine andere Breite oder Höhe an. Sie müssen keinen Wert in der ändern `<path>` .</span><span class="sxs-lookup"><span data-stu-id="12086-157">When you want to resize this diamond shape, simply specify a different width or height -- that's it; you don't have to change any value in the `<path>`.</span></span> <span data-ttu-id="12086-158">Wenn Sie die Funktion für den lokalen Koordinatenraum nicht verwendet haben, müssen Sie für diese komplizierte Form jeden Wert in der ändern, wenn Sie die Größe ändern möchten `<path>` .</span><span class="sxs-lookup"><span data-stu-id="12086-158">For this complicated shape, if you didn't use the Local Coordinate Space feature, you would have to change every value in the `<path>` whenever you wanted to resize it.</span></span>

<span data-ttu-id="12086-159">Beispielsweise können Sie die Rautenform skalieren, indem Sie einfach eine andere Breite oder Höhe angeben, wie in der folgenden VML-Darstellung dargestellt:</span><span class="sxs-lookup"><span data-stu-id="12086-159">For example, you can scale the diamond shape by simply specifying a different width or height, as shown in the following VML representation:</span></span>

![cord2.gif (1692 Bytes)](images/cord2.gif)


```HTML
<v:shape style='position:relative;left:10pt;top:5pt;width:200pt; height:200pt;'
coordsize="21600,21600" path="m10800,0l0,10800,10800,21600,21600,10800xe"
fillcolor="red" strokecolor="blue" strokeweight="2pt">
</v:shape>
```





<span data-ttu-id="12086-161">Sie können auch den lokalen Koordinaten Bereich im- `<group>` Element verwenden, damit der Inhalt aller Formen innerhalb der Gruppe entsprechend der gleichen Koordinate zentral hochskaliert wird.</span><span class="sxs-lookup"><span data-stu-id="12086-161">You can also use Local Coordinate Space in the `<group>` element so that the contents of all shapes within the group are scaled together according to the same coordinate.</span></span> <span data-ttu-id="12086-162">Wenn Sie dann eine Gruppe von Formen skalieren oder verschieben möchten, ändern Sie einfach die Einstellungen für Breite und Höhe bzw. **coordsize** und **coordorigin** der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="12086-162">Then, whenever you want to scale or move a group of shapes, simply change the width and height, or **coordsize** and **coordorigin** settings, of the group.</span></span>

<span data-ttu-id="12086-163">In der folgenden VML-Darstellung wird z `<v:group style='... width:200pt;height:200pt;'>` . b. die Größe des enthaltenden Felds für die Gruppe mit 200 Punkten um 200 Punkte definiert.</span><span class="sxs-lookup"><span data-stu-id="12086-163">For example, in the following VML representation, `<v:group style='... width:200pt;height:200pt;'>` defines the size of the containing box for the group to be 200 points by 200 points.</span></span>

![cord3.gif (645 bytes)](images/cord3.gif)


```HTML
<v:group style='position:relative;left:1pt;top:2pt;width:200pt; height:200pt;'
coordsize="1000,1000" coordorigin="-500,-500">
<v:oval style='position:relative;left:0;top:0;width:400;height:300;' fillcolor="red" />
<v:roundrect style='position:relative;left:0;top:0;width:250;height:200;' fillcolor="green" />
</v:group>
```





-   <span data-ttu-id="12086-165">`coordsize="1000,1000"` definiert die Größe des lokalen Koordinaten Raums für die Gruppe, um 1000 Einheiten um 1000 Einheiten zu sein.</span><span class="sxs-lookup"><span data-stu-id="12086-165">`coordsize="1000,1000"` defines the size of the Local Coordinate Space for the group to be 1000 units by 1000 units.</span></span> <span data-ttu-id="12086-166">Daher entspricht eine Einheit im lokalen Koordinaten Bereich dem 1/5-Punkt.</span><span class="sxs-lookup"><span data-stu-id="12086-166">Therefore, 1 unit in the Local Coordinate Space is equivalent to 1/5 point.</span></span>
-   <span data-ttu-id="12086-167">`coordorigin="-500,-500"` definiert die linke obere Ecke des enthaltenden Felds als "-500,-500".</span><span class="sxs-lookup"><span data-stu-id="12086-167">`coordorigin="-500,-500"` defines the top left corner of the containing box to be "-500, -500".</span></span> <span data-ttu-id="12086-168">Daher reicht das Koordinatensystem in der enthaltenden Box zwischen-500 und 500 entlang der x-Achse und-500 bis 500 entlang der y-Achse.</span><span class="sxs-lookup"><span data-stu-id="12086-168">Therefore, the coordinate system inside the containing box ranges from -500 to 500 along the x-axis, and -500 to 500 along the y-axis.</span></span> <span data-ttu-id="12086-169">Anders ausgedrückt: die Mitte des enthaltenden Felds ist "0,0".</span><span class="sxs-lookup"><span data-stu-id="12086-169">In other words, the center of the containing box is "0, 0".</span></span>
-   <span data-ttu-id="12086-170">`<v:oval style='... width:400;height:300;'>` definiert die Größe des enthaltenden Felds für das rote Oval um 400 Einheiten (Breite) um 300 Einheiten (Höhe).</span><span class="sxs-lookup"><span data-stu-id="12086-170">`<v:oval style='... width:400;height:300;'>` defines the size of the containing box for the red oval to be 400 units (width) by 300 units (height).</span></span> <span data-ttu-id="12086-171">Da eine Einheit im lokalen Koordinaten Bereich 1/5 Punkt entspricht, ist die Größe des enthaltenden Felds für das rote Oval 80 Punkte (Breite) um 60 Punkte (Höhe).</span><span class="sxs-lookup"><span data-stu-id="12086-171">Because one unit in the Local Coordinate Space is equivalent to 1/5 point, the size of the containing box for the red oval is 80 points (width) by 60 points (height).</span></span>

<span data-ttu-id="12086-172">Ebenso ist die Größe des enthaltenden Felds für das grüne roundRect 50 Punkte (Breite) um 40 Punkte (Höhe).</span><span class="sxs-lookup"><span data-stu-id="12086-172">Similarly, the size of the containing box for the green roundrect is 50 points (width) by 40 points (height).</span></span>

<span data-ttu-id="12086-173">Wenn Sie die Größe des roten oval und des grünen roundrects ändern möchten, ändern Sie einfach `<v:group style='... width:200pt;height:200pt;'>` .</span><span class="sxs-lookup"><span data-stu-id="12086-173">When you want to to resize both the red oval and the green roundrect, simply change `<v:group style='... width:200pt;height:200pt;'>`.</span></span> <span data-ttu-id="12086-174">Das ist das, und Sie müssen die Größe der beiden Formen nicht einzeln ändern.</span><span class="sxs-lookup"><span data-stu-id="12086-174">That's it -- you don't have to individually change the size of the two shapes.</span></span>

<span data-ttu-id="12086-175">Wenn Sie z. b. `<v:group style='... width:200pt;height:200pt;'>` in ändern `<v:group style='... width:300pt;height:300pt;'>` , werden die Formen größer, wie in der folgenden Abbildung dargestellt:</span><span class="sxs-lookup"><span data-stu-id="12086-175">For example, if you change `<v:group style='... width:200pt;height:200pt;'>` to `<v:group style='... width:300pt;height:300pt;'>`, the shapes become larger, as shown in the following picture:</span></span>

![cord4.gif (943 bytes)](images/cord4.gif)



<span data-ttu-id="12086-177">Sie werden auch bemerken, dass sich die Formen anders befinden.</span><span class="sxs-lookup"><span data-stu-id="12086-177">You'd also notice that the shapes are located differently.</span></span> <span data-ttu-id="12086-178">Dies liegt daran, dass die Formen von "0,0" gezeichnet werden, das sich in der Mitte des enthaltenden Felds befindet.</span><span class="sxs-lookup"><span data-stu-id="12086-178">This is because the shapes are drawn from "0, 0" which is located at the center of the containing box.</span></span> <span data-ttu-id="12086-179">Da Sie das enthaltende Feld vergrößern, wird der Mittelpunkt des enthaltenden Felds ebenfalls verschoben.</span><span class="sxs-lookup"><span data-stu-id="12086-179">Because you make the containing box bigger, the center of the containing box is also moved.</span></span>

<span data-ttu-id="12086-180">Wenn Sie `coordorigin="-500,-500"` zu wechseln `coordorigin="0,0"` , wie in der folgenden Abbildung gezeigt, werden Sie feststellen, dass das rote oval und das grüne roundRect jeweils an die neue Position verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="12086-180">If you change `coordorigin="-500,-500"` to `coordorigin="0,0"`, as shown in the following picture, you'll notice that the red oval and the green roundrect are both shifted up to the new location.</span></span> <span data-ttu-id="12086-181">Der Grund hierfür ist, dass "0, 0" nun in der oberen linken Ecke des enthaltenden Felds angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="12086-181">This is because "0, 0" now locates at the top left corner of the containing box.</span></span>

![cord5.gif (648 Bytes)](images/cord5.gif)



<span data-ttu-id="12086-183">Es ist auch wichtig zu beachten, dass das enthaltende Feld keinen Clippingbereich festlegt.</span><span class="sxs-lookup"><span data-stu-id="12086-183">It is also important to note that the containing box does not establish a clipping region.</span></span> <span data-ttu-id="12086-184">Grafiken können außerhalb der Grenzen des enthaltenden Felds gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="12086-184">Graphics may be drawn outside the boundaries of the containing box.</span></span> <span data-ttu-id="12086-185">Das enthaltende Feld dient lediglich zum Zuordnen des lokalen Koordinaten Raums zum Seiten Raum.</span><span class="sxs-lookup"><span data-stu-id="12086-185">The containing box merely serves to map the local coordinate space to the page space.</span></span>

<span data-ttu-id="12086-186">Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation](https://www.w3.org/TR/NOTE-VML#-toc416858382) .</span><span class="sxs-lookup"><span data-stu-id="12086-186">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858382) .</span></span>

 

 