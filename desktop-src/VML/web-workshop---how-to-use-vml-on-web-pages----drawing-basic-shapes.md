---
title: Zeichnen grundlegender Formen
description: In diesem Artikel wird das Zeichnen grundlegender Formen in VML beschrieben, einem Feature, das seit Windows Internet Explorer 9 veraltet ist.
ms.assetid: 05443e1f-c098-441c-a5bc-274cc37ef074
keywords:
- Web-Workshop,Zeichnen von Formen
- Entwerfen von Webseiten, Zeichnen von Formen
- Vector Markup Language (VML), Zeichnen von Formen
- VML (Vector Markup Language), Zeichnen von Formen
- Vektorgrafiken,Zeichnen von Formen
- Zeichnen von Formen
- VML-Formen,Zeichnen
- Vector Markup Language (VML),XML
- VML (Vector Markup Language),XML
- Vektorgrafiken,XML
- Vector Markup Language (VML),CSS2
- VML (Vector Markup Language),CSS2
- Vektorgrafiken,CSS2
- Vector Markup Language (VML),Elemente
- VML (Vector Markup Language),Elemente
- Vektorgrafiken,Elemente
- VML-Elemente, Zeichnen von Formen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00701e8ac77bd5bda7156c04ca25427d131646bf
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407733"
---
# <a name="drawing-basic-shapes"></a><span data-ttu-id="5fe81-120">Zeichnen grundlegender Formen</span><span class="sxs-lookup"><span data-stu-id="5fe81-120">Drawing Basic Shapes</span></span>

<span data-ttu-id="5fe81-121">In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="5fe81-121">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="5fe81-122">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="5fe81-122">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="5fe81-123">Seit Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="5fe81-123">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="5fe81-124">Daher wird sie nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="5fe81-124">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="5fe81-125">Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/)</span><span class="sxs-lookup"><span data-stu-id="5fe81-125">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="5fe81-126">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)</span><span class="sxs-lookup"><span data-stu-id="5fe81-126">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="5fe81-127">In diesem Thema wird veranschaulicht, wie einfach es ist, eine Form mithilfe von VML zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="5fe81-127">In this topic, we will illustrate how easy it is to draw a shape using VML.</span></span>

<span data-ttu-id="5fe81-128">Um ein rotes Oval auf einer Webseite zu erstellen, wie in der folgenden Abbildung dargestellt, können Sie das Oval mithilfe eines Grafischen Bearbeitungstools zeichnen, die Zeichnung als Bitmap speichern und die Bitmap dann auf Ihrer Webseite einfügen:</span><span class="sxs-lookup"><span data-stu-id="5fe81-128">To create a red oval on a Web page, as shown in the following picture, you can draw the oval by using a graphic edit tool, save your drawing as a bitmap, and then insert the bitmap on your Web page:</span></span>

![oval1.gif (627 Bytes)](images/oval1.gif)

<span data-ttu-id="5fe81-130">Alternativ können Sie VML verwenden, um Grafiken zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="5fe81-130">Alternatively, you can use VML to draw graphics.</span></span> <span data-ttu-id="5fe81-131">Im vorherigen Beispiel können Sie die folgenden Zeilen in den Bereich ihrer Webseite eingeben, um das rote Oval `<BODY>` zu zeichnen:</span><span class="sxs-lookup"><span data-stu-id="5fe81-131">In the preceding example, you can type the following lines in the `<BODY>` region of your Web page to draw the red oval:</span></span>


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red"> </v:oval>
```





<span data-ttu-id="5fe81-132">`<v:...>`und `</v:...>` sind das Start- und Endtag in der [XML-Syntax.](#xml-structure)`style='width:100pt; height:75pt'`</span><span class="sxs-lookup"><span data-stu-id="5fe81-132">`<v:...>` and `</v:...>` are the start tag and end tag in [XML syntax](#xml-structure).`style='width:100pt; height:75pt'`</span></span> <span data-ttu-id="5fe81-133">stellt [CSS-Informationen zur Verfügung.](#css-information)</span><span class="sxs-lookup"><span data-stu-id="5fe81-133">provides [CSS information](#css-information).</span></span> <span data-ttu-id="5fe81-134">**oval** und **fillcolor**="red" sind [VML-Elemente.](#vml-elements)</span><span class="sxs-lookup"><span data-stu-id="5fe81-134">**oval** and **fillcolor**="red" are [VML elements](#vml-elements).</span></span>

<span data-ttu-id="5fe81-135">Sie können die Grafiken ändern, indem Sie einfach deren Eigenschaftsattribute in VML ändern.</span><span class="sxs-lookup"><span data-stu-id="5fe81-135">You can alter the graphics by simply changing their property attributes in VML.</span></span> <span data-ttu-id="5fe81-136">Wenn Sie im vorherigen Beispiel in ändern, wie in der folgenden VML-Darstellung gezeigt, ändert sich das rote `fillcolor="red"` `fillcolor="blue"` Oval in Blau:</span><span class="sxs-lookup"><span data-stu-id="5fe81-136">In the preceding example, if you change `fillcolor="red"` to `fillcolor="blue"`, as shown in the following VML representation, the red oval will change to blue:</span></span>


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="blue"> </v:oval>
```





