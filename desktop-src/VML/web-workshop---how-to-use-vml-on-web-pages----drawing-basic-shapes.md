---
title: Zeichnen von grundlegenden Formen
description: In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.
ms.assetid: 05443e1f-c098-441c-a5bc-274cc37ef074
keywords:
- Webworkshop, Zeichnen von Formen
- Entwerfen von Webseiten, Zeichnen von Formen
- Vector Markup Language (VML), Zeichnen von Formen
- VML (Vector Markup Language), Zeichnen von Formen
- Vektorgrafiken, Zeichnungsformen
- Zeichnen von Formen
- VML-Formen, zeichnen
- Vector Markup Language (VML), XML
- VML (Vector Markup Language), XML
- Vektorgrafiken, XML
- Vector Markup Language (VML), CSS2
- VML (Vector Markup Language), CSS2
- Vektorgrafiken, CSS2
- Vector Markup Language (VML), Elemente
- VML (Vector Markup Language), Elemente
- Vektorgrafiken, Elemente
- VML-Elemente, Zeichnen von Formen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7ab25fc9310750c9f49c5978a063c76639ec4bd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474012"
---
# <a name="drawing-basic-shapes"></a><span data-ttu-id="21a4c-121">Zeichnen von grundlegenden Formen</span><span class="sxs-lookup"><span data-stu-id="21a4c-121">Drawing Basic Shapes</span></span>

<span data-ttu-id="21a4c-122">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="21a4c-122">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="21a4c-123">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="21a4c-123">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="21a4c-124">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="21a4c-124">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="21a4c-125">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="21a4c-125">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="21a4c-126">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="21a4c-126">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="21a4c-127">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="21a4c-127">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="21a4c-128">In diesem Thema wird veranschaulicht, wie einfach es ist, eine Form mithilfe von VML zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="21a4c-128">In this topic, we will illustrate how easy it is to draw a shape using VML.</span></span>

<span data-ttu-id="21a4c-129">Zum Erstellen eines roten Oval auf einer Webseite, wie in der folgenden Abbildung gezeigt, können Sie das Oval mit einem Grafik Bearbeitungs Tool zeichnen, die Zeichnung als Bitmap speichern und dann die Bitmap auf der Webseite einfügen:</span><span class="sxs-lookup"><span data-stu-id="21a4c-129">To create a red oval on a Web page, as shown in the following picture, you can draw the oval by using a graphic edit tool, save your drawing as a bitmap, and then insert the bitmap on your Web page:</span></span>

![oval1.gif (627 Bytes)](images/oval1.gif)

<span data-ttu-id="21a4c-131">Alternativ können Sie mit VML Grafiken zeichnen.</span><span class="sxs-lookup"><span data-stu-id="21a4c-131">Alternatively, you can use VML to draw graphics.</span></span> <span data-ttu-id="21a4c-132">Im vorherigen Beispiel können Sie die folgenden Zeilen in der `<BODY>` Region der Webseite eingeben, um das rote Oval zu zeichnen:</span><span class="sxs-lookup"><span data-stu-id="21a4c-132">In the preceding example, you can type the following lines in the `<BODY>` region of your Web page to draw the red oval:</span></span>


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red"> </v:oval>
```





<span data-ttu-id="21a4c-133">`<v:...>` und `</v:...>` sind das Starttag und das Endtag in der [XML-Syntax](#xml-structure).`style='width:100pt; height:75pt'`</span><span class="sxs-lookup"><span data-stu-id="21a4c-133">`<v:...>` and `</v:...>` are the start tag and end tag in [XML syntax](#xml-structure).`style='width:100pt; height:75pt'`</span></span> <span data-ttu-id="21a4c-134">stellt [CSS-Informationen](#css-information)bereit.</span><span class="sxs-lookup"><span data-stu-id="21a4c-134">provides [CSS information](#css-information).</span></span> <span data-ttu-id="21a4c-135">**Oval** und **FillColor**= "Red" sind [VML-Elemente](#vml-elements).</span><span class="sxs-lookup"><span data-stu-id="21a4c-135">**oval** and **fillcolor**="red" are [VML elements](#vml-elements).</span></span>

<span data-ttu-id="21a4c-136">Sie können die Grafiken ändern, indem Sie einfach Ihre Eigenschafts Attribute in VML ändern.</span><span class="sxs-lookup"><span data-stu-id="21a4c-136">You can alter the graphics by simply changing their property attributes in VML.</span></span> <span data-ttu-id="21a4c-137">Wenn Sie im vorherigen Beispiel zu wechseln, `fillcolor="red"` `fillcolor="blue"` wie in der folgenden VML-Darstellung gezeigt, ändert sich das rote Oval in blau:</span><span class="sxs-lookup"><span data-stu-id="21a4c-137">In the preceding example, if you change `fillcolor="red"` to `fillcolor="blue"`, as shown in the following VML representation, the red oval will change to blue:</span></span>


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="blue"> </v:oval>
```





