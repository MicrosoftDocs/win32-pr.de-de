---
title: Verwenden des Fill-Elements
description: In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.
ms.assetid: ed36601d-2e90-412e-ac3f-58324fac300d
keywords:
- Webworkshop, Fill-Element
- Entwerfen von Webseiten, Fill-Element
- Vector Markup Language (VML), Fill-Element
- VML (Vector Markup Language), Fill-Element
- Vektorgrafiken, Fill-Element
- Fill-Element
- VML-Elemente, ausfüllen
- VML-Formen, Fill-Element
- Vector Markup Language (VML), Farbverlaufsfüllung
- VML (Vector Markup Language), Farbverlaufsfüllung
- Vektorgrafiken, Farbverlaufsfüllung
- VML-Formen, Farbverlaufsfüllung
- durch Farbverlauf gefüllte Formen
- Vector Markup Language (VML), Musterfüllung
- VML (Vector Markup Language), Musterfüllung
- Vektorgrafiken, Musterfüllung
- VML-Formen, Musterfüllung
- Muster gefüllte Formen
- Vector Markup Language (VML), Bild Füllung
- VML (Vector Markup Language), Bild Füllung
- Vektorgrafiken, bildfüll
- VML-Formen, Bild Füllung
- Bild gefüllte Formen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf497a3120f53e24f1cff2bf7084469754bbaf7e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104555357"
---
# <a name="using-the-fill-element"></a><span data-ttu-id="17f2c-127">Verwenden des Fill-Elements</span><span class="sxs-lookup"><span data-stu-id="17f2c-127">Using the Fill Element</span></span>

<span data-ttu-id="17f2c-128">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="17f2c-128">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="17f2c-129">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="17f2c-129">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="17f2c-130">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="17f2c-130">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="17f2c-131">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="17f2c-131">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="17f2c-132">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="17f2c-132">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="17f2c-133">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="17f2c-133">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="17f2c-134">Wie Sie gelernt haben, können Sie das **FillColor** -Eigenschafts Attribut eines vordefinierten Shape-Elements verwenden, z. b.,,,, `<oval>` `<line>` `<polyline>` `<curve>` `<rect>` , `<roundrect>` , `<arc>` --, um die Farbe anzugeben, die zum Ausfüllen der Form verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="17f2c-134">As you've learned, you can use the **fillcolor** property attribute of a predefined shape element -- such as `<oval>` , `<line>`, `<polyline>`, `<curve>`, `<rect>`, `<roundrect>`, `<arc>` -- to specify the color that is used to fill the shape.</span></span> <span data-ttu-id="17f2c-135">In diesem Thema wird veranschaulicht, wie eine Form gezeichnet wird, die mit erweiterten Effekten gefüllt ist.</span><span class="sxs-lookup"><span data-stu-id="17f2c-135">In this topic, we will illustrate how to draw a shape that is filled with more advanced effects.</span></span>