<span data-ttu-id="5fe81-137">Browser, die VML unterstützen, können die in VML dargestellten Grafiken rendern und anzeigen, ohne separate Bilddateien herunterladen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="5fe81-137">Browsers that support VML can render and display the graphics represented in VML without having to download separate image files.</span></span> <span data-ttu-id="5fe81-138">Die meisten in VML dargestellten Grafiken werden in Browsern schneller gerendert und erfordern weniger Speicherplatz und Downloadzeit.</span><span class="sxs-lookup"><span data-stu-id="5fe81-138">Most graphics represented in VML are rendered faster in browsers, and require less disk space and download time.</span></span>

<span data-ttu-id="5fe81-139">[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="5fe81-139">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="xml-structure"></a><span data-ttu-id="5fe81-140">XML-Struktur</span><span class="sxs-lookup"><span data-stu-id="5fe81-140">XML Structure</span></span>

<span data-ttu-id="5fe81-141">VML wird gemäß den Regeln von Extensible Markup Language (XML) formatiert.</span><span class="sxs-lookup"><span data-stu-id="5fe81-141">VML is formatted according to the rules of Extensible Markup Language (XML).</span></span> <span data-ttu-id="5fe81-142">Jeder XML-Standardparser kann VML analysieren und die resultierenden Daten an einen VML-spezifischen Prozessor aushingen.</span><span class="sxs-lookup"><span data-stu-id="5fe81-142">Any standard XML parser can parse VML and hand off the resulting data to a VML-specific processor.</span></span> <span data-ttu-id="5fe81-143">Damit die Browser wissen, wie Daten an einen VML-spezifischen Prozessor übergefertigt werden, müssen Sie einige Informationen wie [Namespaces](web-workshop---how-to-use-vml-on-web-pages----appendix.md) und eingebettete benutzerdefinierte [Objekte eingeben.](web-workshop---how-to-use-vml-on-web-pages----appendix.md)</span><span class="sxs-lookup"><span data-stu-id="5fe81-143">To let the browsers know how to hand off data to a VML-specific processor, you need to type some information such as [namespaces](web-workshop---how-to-use-vml-on-web-pages----appendix.md) and [embedded custom objects](web-workshop---how-to-use-vml-on-web-pages----appendix.md).</span></span> <span data-ttu-id="5fe81-144">Anschließend können Sie VML verwenden, um Grafiken wie im vorherigen Beispiel in der `<BODY>` Region ein typ zu geben.</span><span class="sxs-lookup"><span data-stu-id="5fe81-144">You can then use VML to type graphics in the `<BODY>` region just as you did in the preceding example.</span></span>

<span data-ttu-id="5fe81-145">Das `"v:"` Präfix für jedes XML-Tag identifiziert das Tag als VML.</span><span class="sxs-lookup"><span data-stu-id="5fe81-145">The `"v:"` prefix on each XML tag identifies the tag as VML.</span></span> <span data-ttu-id="5fe81-146">Das `"v:"` Präfix in der Region sollte mit konsistent `<BODY>` `<html xmlns:v="...">` sein.</span><span class="sxs-lookup"><span data-stu-id="5fe81-146">The `"v:"` prefix in the `<BODY>` region should be consistent with `<html xmlns:v="...">`.</span></span>

<span data-ttu-id="5fe81-147">[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="5fe81-147">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="css-information"></a><span data-ttu-id="5fe81-148">CSS-Informationen</span><span class="sxs-lookup"><span data-stu-id="5fe81-148">CSS Information</span></span>

<span data-ttu-id="5fe81-149">VML verwendet [Cascading Stylesheets, Ebene 2 (CSS2),](https://www.w3.org/TR/PR-CSS2/) um die Größe der Grafiken zu bestimmen und die Grafiken auf einer Webseite zu positionieren.</span><span class="sxs-lookup"><span data-stu-id="5fe81-149">VML uses [Cascading Style Sheets, Level 2 (CSS2)](https://www.w3.org/TR/PR-CSS2/) to determine the size of the graphics and to position the graphics on a Web page.</span></span> <span data-ttu-id="5fe81-150">Im vorherigen Beispiel haben wir die Größe des Ovals als 100 Punkte (Breite) um 75 Punkte (Höhe) ( ) `style='width:100pt;height:75pt'` angegeben.</span><span class="sxs-lookup"><span data-stu-id="5fe81-150">In the preceding example, we specified the size of the oval as 100 points (width) by 75 points (height) (`style='width:100pt;height:75pt'` ).</span></span>

<span data-ttu-id="5fe81-151">[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="5fe81-151">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="vml-elements"></a><span data-ttu-id="5fe81-152">VML-Elemente</span><span class="sxs-lookup"><span data-stu-id="5fe81-152">VML Elements</span></span>

<span data-ttu-id="5fe81-153">Im vorherigen Beispiel haben wir ein vordefiniertes VML-Element `<oval>` verwendet, um ein Oval zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="5fe81-153">In the preceding example, we used a VML predefined `<oval>` element to draw an oval.</span></span> <span data-ttu-id="5fe81-154">Anschließend haben wir das **fillcolor-Eigenschaftsattribut** des Elements verwendet, um das Oval mit Rot zu `<oval>` füllen.</span><span class="sxs-lookup"><span data-stu-id="5fe81-154">We then used the **fillcolor** property attribute of the `<oval>` element to fill the oval with red.</span></span>

<span data-ttu-id="5fe81-155">Basierend auf [dem Abschnitt Start-Tags, Endtags](https://www.w3.org/TR/REC-xml#sec-starttags) und Empty-Element Tags der [XML 1.0-Spezifikation](https://www.w3.org/TR/REC-xml)können leere Elementtags für jedes Element ohne Inhalt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5fe81-155">Based upon the [Start-Tags, End-Tags, and Empty-Element Tags](https://www.w3.org/TR/REC-xml#sec-starttags) section of [XML 1.0 specification](https://www.w3.org/TR/REC-xml), empty-element tags may be used for any element that has no content.</span></span> <span data-ttu-id="5fe81-156">Wie in der folgenden VML-Darstellung gezeigt, gibt es beispielsweise keinen Inhalt (Unterelement) innerhalb des `<oval>` -Elements.</span><span class="sxs-lookup"><span data-stu-id="5fe81-156">For example, as shown in the following VML representation, there is no content (sub-element) within the `<oval>` element.</span></span> <span data-ttu-id="5fe81-157">(Beachten Sie, **dass stil** und **fillcolor** die Attribute des Elements `<oval>` sind. Sie sind keine Unterelemente.)</span><span class="sxs-lookup"><span data-stu-id="5fe81-157">(Note that the **style** and **fillcolor** are the attributes of the `<oval>` element; they are not sub-elements.)</span></span>


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red"> </v:oval>
```



<span data-ttu-id="5fe81-158">Daher können Sie das Empty-Element-Tag wie in der folgenden VML-Darstellung gezeigt verwenden, um dasselbe wie in der obigen Zeile zu repräsentieren.</span><span class="sxs-lookup"><span data-stu-id="5fe81-158">Therefore, you can use the empty-element tag, as shown in the following VML representation, to represent the same thing as the above line.</span></span>


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red" />
```



<span data-ttu-id="5fe81-159">[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="5fe81-159">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="5fe81-160">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="5fe81-160">Summary</span></span>

<span data-ttu-id="5fe81-161">Sie können VML verwenden, um Grafiken auf einer Webseite zu zeichnen, und diese Grafiken dann anpassen, indem Sie einfach deren Eigenschaftenattribute ändern.</span><span class="sxs-lookup"><span data-stu-id="5fe81-161">You can use VML to draw graphics on a Web page, and then customize those graphics by simply changing their property attributes.</span></span> <span data-ttu-id="5fe81-162">Außerdem werden die meisten in VML dargestellten Grafiken in Browsern schneller gerendert, und der Download nimmt weniger Zeit und Speicherplatz auf dem Datenträger ein.</span><span class="sxs-lookup"><span data-stu-id="5fe81-162">Also, most graphics represented in VML are rendered faster in browsers, and take less download time and disk space.</span></span>

 

 