<span data-ttu-id="21a4c-138">Browser, die VML unterstützen, können die in VML dargestellten Grafiken renderten und anzeigen, ohne separate Bilddateien herunterladen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="21a4c-138">Browsers that support VML can render and display the graphics represented in VML without having to download separate image files.</span></span> <span data-ttu-id="21a4c-139">Die meisten in VML dargestellten Grafiken werden in Browsern schneller gerendert und erfordern weniger Speicherplatz und Downloadzeit.</span><span class="sxs-lookup"><span data-stu-id="21a4c-139">Most graphics represented in VML are rendered faster in browsers, and require less disk space and download time.</span></span>

<span data-ttu-id="21a4c-140">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="21a4c-140">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="xml-structure"></a><span data-ttu-id="21a4c-141">XML-Struktur</span><span class="sxs-lookup"><span data-stu-id="21a4c-141">XML Structure</span></span>

<span data-ttu-id="21a4c-142">VML wird gemäß den Regeln der Extensible Markup Language (XML) formatiert.</span><span class="sxs-lookup"><span data-stu-id="21a4c-142">VML is formatted according to the rules of Extensible Markup Language (XML).</span></span> <span data-ttu-id="21a4c-143">Jeder Standard-XML-Parser kann VML analysieren und die resultierenden Daten an einen VML-spezifischen Prozessor übergeben.</span><span class="sxs-lookup"><span data-stu-id="21a4c-143">Any standard XML parser can parse VML and hand off the resulting data to a VML-specific processor.</span></span> <span data-ttu-id="21a4c-144">Wenn Sie den Browsern mitteilen möchten, wie Daten an einen VML-spezifischen Prozessor übergeben werden, müssen Sie einige Informationen eingeben, wie z. b. [Namespaces](web-workshop---how-to-use-vml-on-web-pages----appendix.md) und [eingebettete benutzerdefinierte Objekte](web-workshop---how-to-use-vml-on-web-pages----appendix.md).</span><span class="sxs-lookup"><span data-stu-id="21a4c-144">To let the browsers know how to hand off data to a VML-specific processor, you need to type some information such as [namespaces](web-workshop---how-to-use-vml-on-web-pages----appendix.md) and [embedded custom objects](web-workshop---how-to-use-vml-on-web-pages----appendix.md).</span></span> <span data-ttu-id="21a4c-145">Anschließend können Sie mit VML Grafiken in der `<BODY>` Region wie im vorherigen Beispiel eingeben.</span><span class="sxs-lookup"><span data-stu-id="21a4c-145">You can then use VML to type graphics in the `<BODY>` region just as you did in the preceding example.</span></span>

<span data-ttu-id="21a4c-146">`"v:"`Mit dem Präfix für jedes XML-Tag wird das Tag als VML identifiziert.</span><span class="sxs-lookup"><span data-stu-id="21a4c-146">The `"v:"` prefix on each XML tag identifies the tag as VML.</span></span> <span data-ttu-id="21a4c-147">Das `"v:"` Präfix in der `<BODY>` Region sollte mit übereinstimmen `<html xmlns:v="...">` .</span><span class="sxs-lookup"><span data-stu-id="21a4c-147">The `"v:"` prefix in the `<BODY>` region should be consistent with `<html xmlns:v="...">`.</span></span>

<span data-ttu-id="21a4c-148">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="21a4c-148">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="css-information"></a><span data-ttu-id="21a4c-149">CSS-Informationen</span><span class="sxs-lookup"><span data-stu-id="21a4c-149">CSS Information</span></span>