<span data-ttu-id="17f2c-136">Sie können das `<fill>` untergeordnete Element innerhalb des- `<shape>` ,-oder-Elements `<shapetype>` oder eines beliebigen vordefinierten Shape-Elements platzieren, um das Ausfüllen der Form zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="17f2c-136">You can place the `<fill>` sub-element inside the `<shape>`, or `<shapetype>`, or any predefined shape element to describe how to fill the shape.</span></span> <span data-ttu-id="17f2c-137">Anschließend können Sie die Eigenschafts Attribute des `<fill>` unter Elements verwenden, um den Fülleffekt anzupassen, z. b. [Farbverlaufsfüllung](#gradient-fill), [Musterfüllung](#pattern-fill), [Bild Füllung](#picture-fill).</span><span class="sxs-lookup"><span data-stu-id="17f2c-137">You can then use the property attributes of the `<fill>` sub-element to customize the fill effect, such as [gradient fill](#gradient-fill), [pattern fill](#pattern-fill), [picture fill](#picture-fill).</span></span>

<span data-ttu-id="17f2c-138">In diesem Thema:</span><span class="sxs-lookup"><span data-stu-id="17f2c-138">In this topic:</span></span>

-   [<span data-ttu-id="17f2c-139">Farbverlaufsfüllung</span><span class="sxs-lookup"><span data-stu-id="17f2c-139">Gradient Fill</span></span>](#gradient-fill)
-   [<span data-ttu-id="17f2c-140">Musterfüllung</span><span class="sxs-lookup"><span data-stu-id="17f2c-140">Pattern Fill</span></span>](#pattern-fill)
-   [<span data-ttu-id="17f2c-141">Bild Füllung</span><span class="sxs-lookup"><span data-stu-id="17f2c-141">Picture Fill</span></span>](#picture-fill)

## <a name="gradient-fill"></a><span data-ttu-id="17f2c-142">Farbverlaufsfüllung</span><span class="sxs-lookup"><span data-stu-id="17f2c-142">Gradient Fill</span></span>

<span data-ttu-id="17f2c-143">Um eine Form vom **Typ** "Gradient" zu zeichnen, können Sie das Type-Eigenschafts Attribut des `<fill>` unter Elements auf "Gradient" oder "gradientradi" festlegen und dann andere Eigenschafts Attribute des `<fill>` unter Elements angeben, z. b. **Methode**, **color2**, **Fokus** und **Winkel**.</span><span class="sxs-lookup"><span data-stu-id="17f2c-143">To draw a gradient-filled shape, you can set the **type** property attribute of the `<fill>` sub-element to "gradient" or "gradientRadial", and then specify other property attributes of the `<fill>` sub-element, such as **method**, **color2**, **focus**, and **angle**.</span></span>

<span data-ttu-id="17f2c-144">**Beispiele:**</span><span class="sxs-lookup"><span data-stu-id="17f2c-144">**Examples:**</span></span>

<span data-ttu-id="17f2c-145">Zum Erstellen einer Form, die horizontal mit einem Farbverlauf gefüllt ist, können Sie das Attribut **Type** Property auf "Gradient" festlegen, wie in der folgenden VML-Darstellung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="17f2c-145">To create a shape that is gradient-filled horizontally, you can set the **type** property attribute to "gradient", as shown in the following VML representation:</span></span>

![horizontal1.gif (3055 Bytes)](images/horizontal1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill type="gradient" />
</v:rect>
```




<span data-ttu-id="17f2c-147">Wenn Sie das **FillColor** -Eigenschafts Attribut der Form ändern, wird die Form dann mit einer anderen Farbe aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="17f2c-147">If you change the **fillcolor** property attribute of the shape, the shape is then gradient-filled with a different color.</span></span> <span data-ttu-id="17f2c-148">Sie können eine zweite Farbe hinzufügen, indem Sie das **color2** -Eigenschafts Attribut des `<fill>` unter Elements angeben.</span><span class="sxs-lookup"><span data-stu-id="17f2c-148">You can add a second color by specifying the **color2** property attribute of the `<fill>` sub-element.</span></span> <span data-ttu-id="17f2c-149">Um z. b. eine Form zu erstellen, die in zwei Farben mit einem Farbverlauf gefüllt ist, können Sie eine zweite Farbe hinzufügen, indem Sie das **color2** -Eigenschafts Attribut des `<fill>` unter Elements angeben, wie in der folgenden VML-Darstellung dargestellt:</span><span class="sxs-lookup"><span data-stu-id="17f2c-149">For example, to create a shape that is gradient-filled in two colors, you can add a second color by specifying the **color2** property attribute of the `<fill>` sub-element, as shown in the following VML representation:</span></span>

![horizontal2.gif (3127 Bytes)](images/horizontal2.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill color2="blue" type="gradient" />
</v:rect>
```




<span data-ttu-id="17f2c-151">Sie können das **method** -Eigenschaften Attribut auf "Linear" oder "Sigma" oder "Any" oder "None" festlegen.</span><span class="sxs-lookup"><span data-stu-id="17f2c-151">You can set the **method** property attribute to "linear" or "sigma" or "any" or "none".</span></span> <span data-ttu-id="17f2c-152">Die Auswirkung des Farbverlaufs unterscheidet sich geringfügig.</span><span class="sxs-lookup"><span data-stu-id="17f2c-152">The effect of the gradient is slightly different.</span></span> <span data-ttu-id="17f2c-153">Außerdem können Sie mit dem **Angle**-,**Fokus**-,**focussize**-oder **focusposition** -Eigenschafts Attribut ändern, wie der Farbverlauf verläuft.</span><span class="sxs-lookup"><span data-stu-id="17f2c-153">Also, you can use the **angle**,**focus**,**focussize**, or **focusposition** property attribute to change how the gradient goes.</span></span>

<span data-ttu-id="17f2c-154">**Beispiele:**</span><span class="sxs-lookup"><span data-stu-id="17f2c-154">**Examples:**</span></span>

 

<span data-ttu-id="17f2c-155">Zum Erstellen einer Form, die mit einem vertikalen Farbverlauf aufgefüllt ist, können Sie das Angle-Eigenschafts Attribut auf Angle = "-90" festlegen, wie in der folgenden VML-Darstellung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="17f2c-155">To create a shape that is gradient-filled vertically, you can set the angle property attribute to angle="-90", as shown in the following VML representation:</span></span>

![vertical1.gif (3836 Bytes)](images/vertical1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-90"
type="gradient" />
</v:rect>
```




<span data-ttu-id="17f2c-157">Um eine Form zu erstellen, die von diagonalem bewegen mit einem Farbverlauf gefüllt ist, können Sie das **Angle** -Eigenschafts Attribut auf Angle = "-135" festlegen, wie in der folgenden VML-Darstellung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="17f2c-157">To create a shape that is gradient-filled from diagonal moving up, you can set the **angle** property attribute to angle="-135", as shown in the following VML representation:</span></span>

![dialgonalup1.gif (5816 Bytes)](images/dialgonalup1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-135"
type="gradient" />
</v:rect>
```




<span data-ttu-id="17f2c-159">Um eine Form zu erstellen, die von einem diagonalen, nach unten ausgefüllten Farbverlauf gefüllt ist, können Sie das **Angle** -Eigenschafts Attribut auf Angle = "-45" festlegen, wie in der folgenden VML-Darstellung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="17f2c-159">To create a shape that is gradient-filled from diagonal moving down, you can set the **angle** property attribute to angle="-45", as shown in the following VML representation:</span></span>

![diagonaldown1.gif (5753 Bytes)](images/diagonaldown1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-45"
type="gradient" />
</v:rect>
```




<span data-ttu-id="17f2c-161">Um eine Form zu erstellen, die aus dem Mittelpunkt aufgefüllt wird, können Sie angeben `angle="-45" focus="100%" focusposition=".5, .5" focussize="0, 0" type="gradientRadial"` , wie in der folgenden VML-Darstellung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="17f2c-161">To create a shape that is gradient-filled from the center, you can specify `angle="-45" focus="100%" focusposition=".5, .5" focussize="0, 0" type="gradientRadial"`, as shown in the following VML representation:</span></span>

![fromcenter1.gif (4598 Bytes)](images/fromcenter1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-45"
focus="100%" focusposition=".5,.5" focussize="0,0"
type="gradientRadial" />
</v:rect>
```




<span data-ttu-id="17f2c-163">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="17f2c-163">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="pattern-fill"></a><span data-ttu-id="17f2c-164">Musterfüllung</span><span class="sxs-lookup"><span data-stu-id="17f2c-164">Pattern Fill</span></span>

<span data-ttu-id="17f2c-165">Um eine Muster gefüllte Form zu zeichnen, können Sie das **Type** -Eigenschafts Attribut des `<fill>` unter Elements auf "Pattern" festlegen und anschließend andere Eigenschafts Attribute des `<fill>` unter Elements angeben, z. b. **src** und **color2**.</span><span class="sxs-lookup"><span data-stu-id="17f2c-165">To draw a pattern-filled shape, you can set the **type** property attribute of the `<fill>` sub-element to "pattern", and then specify other property attributes of the `<fill>` sub-element, such as **src** and **color2**.</span></span>

<span data-ttu-id="17f2c-166">**Beispiele:**</span><span class="sxs-lookup"><span data-stu-id="17f2c-166">**Examples:**</span></span>

<span data-ttu-id="17f2c-167">Zum Erstellen einer Form, die mit einem Musterbild gefüllt ist, können Sie das **Type** -Eigenschafts Attribut auf "Pattern" festlegen und das **src** -Eigenschafts Attribut auf den Speicherort der Pattern-Bilddatei verweisen, wie in der folgenden VML-Darstellung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="17f2c-167">To create a shape that is filled with a pattern image, you can specify the **type** property attribute to "pattern", and point the **src** property attribute to the location of the pattern image file, as shown in the following VML representation:</span></span>

![pattern1.gif (872 bytes)](images/pattern1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill type="pattern" src="image1.gif"/>
</v:rect>
```




<span data-ttu-id="17f2c-169">Wenn Sie das **src** -Eigenschafts Attribut auf eine andere Musterdatei verweisen, können Sie eine Form erstellen, die mit einem anderen Muster gefüllt ist.</span><span class="sxs-lookup"><span data-stu-id="17f2c-169">If you point the **src** property attribute to a different pattern file, you can create a shape that is filled with a different pattern.</span></span> <span data-ttu-id="17f2c-170">Außerdem können Sie die Farbe ändern, indem Sie einen anderen Wert für das **FillColor** -oder **color2** -Eigenschafts Attribut angeben, wie in der folgenden VML-Darstellung dargestellt:</span><span class="sxs-lookup"><span data-stu-id="17f2c-170">Also, you can change the color by specifying a different value for the **fillcolor** or **color2** property attribute, as shown in the following VML representation:</span></span>

![pattern2.gif (831 Bytes)](images/pattern2.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="white">
<v:fill type="pattern" src="image2.gif"
color2="blue" />
</v:rect>
```




<span data-ttu-id="17f2c-172">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="17f2c-172">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="picture-fill"></a><span data-ttu-id="17f2c-173">Bild Füllung</span><span class="sxs-lookup"><span data-stu-id="17f2c-173">Picture Fill</span></span>

<span data-ttu-id="17f2c-174">Zum Zeichnen eines Bilds können Sie das **Type** -Eigenschafts Attribut des `<fill>` unter Elements auf "Frame" festlegen und anschließend andere Eigenschafts Attribute des `<fill>` unter Elements angeben, z. b. **src** und **color2**.</span><span class="sxs-lookup"><span data-stu-id="17f2c-174">To draw a picture-filled shape, you can set the **type** property attribute of the `<fill>` sub-element to "frame", and then specify other property attributes of the `<fill>` sub-element, such as **src** and **color2**.</span></span>

<span data-ttu-id="17f2c-175">**Beispiele:**</span><span class="sxs-lookup"><span data-stu-id="17f2c-175">**Examples:**</span></span>

<span data-ttu-id="17f2c-176">Um eine Form zu erstellen, die mit einer Bilddatei gefüllt ist, können Sie das **Type** -Eigenschafts Attribut auf "Frame" festlegen und dann das **src** -Eigenschafts Attribut auf den Speicherort der Bilddatei verweisen, wie in der folgenden VML-Darstellung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="17f2c-176">To create a shape that is filled with a picture file, you can specify the **type** property attribute to "frame", and then point the **src** property attribute to the location of the picture file, as shown in the following VML representation:</span></span>

![picture1.gif (8496 Bytes)](images/picture1.gif)


```HTML
<v:oval style='width:120pt;height:90pt' strokecolor="red"
strokeweight="2.5pt">
<v:fill type="frame" src="image1.jpg" />
</v:oval>
```




<span data-ttu-id="17f2c-178">Sie können problemlos eine Form erstellen, die mit einem anderen Bild gefüllt ist, indem Sie das **src** -Eigenschafts Attribut auf eine andere Datei zeigen.</span><span class="sxs-lookup"><span data-stu-id="17f2c-178">You can easily create a shape that is filled with a different picture by pointing the **src** property attribute to another file.</span></span>

<span data-ttu-id="17f2c-179">Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation](https://www.w3.org/TR/NOTE-VML#-toc416858394) .</span><span class="sxs-lookup"><span data-stu-id="17f2c-179">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858394) .</span></span>

 

 