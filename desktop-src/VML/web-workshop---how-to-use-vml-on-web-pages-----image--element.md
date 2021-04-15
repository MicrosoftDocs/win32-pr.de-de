---
title: Verwenden des Image-Elements
description: In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.
ms.assetid: 444c0b21-35f0-4e2d-ab6d-87a88229d9d2
keywords:
- Webworkshop, Image-Element
- Entwerfen von Webseiten, Image-Element
- Vector Markup Language (VML), Image-Element
- VML (Vector Markup Language), Image-Element
- Vektorgrafiken, Bildelement
- Bildelement
- VML-Elemente, Bild
- VML-Formen, Image-Element
- Vector Markup Language (VML), Attribute für Zuschneiden von Eigenschaften
- VML (Vector Markup Language), Attribute der zuschnittschaft
- Vektorgrafiken, Attribute für Zuschneiden von Eigenschaften
- VML-Formen, Attribute für Zuschneiden von Eigenschaften
- Attribute der zuschnitteigenschaften
- Vector Markup Language (VML), Eigenschafts Attribut erhalten
- VML (Vector Markup Language), Eigenschafts Attribut erhalten
- Vektorgrafiken, Eigenschafts Attribut gewinnen
- VML-Formen, Eigenschafts Attribut gewinnen
- Eigenschafts Attribut erhalten
- Vector Markup Language (VML), Kontrast
- VML (Vector Markup Language), Kontrast
- Vektorgrafiken, Kontrast
- VML-Formen, Kontrast
- Vector Markup Language (VML), Attribut der Blacklevel-Eigenschaft
- VML (Vector Markup Language), Attribut der Blacklevel-Eigenschaft
- Vektorgrafiken, Attribut der Blacklevel-Eigenschaft
- VML-Formen, Attribut der Blacklevel-Eigenschaft
- Attribut der Blacklevel-Eigenschaft
- Vector Markup Language (VML), Helligkeit
- VML (Vector Markup Language), Helligkeit
- Vektorgrafiken, Helligkeit
- VML-Formen, Helligkeit
- Vector Markup Language (VML), Graustufen Eigenschafts Attribut
- VML (Vector Markup Language), Graustufen Eigenschafts Attribut
- Vektorgrafiken, Graustufen Eigenschafts Attribut
- VML-Formen, Graustufen Eigenschafts Attribut
- Graustufen-Eigenschafts Attribut
- Vector Markup Language (VML), Gamma Property-Attribut
- VML (Vector Markup Language), Gamma Property-Attribut
- Vektorgrafiken, Gamma Property-Attribut
- VML-Formen, Gamma Property-Attribut
- Gamma Property-Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 820039ff76f3685eeea7a65e2bbc01578abbe581
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104517048"
---
# <a name="using-the-image-element"></a><span data-ttu-id="885fb-145">Verwenden des Image-Elements</span><span class="sxs-lookup"><span data-stu-id="885fb-145">Using the Image Element</span></span>

<span data-ttu-id="885fb-146">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="885fb-146">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="885fb-147">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="885fb-147">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="885fb-148">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="885fb-148">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="885fb-149">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="885fb-149">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="885fb-150">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="885fb-150">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="885fb-151">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="885fb-151">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="885fb-152">Verwenden von `<image>`</span><span class="sxs-lookup"><span data-stu-id="885fb-152">Using `<image>`</span></span>

<span data-ttu-id="885fb-153">In diesem Thema wird veranschaulicht, wie das-Element verwendet wird, `<image>` um Bilder mit verschiedenen speziellen Effekten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="885fb-153">In this topic, we will illustrate how to use the `<image>` element to display pictures with various special effects.</span></span>

<span data-ttu-id="885fb-154">Wenn Sie ein Bild anzeigen möchten, das aus einer externen Quelle geladen wurde, verwenden Sie in der Regel das `<img>` in HTML bereitgestellte-Element, und zeigen Sie dann das **src** -Eigenschafts Attribut auf den Speicherort der Bilddatei.</span><span class="sxs-lookup"><span data-stu-id="885fb-154">If you wanted to display a picture that was loaded from an external source, you would usually use the `<img>` element provided in HTML, and then point the **src** property attribute to the location of the image file.</span></span>