<span data-ttu-id="21a4c-150">VML verwendet [Cascading Stylesheets, Ebene 2 (CSS2),](https://www.w3.org/TR/PR-CSS2/) um die Größe der Grafiken zu bestimmen und die Grafiken auf einer Webseite zu positionieren.</span><span class="sxs-lookup"><span data-stu-id="21a4c-150">VML uses [Cascading Style Sheets, Level 2 (CSS2)](https://www.w3.org/TR/PR-CSS2/) to determine the size of the graphics and to position the graphics on a Web page.</span></span> <span data-ttu-id="21a4c-151">Im vorherigen Beispiel haben wir die Größe des Oval als 100 Punkte (Breite) um 75 Punkte (Höhe) ( `style='width:100pt;height:75pt'` ) angegeben.</span><span class="sxs-lookup"><span data-stu-id="21a4c-151">In the preceding example, we specified the size of the oval as 100 points (width) by 75 points (height) (`style='width:100pt;height:75pt'` ).</span></span>

<span data-ttu-id="21a4c-152">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="21a4c-152">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="vml-elements"></a><span data-ttu-id="21a4c-153">VML-Elemente</span><span class="sxs-lookup"><span data-stu-id="21a4c-153">VML Elements</span></span>

<span data-ttu-id="21a4c-154">Im vorherigen Beispiel haben wir ein vordefiniertes VML-Element verwendet, `<oval>` um ein Oval zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="21a4c-154">In the preceding example, we used a VML predefined `<oval>` element to draw an oval.</span></span> <span data-ttu-id="21a4c-155">Anschließend haben wir das **FillColor** -Eigenschafts Attribut des- `<oval>` Elements verwendet, um das Oval in rot auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="21a4c-155">We then used the **fillcolor** property attribute of the `<oval>` element to fill the oval with red.</span></span>

<span data-ttu-id="21a4c-156">Basierend auf dem [Starttags-, Endtags-und Empty-Element Tags-](https://www.w3.org/TR/REC-xml#sec-starttags) Abschnitt der [Spezifikation von XML 1,0](https://www.w3.org/TR/REC-xml)können leere Element Tags für alle Elemente verwendet werden, die über keinen Inhalt verfügen.</span><span class="sxs-lookup"><span data-stu-id="21a4c-156">Based upon the [Start-Tags, End-Tags, and Empty-Element Tags](https://www.w3.org/TR/REC-xml#sec-starttags) section of [XML 1.0 specification](https://www.w3.org/TR/REC-xml), empty-element tags may be used for any element that has no content.</span></span> <span data-ttu-id="21a4c-157">Beispielsweise gibt es in der folgenden VML-Darstellung keinen Inhalt (Unterelement) innerhalb des- `<oval>` Elements.</span><span class="sxs-lookup"><span data-stu-id="21a4c-157">For example, as shown in the following VML representation, there is no content (sub-element) within the `<oval>` element.</span></span> <span data-ttu-id="21a4c-158">(Beachten Sie, dass **Stil** und **FillColor** die Attribute des- `<oval>` Elements sind; Sie sind keine unter Elemente.)</span><span class="sxs-lookup"><span data-stu-id="21a4c-158">(Note that the **style** and **fillcolor** are the attributes of the `<oval>` element; they are not sub-elements.)</span></span>


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red"> </v:oval>
```



<span data-ttu-id="21a4c-159">Daher können Sie das Tag "Empty-Element" verwenden, wie in der folgenden VML-Darstellung dargestellt, um das gleiche Element wie die obige Zeile darzustellen.</span><span class="sxs-lookup"><span data-stu-id="21a4c-159">Therefore, you can use the empty-element tag, as shown in the following VML representation, to represent the same thing as the above line.</span></span>


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red" />
```



<span data-ttu-id="21a4c-160">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="21a4c-160">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="21a4c-161">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="21a4c-161">Summary</span></span>

<span data-ttu-id="21a4c-162">Sie können VML verwenden, um Grafiken auf einer Webseite zu zeichnen, und dann diese Grafiken anpassen, indem Sie einfach Ihre Eigenschafts Attribute ändern.</span><span class="sxs-lookup"><span data-stu-id="21a4c-162">You can use VML to draw graphics on a Web page, and then customize those graphics by simply changing their property attributes.</span></span> <span data-ttu-id="21a4c-163">Außerdem werden die meisten in VML dargestellten Grafiken schneller in Browsern gerendert und benötigen weniger Downloadzeit und Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="21a4c-163">Also, most graphics represented in VML are rendered faster in browsers, and take less download time and disk space.</span></span>

 

 