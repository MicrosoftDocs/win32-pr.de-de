---
title: Häufig gestellte Fragen zu VML
description: Häufig gestellte Fragen zu VML
ms.assetid: f7f2ce12-facf-4042-b2a7-acaa3e25816a
keywords:
- Vector Markup Language (VML), FAQs
- VML (Vector Markup Language), FAQs
- Vektorgrafiken, FAQs
- Vector Markup Language (VML), häufig gestellte Fragen
- VML (Vector Markup Language), häufig gestellte Fragen
- Vektorgrafiken, häufig gestellte Fragen
- Vector Markup Language (VML), GIF-Unterschiede
- VML (Vector Markup Language), GIF-Unterschiede
- Vector Markup Language (VML), PNG-Unterschiede
- VML (Vector Markup Language), PNG-Unterschiede
- Vektorgrafiken, Unterschiede im Raster Format
- Vector Markup Language (VML), XML
- VML (Vector Markup Language), XML
- Vektorgrafiken, XML
- Vector Markup Language (VML), Animation
- VML (Vector Markup Language), Animation
- Vektorgrafiken, Animation
- Vector Markup Language (VML), Macromedia Flash
- VML (Vector Markup Language), Macromedia Flash
- Vektorgrafiken, Macromedia Flash
- Raster Formate
- Animation
- Macromedia Flash
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e108f2055e7a0fbae1c5ed542fe68c59ec9b212b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948955"
---
# <a name="frequently-asked-questions-about-vml"></a><span data-ttu-id="cd941-126">Häufig gestellte Fragen zu VML</span><span class="sxs-lookup"><span data-stu-id="cd941-126">Frequently Asked Questions About VML</span></span>

<span data-ttu-id="cd941-127">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="cd941-127">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="cd941-128">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="cd941-128">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="cd941-129">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="cd941-129">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="cd941-130">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="cd941-130">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="cd941-131">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="cd941-131">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="cd941-132">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="cd941-132">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

## <a name="does-vml-compete-with-gif-and-png"></a><span data-ttu-id="cd941-133">Konkurriert VML mit GIF und PNG?</span><span class="sxs-lookup"><span data-stu-id="cd941-133">Does VML compete with GIF and PNG?</span></span>

<span data-ttu-id="cd941-134">Nein.</span><span class="sxs-lookup"><span data-stu-id="cd941-134">No.</span></span> <span data-ttu-id="cd941-135">Sowohl GIF als auch PNG sind Raster Formate (oder Bitmapformate), die zum Speichern von Vektorgrafiken verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="cd941-135">Both GIF and PNG are raster (or bit-mapped) formats that can be used to store vector graphics.</span></span> <span data-ttu-id="cd941-136">In den Raster Formaten wird jedes Pixel gespeichert, während Vektorformate wie VML mathematische Beschreibungen oder Gliederungen verwenden, um die Grafiken zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="cd941-136">Raster formats store every pixel, whereas vector formats such as VML use mathematical descriptions or outlines to describe the graphics.</span></span> <span data-ttu-id="cd941-137">Vektorgrafiken, die in einem vektorbasierten Format gespeichert sind, sind kompakter als die in Raster Formaten gespeicherten Vektorgrafiken, was zu schnelleren Downloadzeiten für Webbenutzer führt.</span><span class="sxs-lookup"><span data-stu-id="cd941-137">Vector graphics stored in a vector-based format are more compact than those stored in raster formats, resulting in faster download times for Web users.</span></span>

<span data-ttu-id="cd941-138">Außerdem werden VML-Grafiken Inline an die HTML-Seite übermittelt, anstatt sich auf externe Dateien zu verlassen, wie es bei GIF und PNG heute der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="cd941-138">In addition, VML graphics are delivered inline to the HTML page rather than relying on external files, as is the case with GIF and PNG today.</span></span> <span data-ttu-id="cd941-139">Dadurch können VML-Grafiken skaliert und mit anderen Webseiten Elementen interagieren, wenn die Größe der Seite geändert wird, sodass die Endbenutzer Leistung verbessert wird.</span><span class="sxs-lookup"><span data-stu-id="cd941-139">This allows VML graphics to scale and interact with other Web page elements as the page is resized, thus improving the end-user experience.</span></span>

<span data-ttu-id="cd941-140">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="cd941-140">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="why-is-microsoft-supporting-another-xml-based-standard-when-xml-is-hardly-in-use-and-is-young-enough-as-it-is"></a><span data-ttu-id="cd941-141">Warum unterstützt Microsoft einen anderen XML-basierten Standard, wenn XML kaum verwendet wird und so jung genug ist?</span><span class="sxs-lookup"><span data-stu-id="cd941-141">Why is Microsoft supporting another XML-based standard when XML is hardly in use and is young enough as it is?</span></span>

<span data-ttu-id="cd941-142">XML ist eine leistungsstarke, aber einfache Methode, um strukturierte Daten im Web darzustellen und HTML für die Anzeige vollständig zu ergänzen.</span><span class="sxs-lookup"><span data-stu-id="cd941-142">XML is a powerful yet simple way to represent structured data on the Web, and fully complements HTML for display.</span></span> <span data-ttu-id="cd941-143">VML ist ein Beispiel für die vielen anwendungsspezifischen XML-basierten Formate, die in den kommenden Monaten entwickelt und implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="cd941-143">VML is one example of the many application-specific, XML-based formats that will be developed and implemented in the coming months.</span></span> <span data-ttu-id="cd941-144">Beispielsweise wird in der nächsten Version von Office VML verwendet, um HTML-Dokumente mit Anmerkungen zu versehen, um Formatierungsinformationen von Office-Grafik Grafiken zwischen dem systemeigenen Office-Dateiformat und HTML zu erhalten. so können Office-Benutzer nahtlos zwischen den beiden Formaten wechseln.</span><span class="sxs-lookup"><span data-stu-id="cd941-144">For instance, in the next version of Office, VML will be used to annotate HTML documents -- to preserve formatting information of Office Art graphics between the native Office file format and HTML, thus enabling Office users to switch seamlessly between the two formats.</span></span>

