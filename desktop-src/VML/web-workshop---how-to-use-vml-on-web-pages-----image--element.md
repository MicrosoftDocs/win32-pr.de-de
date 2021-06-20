---
title: Verwenden des Image-Elements
description: In diesem Artikel wird die Verwendung des Image-Elements in VML beschrieben, einem Feature, das seit Windows Internet Explorer 9 veraltet ist.
ms.assetid: 444c0b21-35f0-4e2d-ab6d-87a88229d9d2
keywords:
- Web-Workshop,image-Element
- Entwerfen von Webseiten,image-Element
- Vector Markup Language (VML),image-Element
- VML (Vector Markup Language),image-Element
- Vektorgrafik,Bildelement
- Bildelement
- VML-Elemente,Image
- VML-Formen, Bildelement
- Vector Markup Language (VML), Zuschneiden von Eigenschaftenattributen
- VML (Vector Markup Language),Zuschneiden von Eigenschaftenattributen
- Vektorgrafiken,Eigenschaftenattribute zuschneiden
- VML-Formen,Eigenschaftenattribute zuschneiden
- Zuschneideeigenschaftenattribute
- Vector Markup Language (VML),gain-Eigenschaftenattribut
- VML (Vector Markup Language),gain-Eigenschaftenattribut
- Vektorgrafiken,Gain-Eigenschaftsattribut
- VML-Formen,Gain-Eigenschaftsattribut
- gain-Eigenschaftenattribut
- Vector Markup Language (VML), Kontrast
- VML (Vector Markup Language),Kontrast
- Vektorgrafiken,Kontrast
- VML-Formen,Kontrast
- Vector Markup Language (VML), blacklevel-Eigenschaftenattribut
- VML (Vector Markup Language),blacklevel-Eigenschaftenattribut
- Vektorgrafiken,Blacklevel-Eigenschaftsattribut
- VML-Formen, Blacklevel-Eigenschaftsattribut
- blacklevel-Eigenschaftenattribut
- Vector Markup Language (VML), Helligkeit
- VML (Vector Markup Language), Helligkeit
- Vektorgrafiken, Helligkeit
- VML-Formen, Helligkeit
- Vector Markup Language (VML), Grayscale-Eigenschaftsattribut
- VML (Vector Markup Language),grayscale-Eigenschaftenattribut
- Vektorgrafik,Grayscale-Eigenschaftsattribut
- VML-Formen,Grayscale-Eigenschaftsattribut
- grayscale-Eigenschaftenattribut
- Vector Markup Language (VML),gamma-Eigenschaftsattribut
- VML (Vector Markup Language),gamma-Eigenschaftenattribut
- Vektorgrafiken, Gammaeigenschaftsattribut
- VML-Formen, Gammaeigenschaftsattribut
- gamma-Eigenschaftsattribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 572acef76afc42e02f476ca1825ef2541f596380
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407803"
---
# <a name="using-the-image-element"></a><span data-ttu-id="02e86-144">Verwenden des Image-Elements</span><span class="sxs-lookup"><span data-stu-id="02e86-144">Using the Image Element</span></span>

<span data-ttu-id="02e86-145">In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="02e86-145">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="02e86-146">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="02e86-146">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="02e86-147">Seit Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="02e86-147">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="02e86-148">Daher wird sie nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="02e86-148">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="02e86-149">Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/)</span><span class="sxs-lookup"><span data-stu-id="02e86-149">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="02e86-150">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)</span><span class="sxs-lookup"><span data-stu-id="02e86-150">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="02e86-151">Verwenden von `<image>`</span><span class="sxs-lookup"><span data-stu-id="02e86-151">Using `<image>`</span></span>

<span data-ttu-id="02e86-152">In diesem Thema wird veranschaulicht, wie das -Element verwendet wird, um `<image>` Bilder mit verschiedenen Sondereffekten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="02e86-152">In this topic, we will illustrate how to use the `<image>` element to display pictures with various special effects.</span></span>

<span data-ttu-id="02e86-153">Wenn Sie ein Bild anzeigen möchten, das aus einer externen Quelle geladen wurde, verwenden Sie in der Regel das in HTML bereitgestellte Element und verweisen dann das src-Eigenschaftsattribut auf den Speicherort der `<img>` Bilddatei. </span><span class="sxs-lookup"><span data-stu-id="02e86-153">If you wanted to display a picture that was loaded from an external source, you would usually use the `<img>` element provided in HTML, and then point the **src** property attribute to the location of the image file.</span></span>

