---
title: Verwenden des Fill-Elements
description: In diesem Artikel wird die Verwendung des Fill-Elements von VML beschrieben, einem Feature, das ab Windows Internet Explorer 9 veraltet ist.
ms.assetid: ed36601d-2e90-412e-ac3f-58324fac300d
keywords:
- Web workshop,fill-Element
- Entwerfen von Webseiten, Füllen des Elements
- Vector Markup Language (VML),Fill-Element
- VML (Vector Markup Language),Fill-Element
- Vektorgrafiken, Fill-Element
- fill-Element
- VML-Elemente, auffüllen
- VML-Formen, Fill-Element
- Vector Markup Language (VML), Farbverlaufsfüllung
- VML (Vector Markup Language),Farbverlaufsfüllung
- Vektorgrafik, Farbverlaufsfüllung
- VML-Formen, Farbverlaufsfüllung
- Mit Farbverlauf gefüllte Formen
- Vector Markup Language (VML), Musterfüllung
- VML (Vector Markup Language),Musterfüllung
- Vektorgrafiken, Musterfüllung
- VML-Formen, Musterfüllung
- Mit Mustern gefüllte Formen
- Vector Markup Language (VML),Bildfüllung
- VML (Vector Markup Language),Bildfüllung
- Vektorgrafiken, Bildfüllung
- VML-Formen, Bildfüllung
- Mit Bildern gefüllte Formen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecb243e4896443fd36a1b22c2ac3a0ab0bedfb2b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407793"
---
# <a name="using-the-fill-element"></a><span data-ttu-id="2c155-126">Verwenden des Fill-Elements</span><span class="sxs-lookup"><span data-stu-id="2c155-126">Using the Fill Element</span></span>

<span data-ttu-id="2c155-127">In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="2c155-127">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="2c155-128">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="2c155-128">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="2c155-129">Seit Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="2c155-129">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="2c155-130">Daher wird sie nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="2c155-130">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="2c155-131">Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/)</span><span class="sxs-lookup"><span data-stu-id="2c155-131">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="2c155-132">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)</span><span class="sxs-lookup"><span data-stu-id="2c155-132">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="2c155-133">Wie Sie gelernt haben, können  Sie das fillcolor-Eigenschaftsattribut eines vordefinierten Formelements wie `<oval>` , , , , , , `<line>` `<polyline>` `<curve>` `<rect>` `<roundrect>` `<arc>` verwenden, um die Farbe anzugeben, die zum Füllen der Form verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2c155-133">As you've learned, you can use the **fillcolor** property attribute of a predefined shape element -- such as `<oval>` , `<line>`, `<polyline>`, `<curve>`, `<rect>`, `<roundrect>`, `<arc>` -- to specify the color that is used to fill the shape.</span></span> <span data-ttu-id="2c155-134">In diesem Thema wird veranschaulicht, wie eine Form gezeichnet wird, die mit erweiterten Effekten gefüllt ist.</span><span class="sxs-lookup"><span data-stu-id="2c155-134">In this topic, we will illustrate how to draw a shape that is filled with more advanced effects.</span></span>

<span data-ttu-id="2c155-135">Sie können das `<fill>` Unterelement innerhalb von `<shape>` oder oder in einem `<shapetype>` beliebigen vordefinierten Shape-Element platzieren, um zu beschreiben, wie die Form gefüllt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2c155-135">You can place the `<fill>` sub-element inside the `<shape>`, or `<shapetype>`, or any predefined shape element to describe how to fill the shape.</span></span> <span data-ttu-id="2c155-136">Anschließend können Sie die Eigenschaftenattribute des `<fill>` Unterelements verwenden, um den Fülleffekt anzupassen, z. B. [Farbverlaufsfüllung,](#gradient-fill) [Musterfüllung,](#pattern-fill) [Bildfüllung.](#picture-fill)</span><span class="sxs-lookup"><span data-stu-id="2c155-136">You can then use the property attributes of the `<fill>` sub-element to customize the fill effect, such as [gradient fill](#gradient-fill), [pattern fill](#pattern-fill), [picture fill](#picture-fill).</span></span>