<span data-ttu-id="885fb-155">Alternativ können Sie das-Element verwenden, das `<image>` in VML bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="885fb-155">Alternatively you can use the `<image>` element provided in VML.</span></span> <span data-ttu-id="885fb-156">Wenn Sie das- `<image>` Element verwenden, können Sie nur eine Bilddatei erstellen und das Bild dann unterschiedlich anzeigen, indem Sie die Eigenschafts Attribute des- `<image>` Elements ändern.</span><span class="sxs-lookup"><span data-stu-id="885fb-156">When you use the `<image>` element, you can create only one image file and then display the image differently by altering the property attributes of the `<image>` element.</span></span> <span data-ttu-id="885fb-157">Außerdem bietet das- `<image>` Element einige besondere Effekte, die Sie nicht verwenden können, indem Sie einfach das- `<img>` Element von HTML verwenden, wie z. b. das [Ausschneiden](#crop), den [Kontrast](#contrast), die [Helligkeit](#brightness), [Gamma](#gamma)und [grau](#grayscale)Stufen.</span><span class="sxs-lookup"><span data-stu-id="885fb-157">Also, the `<image>` element provides several special effects that you can't do by simply using the `<img>` element of HTML, such as [cropping](#crop), [contrast](#contrast), [brightness](#brightness), [gamma](#gamma), and [grayscale](#grayscale).</span></span>

<span data-ttu-id="885fb-158">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="885fb-158">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="crop"></a><span data-ttu-id="885fb-159">an</span><span class="sxs-lookup"><span data-stu-id="885fb-159">crop</span></span>

<span data-ttu-id="885fb-160">Sie können die Eigenschaften Attribute **CropBottom**, **CropTop**, **CropLeft** und **CropRight** des-Elements verwenden `<image>` , um unterschiedliche Bilder anzuzeigen, die aus derselben Bilddatei zugeschnitten werden.</span><span class="sxs-lookup"><span data-stu-id="885fb-160">You can use the **cropbottom**, **croptop**, **cropleft**, and **cropright** property attributes of the `<image>` element to display different pictures that are cropped from the same image file.</span></span>

<span data-ttu-id="885fb-161">Der Wert dieser zuschnittsattribute stellt den Prozentsatz aus dem Rand des Bilds dar.</span><span class="sxs-lookup"><span data-stu-id="885fb-161">The value of these crop attributes represents the percentage cut from the edge of the picture.</span></span> <span data-ttu-id="885fb-162">Der Wert kann eine beliebige Zahl zwischen 0 und 1 sein.</span><span class="sxs-lookup"><span data-stu-id="885fb-162">The value can be any number between 0 to 1.</span></span> <span data-ttu-id="885fb-163">Standardmäßig wird der Wert auf 0 festgelegt, was bedeutet, dass keine Zuschneiden von der Kante erfolgt.</span><span class="sxs-lookup"><span data-stu-id="885fb-163">By default, the value is set to 0, indicating no crop from the edge.</span></span> <span data-ttu-id="885fb-164">Der Wert 0,1 gibt an, dass 10 Prozent von der Kante abgeschnitten werden. der Wert 0,15 gibt an, dass der Rand 15 Prozent überspringt usw.</span><span class="sxs-lookup"><span data-stu-id="885fb-164">The value 0.1 indicates a cropping of 10 percent from the edge, The value 0.15 indicates a cropping of 15 percent from the edge, and so on.</span></span>

<span data-ttu-id="885fb-165">Wenn Sie z. b. fünf Bilder anzeigen möchten, die alle aus derselben Bilddatei entfernt wurden, können Sie das `<image>` -Element verwenden und andere zuschnittwerte angeben, wie in der folgenden VML-Darstellung dargestellt:</span><span class="sxs-lookup"><span data-stu-id="885fb-165">For example, to display five pictures that are all cropped from the same image file, you can use the `<image>` element and specify different crop values, as shown in the following VML representation:</span></span>

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





<span data-ttu-id="885fb-171">Das erste Bild, `<v:image style='width:100pt;height:80pt' src="image1.jpg" />` , verfügt über keinen zuschöpfungs Wert.</span><span class="sxs-lookup"><span data-stu-id="885fb-171">The first image, `<v:image style='width:100pt;height:80pt' src="image1.jpg" />`, doesn't have any crop value.</span></span> <span data-ttu-id="885fb-172">Aus diesem Grund wird 100 Prozent des ursprünglichen Abbilds mit einer Größe von 100 Punkten um 80 Punkte angezeigt.</span><span class="sxs-lookup"><span data-stu-id="885fb-172">Therefore, 100 percent of the original image is displayed at a size of 100 points by 80 points.</span></span>

<span data-ttu-id="885fb-173">Das zweite Bild, `<v:image style='width:85pt;height:64pt' src="image1.jpg" cropbottom="0.2" cropright="0.15"/>` , weist einige zuschnittwerte auf.</span><span class="sxs-lookup"><span data-stu-id="885fb-173">The second image, `<v:image style='width:85pt;height:64pt' src="image1.jpg" cropbottom="0.2" cropright="0.15"/>`, has some crop values.</span></span> <span data-ttu-id="885fb-174">`cropbottom="0.2"` Gibt an, dass 20 Prozent des Bilds vom unteren Rand abgeschnitten werden. `cropright="0.15"` gibt an, dass 15 Prozent des Bilds vom rechten Rand abgeschnitten werden.</span><span class="sxs-lookup"><span data-stu-id="885fb-174">`cropbottom="0.2"` indicates that 20 percent of the picture will be cropped from the bottom; `cropright="0.15"` indicates that 15 percent of the picture will be cropped from the right edge.</span></span> <span data-ttu-id="885fb-175">Das verbleibende Bild wird dann mit einer Größe von 85 Punkten um 64 Punkte angezeigt.</span><span class="sxs-lookup"><span data-stu-id="885fb-175">The remaining picture is then displayed at a size of 85 points by 64 points.</span></span>

<span data-ttu-id="885fb-176">Ähnlich weisen die Dritten, vierten und fünften Bilder einige zuschnittwerte auf.</span><span class="sxs-lookup"><span data-stu-id="885fb-176">Similarly the third, fourth, and fifth images have some crop values.</span></span> <span data-ttu-id="885fb-177">Das ursprüngliche Bild wird entsprechend den zuschnittwerten zugeschnitten und dann entsprechend dem Wert von Width und Height angezeigt.</span><span class="sxs-lookup"><span data-stu-id="885fb-177">The original picture is cropped according to the crop values, and is then displayed according to the value of width and height.</span></span>

<span data-ttu-id="885fb-178">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="885fb-178">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="contrast"></a><span data-ttu-id="885fb-179">Kontrast</span><span class="sxs-lookup"><span data-stu-id="885fb-179">contrast</span></span>

<span data-ttu-id="885fb-180">Sie können das Attribut "Eigenschaft **erwerben** " des- `<image>` Elements verwenden, um verschiedene Bilder mit unterschiedlichen Kontrasteinstellungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="885fb-180">You can use the **gain** property attribute of the `<image>` element to display various pictures that have different contrast settings.</span></span>

<span data-ttu-id="885fb-181">Der Wert des Attributs für die **Attribut Eigenschaft kann** beliebig sein.</span><span class="sxs-lookup"><span data-stu-id="885fb-181">The value of the **gain** property attribute can be any number.</span></span> <span data-ttu-id="885fb-182">Standardmäßig ist der Wert 1, was die Verwendung des gleichen Kontrast wie das ursprüngliche Bild angibt.</span><span class="sxs-lookup"><span data-stu-id="885fb-182">By default, the value is 1, indicating the use of the same contrast as the original image.</span></span> <span data-ttu-id="885fb-183">Der Wert 0 gibt keinen Kontrast an.</span><span class="sxs-lookup"><span data-stu-id="885fb-183">The value 0 indicates no contrast.</span></span> <span data-ttu-id="885fb-184">Je größer die Zahl, desto höher der Kontrast.</span><span class="sxs-lookup"><span data-stu-id="885fb-184">The larger the number, the higher the contrast.</span></span>

<span data-ttu-id="885fb-185">Wenn Sie z. b. fünf Bilder mit unterschiedlichen Kontrasteinstellungen anzeigen möchten, können Sie das `<image>` -Element verwenden und einen anderen Wert für das Attribut "Eigenschaft **erhalten** " festlegen, wie in der folgenden VML-Darstellung dargestellt:</span><span class="sxs-lookup"><span data-stu-id="885fb-185">For example, to display five pictures that have different contrast settings, you can use the `<image>` element and set a different value for the **gain** property attribute, as shown in the following VML representation:</span></span>

![image1.jpg (5770 Bytes)](images/image1.jpg)![Image2 \-2.jpg (270 bytes)](images/image2-2.jpg)![Image2 \-3.jpg (1919 Bytes)](images/image2-3.jpg)![Image2 \-4.jpg (3143 Bytes)](images/image2-4.jpg)![Image2 \-5.jpg (1724 Bytes)](images/image2-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=0 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=0.5 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=3 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=-0.4 />
```





<span data-ttu-id="885fb-191">Wenn das Attribut für die Eigenschaft " **Gewinn** " auf 0 festgelegt ist, wird das gesamte Bild grau, da kein Kontrast vorliegt.</span><span class="sxs-lookup"><span data-stu-id="885fb-191">When the **gain** property attribute is set to 0, the entire image becomes gray because there is no contrast.</span></span> <span data-ttu-id="885fb-192">Der Kontrast ist deutlicher, wenn das Attribut für die Eigenschaft " **Gewinn** " auf den Wert "0,5" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="885fb-192">The contrast is more noticeable when the **gain** property attribute is set to 3 than when it is set to 0.5.</span></span> <span data-ttu-id="885fb-193">Der Kontrast wird umgekehrt, wenn das Attribut für die Eigenschaft " **Gewinn** " auf einen negativen Wert wie "-0,4" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="885fb-193">The contrast is reversed when the **gain** property attribute is set to a negative value such as -0.4.</span></span>

<span data-ttu-id="885fb-194">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="885fb-194">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="brightness"></a><span data-ttu-id="885fb-195">Helligkeit</span><span class="sxs-lookup"><span data-stu-id="885fb-195">brightness</span></span>

<span data-ttu-id="885fb-196">Sie können das Attribut der **Blacklevel** -Eigenschaft des- `<image>` Elements verwenden, um verschiedene Bilder mit unterschiedlichen Helligkeitseinstellungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="885fb-196">You can use the **blacklevel** property attribute of the `<image>` element to display various pictures that have different brightness settings.</span></span>

<span data-ttu-id="885fb-197">Der Wert des Attributs der **Blacklevel** -Eigenschaft kann ein beliebiger Wert zwischen 0 und 1 sein.</span><span class="sxs-lookup"><span data-stu-id="885fb-197">The value of the **blacklevel** property attribute can be any value between 0 to 1.</span></span> <span data-ttu-id="885fb-198">Standardmäßig ist der Wert 0 (null) und gibt an, dass die Ebene der Helligkeit im ursprünglichen Bild beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="885fb-198">By default, the value is 0, indicating that the level of brightness in the original image is preserved.</span></span> <span data-ttu-id="885fb-199">Der Wert 1 gibt den höchsten Grad an Helligkeit an.</span><span class="sxs-lookup"><span data-stu-id="885fb-199">The value 1 indicates the highest level of brightness.</span></span>

<span data-ttu-id="885fb-200">Wenn Sie z. b. fünf Bilder mit unterschiedlichen Helligkeitseinstellungen anzeigen möchten, können Sie das `<image>` -Element verwenden und einen anderen Wert für das Attribut der **Blacklevel** -Eigenschaft festlegen, wie in der folgenden VML-Darstellung dargestellt:</span><span class="sxs-lookup"><span data-stu-id="885fb-200">For example, to display five pictures that have different brightness settings, you can use the `<image>` element and set a different value for the **blacklevel** property attribute, as shown in the following VML representation:</span></span>

![image1.jpg (5770 Bytes)](images/image1.jpg)![image3 \-2.jpg (2579 Bytes)](images/image3-2.jpg)![image3 \-3.jpg (2330 Bytes)](images/image3-3.jpg)![image3 \-4.jpg (2727 Bytes)](images/image3-4.jpg)![image3 \-5.jpg (2435 Bytes)](images/image3-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=0.1 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=0.2 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=-0.05 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=-0.15 />
```





<span data-ttu-id="885fb-206">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="885fb-206">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="grayscale"></a><span data-ttu-id="885fb-207">Graustufe</span><span class="sxs-lookup"><span data-stu-id="885fb-207">grayscale</span></span>

<span data-ttu-id="885fb-208">Sie können das **Graustufen** Eigenschafts Attribut des- `<image>` Elements verwenden, um Bilder mit oder ohne Graustufen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="885fb-208">You can use the **grayscale** property attribute of the `<image>` element to display pictures with or without grayscale.</span></span>

<span data-ttu-id="885fb-209">Der Wert des **Graustufen** Eigenschafts Attributs kann entweder "true" oder "false" sein.</span><span class="sxs-lookup"><span data-stu-id="885fb-209">The value of the **grayscale** property attribute can be either true or false.</span></span> <span data-ttu-id="885fb-210">Standardmäßig ist der Wert auf false festgelegt, damit das Bild in Farbe angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="885fb-210">By default, the value is set to false so that the image will be displayed in color.</span></span> <span data-ttu-id="885fb-211">Wenn der Wert auf true festgelegt ist, wird das Bild in Graustufen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="885fb-211">If the value is set to true, the image will be displayed in grayscale.</span></span>

<span data-ttu-id="885fb-212">Beispielsweise verwendet das erste Bild, wie in der folgenden Abbildung gezeigt, die Standardeinstellung (false) des Graustufen-Attributs ( `<v:image style='width:100pt;height:80pt' src="image1.jpg" />` ).</span><span class="sxs-lookup"><span data-stu-id="885fb-212">For example, as shown in the following picture, the first image uses the default setting (false)of the grayscale attribute (`<v:image style='width:100pt;height:80pt' src="image1.jpg" />` ).</span></span> <span data-ttu-id="885fb-213">Daher wird das Bild in Farbe angezeigt.</span><span class="sxs-lookup"><span data-stu-id="885fb-213">Therefore, the picture is displayed in color.</span></span>

<span data-ttu-id="885fb-214">Das zweite Bild legt das Graustufen Attribut auf "true ()" fest `<v:image style='width:100pt;height:80pt' src="image1.jpg" grayscale=true />` .</span><span class="sxs-lookup"><span data-stu-id="885fb-214">The second image sets the grayscale attribute to true (`<v:image style='width:100pt;height:80pt' src="image1.jpg" grayscale=true />` ).</span></span> <span data-ttu-id="885fb-215">Daher wird das Bild in Graustufen angezeigt, wie in der folgenden VML-Darstellung dargestellt:</span><span class="sxs-lookup"><span data-stu-id="885fb-215">Therefore, the picture is displayed in grayscale, as shown in the following VML representation:</span></span>

![image1.jpg (5770 Bytes)](images/image1.jpg)!["image4 \-2.jpg (2138 Bytes)](images/image4-2.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg"
grayscale=true />
```





<span data-ttu-id="885fb-218">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="885fb-218">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="gamma"></a><span data-ttu-id="885fb-219">Gamma</span><span class="sxs-lookup"><span data-stu-id="885fb-219">gamma</span></span>

<span data-ttu-id="885fb-220">Sie können das **Gamma** Property-Attribut des- `<image>` Elements verwenden, um Bilder mit unterschiedlichen Gamma Einstellungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="885fb-220">You can use the **gamma** property attribute of the `<image>` element to display pictures that have different gamma settings.</span></span>

<span data-ttu-id="885fb-221">Der Wert des Gamma property-Attributs kann ein beliebiger Wert zwischen 0 und 1 sein.</span><span class="sxs-lookup"><span data-stu-id="885fb-221">The value of the gamma property attribute can be any value between 0 and 1.</span></span> <span data-ttu-id="885fb-222">Standardmäßig ist der Wert auf 1 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="885fb-222">By default, the value is set to 1.</span></span>

<span data-ttu-id="885fb-223">Wenn Sie z. b. drei Bilder mit unterschiedlichen Gamma Einstellungen anzeigen möchten, können Sie das `<image>` -Element verwenden und einen anderen Wert des **Gamma** property-Attributs festlegen, wie in der folgenden VML-Darstellung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="885fb-223">For example, to display three pictures that have different gamma settings, you can use the `<image>` element and set a different value of the **gamma** property attribute, as shown in the following VML representation:</span></span>

![image5 \-1.jpg (2714 Bytes)](images/image5-1.jpg)![image5 \-2.jpg (2729 Bytes)](images/image5-2.jpg)![image5 \-3.jpg (2726 Bytes)](images/image5-3.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gamma=0 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gamma=0.5 />
```





<span data-ttu-id="885fb-227">Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation](https://www.w3.org/TR/NOTE-VML#-toc416858408) .</span><span class="sxs-lookup"><span data-stu-id="885fb-227">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858408) .</span></span>

 

 