<span data-ttu-id="02e86-154">Alternativ können Sie das in `<image>` VML bereitgestellte Element verwenden.</span><span class="sxs-lookup"><span data-stu-id="02e86-154">Alternatively you can use the `<image>` element provided in VML.</span></span> <span data-ttu-id="02e86-155">Wenn Sie das -Element verwenden, können Sie nur eine Bilddatei erstellen und das Bild dann anders anzeigen, indem Sie die Eigenschaftenattribute `<image>` des Elements `<image>` ändern.</span><span class="sxs-lookup"><span data-stu-id="02e86-155">When you use the `<image>` element, you can create only one image file and then display the image differently by altering the property attributes of the `<image>` element.</span></span> <span data-ttu-id="02e86-156">Darüber hinaus bietet das -Element mehrere Sondereffekte, die Sie nicht einfach mithilfe des HTML-Elements verwenden können, z. B. zuschneiden, `<image>` kontrastieren, `<img>` [](#crop) [Helligkeit,](#brightness) [Gamma](#gamma)und [Graustufen.](#grayscale) [](#contrast)</span><span class="sxs-lookup"><span data-stu-id="02e86-156">Also, the `<image>` element provides several special effects that you can't do by simply using the `<img>` element of HTML, such as [cropping](#crop), [contrast](#contrast), [brightness](#brightness), [gamma](#gamma), and [grayscale](#grayscale).</span></span>

<span data-ttu-id="02e86-157">[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="02e86-157">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="crop"></a><span data-ttu-id="02e86-158">Ernte</span><span class="sxs-lookup"><span data-stu-id="02e86-158">crop</span></span>

<span data-ttu-id="02e86-159">Sie können die **Eigenschaftenattribute cropbottom**, **croptop**, **cropleft** und **cropright** des Elements verwenden, um verschiedene Bilder anzuzeigen, die aus derselben `<image>` Bilddatei zugeschnitten werden.</span><span class="sxs-lookup"><span data-stu-id="02e86-159">You can use the **cropbottom**, **croptop**, **cropleft**, and **cropright** property attributes of the `<image>` element to display different pictures that are cropped from the same image file.</span></span>

<span data-ttu-id="02e86-160">Der Wert dieser Zuschneideattribute stellt den Prozentualen Schnitt vom Rand des Bilds dar.</span><span class="sxs-lookup"><span data-stu-id="02e86-160">The value of these crop attributes represents the percentage cut from the edge of the picture.</span></span> <span data-ttu-id="02e86-161">Der Wert kann eine beliebige Zahl zwischen 0 und 1 sein.</span><span class="sxs-lookup"><span data-stu-id="02e86-161">The value can be any number between 0 to 1.</span></span> <span data-ttu-id="02e86-162">Standardmäßig ist der Wert auf 0 festgelegt, was angibt, dass keine Zuschneide vom Rand entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="02e86-162">By default, the value is set to 0, indicating no crop from the edge.</span></span> <span data-ttu-id="02e86-163">Der Wert 0,1 gibt einen Zuschnitt von 10 Prozent vom Rand an, der Wert 0,15 steht für einen Zuschnitt von 15 Prozent vom Rand und so weiter.</span><span class="sxs-lookup"><span data-stu-id="02e86-163">The value 0.1 indicates a cropping of 10 percent from the edge, The value 0.15 indicates a cropping of 15 percent from the edge, and so on.</span></span>

<span data-ttu-id="02e86-164">Um beispielsweise fünf Bilder anzuzeigen, die alle aus derselben Bilddatei zugeschnitten wurden, können Sie das -Element verwenden und verschiedene Zuschneidewerte angeben, wie in der folgenden `<image>` VML-Darstellung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="02e86-164">For example, to display five pictures that are all cropped from the same image file, you can use the `<image>` element and specify different crop values, as shown in the following VML representation:</span></span>

![image1.jpg (5770 Bytes)](images/image1.jpg)![image1 \-2.jpg (1969 Bytes)](images/image1-2.jpg)![image1 \-3.jpg (1148 Bytes)](images/image1-3.jpg)![image1 \-4.jpg (1686 Bytes)](images/image1-4.jpg)![image1 \-5.jpg (1364 Bytes)](images/image1-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:85pt;height:64pt' src="image1.jpg"
cropbottom="0.2" cropright="0.15"/>
<v:image style='width:50pt;height:44pt' src="image1.jpg"
cropbottom="0.45" cropleft="0.5"/>
<v:image style='width:80pt;height:56pt' src="image1.jpg"
croptop="0.3" cropright="0.2"/>
<v:image style='width:70pt;height:48pt' src="image1.jpg"
croptop="0.4" cropleft="0.3"/>
```





<span data-ttu-id="02e86-170">Das erste Bild , `<v:image style='width:100pt;height:80pt' src="image1.jpg" />` , hat keinen Zuschneidewert.</span><span class="sxs-lookup"><span data-stu-id="02e86-170">The first image, `<v:image style='width:100pt;height:80pt' src="image1.jpg" />`, doesn't have any crop value.</span></span> <span data-ttu-id="02e86-171">Daher werden 100 Prozent des originalen Bilds mit einer Größe von 100 Punkten um 80 Punkten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="02e86-171">Therefore, 100 percent of the original image is displayed at a size of 100 points by 80 points.</span></span>

<span data-ttu-id="02e86-172">Das zweite Bild, `<v:image style='width:85pt;height:64pt' src="image1.jpg" cropbottom="0.2" cropright="0.15"/>` , verfügt über einige Zuschneidewerte.</span><span class="sxs-lookup"><span data-stu-id="02e86-172">The second image, `<v:image style='width:85pt;height:64pt' src="image1.jpg" cropbottom="0.2" cropright="0.15"/>`, has some crop values.</span></span> <span data-ttu-id="02e86-173">`cropbottom="0.2"` gibt an, dass 20 Prozent des Bilds von unten zugeschnitten werden. `cropright="0.15"` gibt an, dass 15 Prozent des Bilds vom rechten Rand aus zugeschnitten werden.</span><span class="sxs-lookup"><span data-stu-id="02e86-173">`cropbottom="0.2"` indicates that 20 percent of the picture will be cropped from the bottom; `cropright="0.15"` indicates that 15 percent of the picture will be cropped from the right edge.</span></span> <span data-ttu-id="02e86-174">Das verbleibende Bild wird dann mit einer Größe von 85 Punkten um 64 Punkten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="02e86-174">The remaining picture is then displayed at a size of 85 points by 64 points.</span></span>

<span data-ttu-id="02e86-175">Auf ähnliche Weise haben das dritte, vierte und fünfte Bild einige Zuschneidewerte.</span><span class="sxs-lookup"><span data-stu-id="02e86-175">Similarly the third, fourth, and fifth images have some crop values.</span></span> <span data-ttu-id="02e86-176">Das ursprüngliche Bild wird gemäß den Zuschneidewerten zugeschnitten und dann entsprechend dem Wert von Breite und Höhe angezeigt.</span><span class="sxs-lookup"><span data-stu-id="02e86-176">The original picture is cropped according to the crop values, and is then displayed according to the value of width and height.</span></span>

<span data-ttu-id="02e86-177">[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="02e86-177">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="contrast"></a><span data-ttu-id="02e86-178">Kontrast</span><span class="sxs-lookup"><span data-stu-id="02e86-178">contrast</span></span>

<span data-ttu-id="02e86-179">Sie können  das Gain-Eigenschaftsattribut des -Elements verwenden, um `<image>` verschiedene Bilder mit unterschiedlichen Kontrasteinstellungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="02e86-179">You can use the **gain** property attribute of the `<image>` element to display various pictures that have different contrast settings.</span></span>

<span data-ttu-id="02e86-180">Der Wert  des gain-Eigenschaftsattributs kann eine beliebige Zahl sein.</span><span class="sxs-lookup"><span data-stu-id="02e86-180">The value of the **gain** property attribute can be any number.</span></span> <span data-ttu-id="02e86-181">Standardmäßig ist der Wert 1, was die Verwendung des gleichen Kontrasts wie das ursprüngliche Bild angibt.</span><span class="sxs-lookup"><span data-stu-id="02e86-181">By default, the value is 1, indicating the use of the same contrast as the original image.</span></span> <span data-ttu-id="02e86-182">Der Wert 0 gibt keinen Kontrast an.</span><span class="sxs-lookup"><span data-stu-id="02e86-182">The value 0 indicates no contrast.</span></span> <span data-ttu-id="02e86-183">Je größer die Zahl, desto höher der Kontrast.</span><span class="sxs-lookup"><span data-stu-id="02e86-183">The larger the number, the higher the contrast.</span></span>

<span data-ttu-id="02e86-184">Wenn Sie beispielsweise fünf Bilder mit unterschiedlichen Kontrasteinstellungen anzeigen möchten, können Sie das -Element verwenden und einen anderen Wert für das gain-Eigenschaftsattribut festlegen, wie in der folgenden `<image>` VML-Darstellung gezeigt: </span><span class="sxs-lookup"><span data-stu-id="02e86-184">For example, to display five pictures that have different contrast settings, you can use the `<image>` element and set a different value for the **gain** property attribute, as shown in the following VML representation:</span></span>

![image1.jpg (5770 Bytes)](images/image1.jpg)![image2 \-2.jpg (270 Bytes)](images/image2-2.jpg)![image2 \-3.jpg (1919 Bytes)](images/image2-3.jpg)![image2 \-4.jpg (3143 Bytes)](images/image2-4.jpg)![image2 \-5.jpg (1724 Bytes)](images/image2-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=0 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=0.5 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=3 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=-0.4 />
```





<span data-ttu-id="02e86-190">Wenn  das Gain-Eigenschaftsattribut auf 0 festgelegt ist, wird das gesamte Bild grau, da kein Kontrast besteht.</span><span class="sxs-lookup"><span data-stu-id="02e86-190">When the **gain** property attribute is set to 0, the entire image becomes gray because there is no contrast.</span></span> <span data-ttu-id="02e86-191">Der Kontrast ist deutlicher,  wenn das Gain-Eigenschaftsattribut auf 3 festgelegt ist, als wenn es auf 0,5 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="02e86-191">The contrast is more noticeable when the **gain** property attribute is set to 3 than when it is set to 0.5.</span></span> <span data-ttu-id="02e86-192">Der Kontrast wird umgekehrt, wenn das Gain-Eigenschaftsattribut auf einen negativen Wert wie -0,4 festgelegt ist. </span><span class="sxs-lookup"><span data-stu-id="02e86-192">The contrast is reversed when the **gain** property attribute is set to a negative value such as -0.4.</span></span>

<span data-ttu-id="02e86-193">[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="02e86-193">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="brightness"></a><span data-ttu-id="02e86-194">Helligkeit</span><span class="sxs-lookup"><span data-stu-id="02e86-194">brightness</span></span>

<span data-ttu-id="02e86-195">Sie können das **Blacklevel-Eigenschaftsattribut** des Elements verwenden, um verschiedene Bilder `<image>` mit unterschiedlichen Helligkeitseinstellungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="02e86-195">You can use the **blacklevel** property attribute of the `<image>` element to display various pictures that have different brightness settings.</span></span>

<span data-ttu-id="02e86-196">Der Wert des **blacklevel-Eigenschaftsattributs** kann ein beliebiger Wert zwischen 0 und 1 sein.</span><span class="sxs-lookup"><span data-stu-id="02e86-196">The value of the **blacklevel** property attribute can be any value between 0 to 1.</span></span> <span data-ttu-id="02e86-197">Standardmäßig ist der Wert 0, was angibt, dass die Helligkeitsstufe im ursprünglichen Bild beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="02e86-197">By default, the value is 0, indicating that the level of brightness in the original image is preserved.</span></span> <span data-ttu-id="02e86-198">Der Wert 1 gibt die höchste Helligkeitsstufe an.</span><span class="sxs-lookup"><span data-stu-id="02e86-198">The value 1 indicates the highest level of brightness.</span></span>

<span data-ttu-id="02e86-199">Um beispielsweise fünf Bilder mit unterschiedlichen Helligkeitseinstellungen anzuzeigen, können Sie das -Element verwenden und einen anderen Wert für das Blacklevel-Eigenschaftsattribut festlegen, wie in der folgenden `<image>` VML-Darstellung gezeigt: </span><span class="sxs-lookup"><span data-stu-id="02e86-199">For example, to display five pictures that have different brightness settings, you can use the `<image>` element and set a different value for the **blacklevel** property attribute, as shown in the following VML representation:</span></span>

![image1.jpg (5770 Bytes)](images/image1.jpg)![image3 \-2.jpg (2579 Bytes)](images/image3-2.jpg)![image3 \-3.jpg (2330 Bytes)](images/image3-3.jpg)![image3 \-4.jpg (2727 Bytes)](images/image3-4.jpg)![image3 \-5.jpg (2435 Bytes)](images/image3-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=0.1 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=0.2 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=-0.05 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=-0.15 />
```





<span data-ttu-id="02e86-205">[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="02e86-205">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="grayscale"></a><span data-ttu-id="02e86-206">Graustufe</span><span class="sxs-lookup"><span data-stu-id="02e86-206">grayscale</span></span>

<span data-ttu-id="02e86-207">Sie können das **Grayscale-Eigenschaftsattribut** des Elements verwenden, um Bilder mit oder `<image>` ohne Graustufen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="02e86-207">You can use the **grayscale** property attribute of the `<image>` element to display pictures with or without grayscale.</span></span>

<span data-ttu-id="02e86-208">Der Wert des **Grayscale-Eigenschaftsattributs** kann entweder true oder false sein.</span><span class="sxs-lookup"><span data-stu-id="02e86-208">The value of the **grayscale** property attribute can be either true or false.</span></span> <span data-ttu-id="02e86-209">Standardmäßig ist der Wert auf FALSE festgelegt, sodass das Bild in Farbe angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="02e86-209">By default, the value is set to false so that the image will be displayed in color.</span></span> <span data-ttu-id="02e86-210">Wenn der Wert auf TRUE festgelegt ist, wird das Bild in Graustufen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="02e86-210">If the value is set to true, the image will be displayed in grayscale.</span></span>

<span data-ttu-id="02e86-211">Wie in der folgenden Abbildung gezeigt, verwendet das erste Bild beispielsweise die Standardeinstellung (false) des Graustufenattributs ( `<v:image style='width:100pt;height:80pt' src="image1.jpg" />` ).</span><span class="sxs-lookup"><span data-stu-id="02e86-211">For example, as shown in the following picture, the first image uses the default setting (false)of the grayscale attribute (`<v:image style='width:100pt;height:80pt' src="image1.jpg" />` ).</span></span> <span data-ttu-id="02e86-212">Daher wird das Bild in Farbe angezeigt.</span><span class="sxs-lookup"><span data-stu-id="02e86-212">Therefore, the picture is displayed in color.</span></span>

<span data-ttu-id="02e86-213">Das zweite Bild legt das Graustufenattribut auf true fest ( `<v:image style='width:100pt;height:80pt' src="image1.jpg" grayscale=true />` ).</span><span class="sxs-lookup"><span data-stu-id="02e86-213">The second image sets the grayscale attribute to true (`<v:image style='width:100pt;height:80pt' src="image1.jpg" grayscale=true />` ).</span></span> <span data-ttu-id="02e86-214">Daher wird das Bild in Graustufen angezeigt, wie in der folgenden VML-Darstellung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="02e86-214">Therefore, the picture is displayed in grayscale, as shown in the following VML representation:</span></span>

![image1.jpg (5770 Bytes)](images/image1.jpg)![image4 \-2.jpg (2138 Bytes)](images/image4-2.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg"
grayscale=true />
```





<span data-ttu-id="02e86-217">[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="02e86-217">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="gamma"></a><span data-ttu-id="02e86-218">Gamma</span><span class="sxs-lookup"><span data-stu-id="02e86-218">gamma</span></span>

<span data-ttu-id="02e86-219">Sie können das **Gammaeigenschaftsattribut** des Elements verwenden, um Bilder mit `<image>` unterschiedlichen Gammaeinstellungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="02e86-219">You can use the **gamma** property attribute of the `<image>` element to display pictures that have different gamma settings.</span></span>

<span data-ttu-id="02e86-220">Der Wert des Gammaeigenschaftsattributs kann ein beliebiger Wert zwischen 0 und 1 sein.</span><span class="sxs-lookup"><span data-stu-id="02e86-220">The value of the gamma property attribute can be any value between 0 and 1.</span></span> <span data-ttu-id="02e86-221">Standardmäßig ist der Wert auf 1 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="02e86-221">By default, the value is set to 1.</span></span>

<span data-ttu-id="02e86-222">Um beispielsweise drei Bilder mit unterschiedlichen Gammaeinstellungen anzuzeigen, können Sie das -Element verwenden und einen anderen Wert des Gammaeigenschaftsattributs festlegen, wie in der folgenden `<image>` VML-Darstellung gezeigt: </span><span class="sxs-lookup"><span data-stu-id="02e86-222">For example, to display three pictures that have different gamma settings, you can use the `<image>` element and set a different value of the **gamma** property attribute, as shown in the following VML representation:</span></span>

![image5 \-1.jpg (2714 Bytes)](images/image5-1.jpg)![image5 \-2.jpg (2729 Bytes)](images/image5-2.jpg)![image5 \-3.jpg (2726 Bytes)](images/image5-3.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gamma=0 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gamma=0.5 />
```





<span data-ttu-id="02e86-226">Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation](https://www.w3.org/TR/NOTE-VML#-toc416858408) .</span><span class="sxs-lookup"><span data-stu-id="02e86-226">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858408) .</span></span>

 

 