<span data-ttu-id="cd941-145">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="cd941-145">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="who-will-support-vml"></a><span data-ttu-id="cd941-146">Wer wird VML unterstützen?</span><span class="sxs-lookup"><span data-stu-id="cd941-146">Who will support VML?</span></span>

<span data-ttu-id="cd941-147">Wir erwarten, dass viele Lieferanten VML unterstützen.</span><span class="sxs-lookup"><span data-stu-id="cd941-147">We expect many vendors to support VML.</span></span> <span data-ttu-id="cd941-148">Autodesk, Hewlett-Packard, Macromedia und Visio haben beispielsweise in zukünftigen Versionen ihrer Produkte Unterstützung für VML zugesichert.</span><span class="sxs-lookup"><span data-stu-id="cd941-148">For example, Autodesk, Hewlett-Packard, Macromedia, and VISIO have pledged support for VML in future versions of their products.</span></span> <span data-ttu-id="cd941-149">Microsoft hat Unterstützung für VML in zukünftigen Versionen der Plattformen, wie z. b. Internet Explorer, zugesagt.</span><span class="sxs-lookup"><span data-stu-id="cd941-149">Microsoft has pledged support for VML in future versions of its platforms such as Internet Explorer.</span></span> <span data-ttu-id="cd941-150">Außerdem wird VML in der nächsten Generation von Office verwendet, um das "Roundtrip" zwischen dem Office-Format und dem HTML-Code zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="cd941-150">In addition, VML will be used in the next generation of Office to enable "round-tripping" between the Office format and HTML.</span></span>

<span data-ttu-id="cd941-151">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="cd941-151">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="does-vml-support-animation"></a><span data-ttu-id="cd941-152">Wird die Animation von VML unterstützt?</span><span class="sxs-lookup"><span data-stu-id="cd941-152">Does VML support animation?</span></span>

<span data-ttu-id="cd941-153">Nein, dies ist derzeit nicht der Fall.</span><span class="sxs-lookup"><span data-stu-id="cd941-153">No, it currently doesn't.</span></span> <span data-ttu-id="cd941-154">Wir arbeiten jedoch mit unseren VML-Partnern zusammen, um Animations Funktionen im VML-Format hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="cd941-154">However, we are working with our VML partners to add animation capability into the VML format.</span></span> <span data-ttu-id="cd941-155">Da VML auf XML basiert, kann der Tagsatz problemlos erweitert werden, um zusätzliche Funktionen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="cd941-155">Since VML is based on XML, the tag set can be easily extended for additional functionality.</span></span>

<span data-ttu-id="cd941-156">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="cd941-156">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="does-vml-replace-macromedia-flash-didnt-macromedia-just-submit-their-flash-format-for-vector-graphics-to-the-w3c"></a><span data-ttu-id="cd941-157">Ersetzt VML Macromedia Flash?</span><span class="sxs-lookup"><span data-stu-id="cd941-157">Does VML replace Macromedia Flash?</span></span> <span data-ttu-id="cd941-158">Hat Macromedia nicht einfach das Flash-Format für Vektorgrafiken an das W3C gesendet?</span><span class="sxs-lookup"><span data-stu-id="cd941-158">Didn't Macromedia just submit their Flash format for vector graphics to the W3C?</span></span>

<span data-ttu-id="cd941-159">Nein.</span><span class="sxs-lookup"><span data-stu-id="cd941-159">No.</span></span> <span data-ttu-id="cd941-160">VML ist ein textbasiertes Austausch-und Übermittlungs Format für Vektorgrafiken, während Flash ein binäres Format für die Übermittlung von vektorbasierten Grafiken und Animationen ist.</span><span class="sxs-lookup"><span data-stu-id="cd941-160">VML is a text-based interchange and delivery format for vector graphics, whereas Flash is a binary format for the delivery of vector-based graphics and animation.</span></span>

<span data-ttu-id="cd941-161">Macromedia hat das Dateiformat nicht an das W3C übermittelt.</span><span class="sxs-lookup"><span data-stu-id="cd941-161">Macromedia did not submit their file format to the W3C.</span></span> <span data-ttu-id="cd941-162">Allerdings haben Sie das Dateiformat für Anwendungsentwickler, Webentwickler und Endbenutzer geöffnet.</span><span class="sxs-lookup"><span data-stu-id="cd941-162">However, they did open their file format up for application developers, Web developers and end users.</span></span> <span data-ttu-id="cd941-163">Weitere Informationen finden Sie unter <https://www.macromedia.com>.</span><span class="sxs-lookup"><span data-stu-id="cd941-163">See <https://www.macromedia.com> for more information.</span></span>

[<span data-ttu-id="cd941-164">Zurück zur VML-Übersicht</span><span class="sxs-lookup"><span data-stu-id="cd941-164">Back to the VML overview</span></span>](web-workshop---specs---standards----how-to-use-vml-on-web-pages.md)

 

 