<span data-ttu-id="2c155-137">In diesem Thema:</span><span class="sxs-lookup"><span data-stu-id="2c155-137">In this topic:</span></span>

-   [<span data-ttu-id="2c155-138">Farbverlaufsfüllung</span><span class="sxs-lookup"><span data-stu-id="2c155-138">Gradient Fill</span></span>](#gradient-fill)
-   [<span data-ttu-id="2c155-139">Musterfüllung</span><span class="sxs-lookup"><span data-stu-id="2c155-139">Pattern Fill</span></span>](#pattern-fill)
-   [<span data-ttu-id="2c155-140">Bildfüllung</span><span class="sxs-lookup"><span data-stu-id="2c155-140">Picture Fill</span></span>](#picture-fill)

## <a name="gradient-fill"></a><span data-ttu-id="2c155-141">Farbverlaufsfüllung</span><span class="sxs-lookup"><span data-stu-id="2c155-141">Gradient Fill</span></span>

<span data-ttu-id="2c155-142">Um eine mit Farbverlauf gefüllte  Form zu zeichnen, können Sie das Type-Eigenschaftsattribut des `<fill>` Unterelements auf "gradient" oder "gradientRadial" festlegen und dann andere Eigenschaftsattribute des `<fill>` Unterelements angeben, z. B. **methode**, **color2,** **focus** und **angle**.</span><span class="sxs-lookup"><span data-stu-id="2c155-142">To draw a gradient-filled shape, you can set the **type** property attribute of the `<fill>` sub-element to "gradient" or "gradientRadial", and then specify other property attributes of the `<fill>` sub-element, such as **method**, **color2**, **focus**, and **angle**.</span></span>

<span data-ttu-id="2c155-143">**Beispiele:**</span><span class="sxs-lookup"><span data-stu-id="2c155-143">**Examples:**</span></span>

<span data-ttu-id="2c155-144">Um eine Form zu erstellen, die horizontal mit  Farbverlauf gefüllt ist, können Sie das type-Eigenschaftsattribut auf "gradient" festlegen, wie in der folgenden VML-Darstellung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="2c155-144">To create a shape that is gradient-filled horizontally, you can set the **type** property attribute to "gradient", as shown in the following VML representation:</span></span>

![horizontal1.gif (3055 Bytes)](images/horizontal1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill type="gradient" />
</v:rect>
```




<span data-ttu-id="2c155-146">Wenn Sie  das Fillcolor-Eigenschaftsattribut der Form ändern, wird die Form mit einer anderen Farbe farbverlaufsgefüllt.</span><span class="sxs-lookup"><span data-stu-id="2c155-146">If you change the **fillcolor** property attribute of the shape, the shape is then gradient-filled with a different color.</span></span> <span data-ttu-id="2c155-147">Sie können eine zweite Farbe  hinzufügen, indem Sie das color2-Eigenschaftsattribut des `<fill>` Unterelements angeben.</span><span class="sxs-lookup"><span data-stu-id="2c155-147">You can add a second color by specifying the **color2** property attribute of the `<fill>` sub-element.</span></span> <span data-ttu-id="2c155-148">Wenn Sie z. B. eine Form erstellen möchten, die in zwei Farben  mit Farbverläufen gefüllt ist, können Sie eine zweite Farbe hinzufügen, indem Sie das color2-Eigenschaftsattribut des `<fill>` Unterelements angeben, wie in der folgenden VML-Darstellung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="2c155-148">For example, to create a shape that is gradient-filled in two colors, you can add a second color by specifying the **color2** property attribute of the `<fill>` sub-element, as shown in the following VML representation:</span></span>

![horizontal2.gif (3127 Bytes)](images/horizontal2.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill color2="blue" type="gradient" />
</v:rect>
```




<span data-ttu-id="2c155-150">Sie können  das Methodeneigenschaftsattribut auf "linear" oder "sigma" oder "any" oder "none" festlegen.</span><span class="sxs-lookup"><span data-stu-id="2c155-150">You can set the **method** property attribute to "linear" or "sigma" or "any" or "none".</span></span> <span data-ttu-id="2c155-151">Die Auswirkung des Farbverlaufs unterscheidet sich geringfügig.</span><span class="sxs-lookup"><span data-stu-id="2c155-151">The effect of the gradient is slightly different.</span></span> <span data-ttu-id="2c155-152">Darüber hinaus können Sie das Eigenschaftenattribut **angle**,**focus**,**focussize** oder **focusposition** verwenden, um zu ändern, wie der Farbverlauf verläuft.</span><span class="sxs-lookup"><span data-stu-id="2c155-152">Also, you can use the **angle**,**focus**,**focussize**, or **focusposition** property attribute to change how the gradient goes.</span></span>

<span data-ttu-id="2c155-153">**Beispiele:**</span><span class="sxs-lookup"><span data-stu-id="2c155-153">**Examples:**</span></span>

 

<span data-ttu-id="2c155-154">Um eine vertikal mit Farbverlauf gefüllte Form zu erstellen, können Sie das Angle-Eigenschaftsattribut auf angle="-90" festlegen, wie in der folgenden VML-Darstellung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="2c155-154">To create a shape that is gradient-filled vertically, you can set the angle property attribute to angle="-90", as shown in the following VML representation:</span></span>

![vertical1.gif (3836 Bytes)](images/vertical1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-90"
type="gradient" />
</v:rect>
```




<span data-ttu-id="2c155-156">Um eine Form zu erstellen, die vom Diagonalen  nach oben mit Farbverläufen gefüllt wird, können Sie das Angle-Eigenschaftsattribut auf angle="-135" festlegen, wie in der folgenden VML-Darstellung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="2c155-156">To create a shape that is gradient-filled from diagonal moving up, you can set the **angle** property attribute to angle="-135", as shown in the following VML representation:</span></span>

![dialgonalup1.gif (5816 Bytes)](images/dialgonalup1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-135"
type="gradient" />
</v:rect>
```




<span data-ttu-id="2c155-158">Um eine Form zu erstellen, die vom Diagonalen  nach unten mit Farbverläufen gefüllt wird, können Sie das Angle-Eigenschaftsattribut auf angle="-45" festlegen, wie in der folgenden VML-Darstellung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="2c155-158">To create a shape that is gradient-filled from diagonal moving down, you can set the **angle** property attribute to angle="-45", as shown in the following VML representation:</span></span>

![diagonaldown1.gif (5753 Bytes)](images/diagonaldown1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-45"
type="gradient" />
</v:rect>
```




<span data-ttu-id="2c155-160">Um eine Form zu erstellen, die von der Mitte aus mit Farbverläufen gefüllt ist, können Sie `angle="-45" focus="100%" focusposition=".5, .5" focussize="0, 0" type="gradientRadial"` angeben, wie in der folgenden VML-Darstellung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="2c155-160">To create a shape that is gradient-filled from the center, you can specify `angle="-45" focus="100%" focusposition=".5, .5" focussize="0, 0" type="gradientRadial"`, as shown in the following VML representation:</span></span>

![fromcenter1.gif (4598 Bytes)](images/fromcenter1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-45"
focus="100%" focusposition=".5,.5" focussize="0,0"
type="gradientRadial" />
</v:rect>
```




<span data-ttu-id="2c155-162">[![Zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="2c155-162">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="pattern-fill"></a><span data-ttu-id="2c155-163">Musterfüllung</span><span class="sxs-lookup"><span data-stu-id="2c155-163">Pattern Fill</span></span>

<span data-ttu-id="2c155-164">Um eine mit Mustern gefüllte  Form zu zeichnen, können Sie das type-Eigenschaftsattribut des `<fill>` Unterelements auf "pattern" festlegen und dann andere Eigenschaftsattribute des `<fill>` Unterelements angeben, z. B. **src** und **color2.**</span><span class="sxs-lookup"><span data-stu-id="2c155-164">To draw a pattern-filled shape, you can set the **type** property attribute of the `<fill>` sub-element to "pattern", and then specify other property attributes of the `<fill>` sub-element, such as **src** and **color2**.</span></span>

<span data-ttu-id="2c155-165">**Beispiele:**</span><span class="sxs-lookup"><span data-stu-id="2c155-165">**Examples:**</span></span>

<span data-ttu-id="2c155-166">Um eine Form zu erstellen, die mit einem  Musterbild gefüllt ist, können Sie das type-Eigenschaftsattribut auf "pattern" angeben und das src-Eigenschaftsattribut auf den Speicherort der Musterbilddatei verweisen, wie in der folgenden VML-Darstellung gezeigt: </span><span class="sxs-lookup"><span data-stu-id="2c155-166">To create a shape that is filled with a pattern image, you can specify the **type** property attribute to "pattern", and point the **src** property attribute to the location of the pattern image file, as shown in the following VML representation:</span></span>

![pattern1.gif (872 Bytes)](images/pattern1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill type="pattern" src="image1.gif"/>
</v:rect>
```




<span data-ttu-id="2c155-168">Wenn Sie  das src-Eigenschaftsattribut auf eine andere Musterdatei verweisen, können Sie eine Form erstellen, die mit einem anderen Muster gefüllt ist.</span><span class="sxs-lookup"><span data-stu-id="2c155-168">If you point the **src** property attribute to a different pattern file, you can create a shape that is filled with a different pattern.</span></span> <span data-ttu-id="2c155-169">Außerdem können Sie die Farbe ändern, indem Sie einen anderen Wert für das **fillcolor-** oder color2-Eigenschaftsattribut angeben, wie in der folgenden VML-Darstellung gezeigt: </span><span class="sxs-lookup"><span data-stu-id="2c155-169">Also, you can change the color by specifying a different value for the **fillcolor** or **color2** property attribute, as shown in the following VML representation:</span></span>

![pattern2.gif (831 Byte)](images/pattern2.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="white">
<v:fill type="pattern" src="image2.gif"
color2="blue" />
</v:rect>
```




<span data-ttu-id="2c155-171">[![Zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="2c155-171">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="picture-fill"></a><span data-ttu-id="2c155-172">Bildfüllung</span><span class="sxs-lookup"><span data-stu-id="2c155-172">Picture Fill</span></span>

<span data-ttu-id="2c155-173">Um eine mit Bildern gefüllte Form  zu zeichnen, können Sie das type-Eigenschaftsattribut des `<fill>` Unterelements auf "frame" festlegen und dann andere Eigenschaftsattribute des `<fill>` Unterelements angeben, z. B. **src** und **color2.**</span><span class="sxs-lookup"><span data-stu-id="2c155-173">To draw a picture-filled shape, you can set the **type** property attribute of the `<fill>` sub-element to "frame", and then specify other property attributes of the `<fill>` sub-element, such as **src** and **color2**.</span></span>

<span data-ttu-id="2c155-174">**Beispiele:**</span><span class="sxs-lookup"><span data-stu-id="2c155-174">**Examples:**</span></span>

<span data-ttu-id="2c155-175">Um eine Form zu erstellen, die mit einer  Bilddatei gefüllt ist, können Sie das type-Eigenschaftsattribut auf "frame" angeben und dann das src-Eigenschaftsattribut auf den Speicherort der Bilddatei verweisen, wie in der folgenden VML-Darstellung gezeigt: </span><span class="sxs-lookup"><span data-stu-id="2c155-175">To create a shape that is filled with a picture file, you can specify the **type** property attribute to "frame", and then point the **src** property attribute to the location of the picture file, as shown in the following VML representation:</span></span>

![picture1.gif (8496 Bytes)](images/picture1.gif)


```HTML
<v:oval style='width:120pt;height:90pt' strokecolor="red"
strokeweight="2.5pt">
<v:fill type="frame" src="image1.jpg" />
</v:oval>
```




<span data-ttu-id="2c155-177">Sie können ganz einfach eine Form erstellen, die  mit einem anderen Bild gefüllt ist, indem Sie das src-Eigenschaftsattribut auf eine andere Datei verweisen.</span><span class="sxs-lookup"><span data-stu-id="2c155-177">You can easily create a shape that is filled with a different picture by pointing the **src** property attribute to another file.</span></span>

<span data-ttu-id="2c155-178">Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation.](https://www.w3.org/TR/NOTE-VML#-toc416858394)</span><span class="sxs-lookup"><span data-stu-id="2c155-178">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858394) .</span></span>

 

 