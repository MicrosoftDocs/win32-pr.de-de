---
title: Grundlegende VML-Typen
description: In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Migrieren Sie Webseiten und Anwendungen, die auf VML basieren, auf SVG oder andere allgemein unterstützte Standards.
ms.assetid: 07c17e7b-5ac4-4a8d-a468-559307408d5b
keywords:
- Vector Markup Language (VML), Basis Typen
- VML (Vector Markup Language), grundlegende Typen
- Vektorgrafiken, grundlegende VML-Typen
- Vector Markup Language (VML), Typen
- VML (Vector Markup Language), Typen
- Vektorgrafiken, VML-Typen
- grundlegende VML-Typen
- boolescher Typ
- Bruchtyp
- ordinentyp
- length-Typ
- Messtyp
- Angle-Typ
- Farbtyp
- Schrifttyp
- Bitmaptyp
- Vektortyp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f05b058c919496b608b875f96e6c03bbeb0d50e8
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2021
ms.locfileid: "104557494"
---
# <a name="basic-vml-types"></a><span data-ttu-id="17764-121">Grundlegende VML-Typen</span><span class="sxs-lookup"><span data-stu-id="17764-121">Basic VML Types</span></span>

<span data-ttu-id="17764-122">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="17764-122">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="17764-123">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="17764-123">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="17764-124">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="17764-124">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="17764-125">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="17764-125">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="17764-126">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="17764-126">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="17764-127">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="17764-127">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="17764-128">**Contents**</span><span class="sxs-lookup"><span data-stu-id="17764-128">**Contents**</span></span>

-   [<span data-ttu-id="17764-129">Introduction (Einführung)</span><span class="sxs-lookup"><span data-stu-id="17764-129">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="17764-130">boolean</span><span class="sxs-lookup"><span data-stu-id="17764-130">boolean</span></span>](#boolean)
-   [<span data-ttu-id="17764-131">fraction</span><span class="sxs-lookup"><span data-stu-id="17764-131">fraction</span></span>](#fraction)
-   [<span data-ttu-id="17764-132">g</span><span class="sxs-lookup"><span data-stu-id="17764-132">ordinate</span></span>](#ordinate)
-   [<span data-ttu-id="17764-133">length</span><span class="sxs-lookup"><span data-stu-id="17764-133">length</span></span>](#length)
    -   [<span data-ttu-id="17764-134">Alternative Darstellungen</span><span class="sxs-lookup"><span data-stu-id="17764-134">Alternative representations</span></span>](#alternative-representations)
-   [<span data-ttu-id="17764-135">gemessen</span><span class="sxs-lookup"><span data-stu-id="17764-135">measure</span></span>](#measure)
    -   [<span data-ttu-id="17764-136">Alternative Darstellungen</span><span class="sxs-lookup"><span data-stu-id="17764-136">Alternative representations</span></span>](#alternative-representations)
-   [<span data-ttu-id="17764-137">angle</span><span class="sxs-lookup"><span data-stu-id="17764-137">angle</span></span>](#angle)
    -   [<span data-ttu-id="17764-138">Alternative Darstellungen</span><span class="sxs-lookup"><span data-stu-id="17764-138">Alternative representations</span></span>](#alternative-representations)
-   [<span data-ttu-id="17764-139">color</span><span class="sxs-lookup"><span data-stu-id="17764-139">color</span></span>](#color)
    -   [<span data-ttu-id="17764-140">Farbeinheiten</span><span class="sxs-lookup"><span data-stu-id="17764-140">Color units</span></span>](#color-units)
    -   [<span data-ttu-id="17764-141">HTML-Farben</span><span class="sxs-lookup"><span data-stu-id="17764-141">HTML colors</span></span>](#html-colors)
    -   [<span data-ttu-id="17764-142">Schema Farben</span><span class="sxs-lookup"><span data-stu-id="17764-142">Scheme colors</span></span>](#scheme-colors)
    -   [<span data-ttu-id="17764-143">System Farben</span><span class="sxs-lookup"><span data-stu-id="17764-143">System colors</span></span>](#system-colors)
    -   [<span data-ttu-id="17764-144">Reine Farben</span><span class="sxs-lookup"><span data-stu-id="17764-144">Pure colors</span></span>](#pure-colors)
    -   [<span data-ttu-id="17764-145">Farbanpassungen</span><span class="sxs-lookup"><span data-stu-id="17764-145">Color adjustments</span></span>](#color-adjustments)
-   [<span data-ttu-id="17764-146">Raster</span><span class="sxs-lookup"><span data-stu-id="17764-146">font</span></span>](#font)
-   [<span data-ttu-id="17764-147">Bitmap</span><span class="sxs-lookup"><span data-stu-id="17764-147">bitmap</span></span>](#bitmap)
    -   [<span data-ttu-id="17764-148">Bild Dateiformate</span><span class="sxs-lookup"><span data-stu-id="17764-148">Picture file formats</span></span>](#picture-file-formats)
-   [<span data-ttu-id="17764-149">ve</span><span class="sxs-lookup"><span data-stu-id="17764-149">vector</span></span>](#vector)

## <a name="introduction"></a><span data-ttu-id="17764-150">Einführung</span><span class="sxs-lookup"><span data-stu-id="17764-150">Introduction</span></span>

<span data-ttu-id="17764-151">In diesem Vorschlag wird eine kleine Anzahl grundlegender Typen verwendet, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="17764-151">This proposal uses a small number of basic types, listed in the table below.</span></span>



| <span data-ttu-id="17764-152">type</span><span class="sxs-lookup"><span data-stu-id="17764-152">Type</span></span>                  | <span data-ttu-id="17764-153">Element</span><span class="sxs-lookup"><span data-stu-id="17764-153">Element</span></span>           | <span data-ttu-id="17764-154">Grundlegende Darstellung</span><span class="sxs-lookup"><span data-stu-id="17764-154">Fundamental Representation</span></span> | <span data-ttu-id="17764-155">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="17764-155">Description</span></span>                                                                                          |
|-----------------------|-------------------|----------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="17764-156">boolean</span><span class="sxs-lookup"><span data-stu-id="17764-156">boolean</span></span>](#boolean)   |                   | <span data-ttu-id="17764-157">1 Bit</span><span class="sxs-lookup"><span data-stu-id="17764-157">1 bit</span></span>                      | <span data-ttu-id="17764-158">Ein boolescher Wert: true oder false.</span><span class="sxs-lookup"><span data-stu-id="17764-158">A boolean value: true or false.</span></span>                                                                      |
| [<span data-ttu-id="17764-159">fraction</span><span class="sxs-lookup"><span data-stu-id="17764-159">fraction</span></span>](#fraction) |                   | <span data-ttu-id="17764-160">Nummer 2 6</span><span class="sxs-lookup"><span data-stu-id="17764-160">number 2 6</span></span>                 | <span data-ttu-id="17764-161">Ein numerischer Wert, der um 2 6 (65536) skaliert und als ganze Zahl mit Vorzeichen gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="17764-161">A numeric value, scaled by 2 6 (65536) and stored as a signed integer.</span></span>                               |
| [<span data-ttu-id="17764-162">g</span><span class="sxs-lookup"><span data-stu-id="17764-162">ordinate</span></span>](#ordinate) |                   | <span data-ttu-id="17764-163">30-Bit-Ganzzahl Plus Vorzeichen</span><span class="sxs-lookup"><span data-stu-id="17764-163">30-bit integer plus sign</span></span>   | <span data-ttu-id="17764-164">Teil einer Koordinate (z. b. in einem Pfad), die durch den Koord definierten Werte.</span><span class="sxs-lookup"><span data-stu-id="17764-164">Part of a coordinate (e.g., in a path ), the values defined by coord.</span></span>                                |
| [<span data-ttu-id="17764-165">length</span><span class="sxs-lookup"><span data-stu-id="17764-165">length</span></span>](#length)     |                   | [<span data-ttu-id="17764-166">Emu</span><span class="sxs-lookup"><span data-stu-id="17764-166">EMU</span></span>](#length)             | <span data-ttu-id="17764-167">Eine physische Länge, z. b. die Breite einer Zeile oder die Größe einer Schriftart.</span><span class="sxs-lookup"><span data-stu-id="17764-167">A physical length, such as the width of a line or the size of a font.</span></span>                                |
| [<span data-ttu-id="17764-168">gemessen</span><span class="sxs-lookup"><span data-stu-id="17764-168">measure</span></span>](#measure)   |                   | <span data-ttu-id="17764-169">EWU oder Nummer 2 6</span><span class="sxs-lookup"><span data-stu-id="17764-169">EMU or number 2 6</span></span>          | <span data-ttu-id="17764-170">Entweder eine physische Länge, einschließlich einer Anzahl von Geräte Pixeln, oder ein Bruchteil einer anderen Menge.</span><span class="sxs-lookup"><span data-stu-id="17764-170">Either a physical length, including a number of device pixels, or a fraction of some other quantity.</span></span> |
| [<span data-ttu-id="17764-171">angle</span><span class="sxs-lookup"><span data-stu-id="17764-171">angle</span></span>](#angle)       |                   | <span data-ttu-id="17764-172">Grad 2 6</span><span class="sxs-lookup"><span data-stu-id="17764-172">degrees 2 6</span></span>                | <span data-ttu-id="17764-173">Ein Winkel. positiv ist der Uhrzeigersinn.</span><span class="sxs-lookup"><span data-stu-id="17764-173">An angle; positive is clockwise.</span></span>                                                                     |
| [<span data-ttu-id="17764-174">color</span><span class="sxs-lookup"><span data-stu-id="17764-174">color</span></span>](#color)       | [<span data-ttu-id="17764-175">c</span><span class="sxs-lookup"><span data-stu-id="17764-175">c</span></span>](#color)       | <span data-ttu-id="17764-176">complex</span><span class="sxs-lookup"><span data-stu-id="17764-176">complex</span></span>                    | <span data-ttu-id="17764-177">Ein Element, mit dem eine Farbe abgeleitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="17764-177">An element that allows a color to be derived.</span></span>                                                        |
| [<span data-ttu-id="17764-178">Raster</span><span class="sxs-lookup"><span data-stu-id="17764-178">font</span></span>](#font)         | [<span data-ttu-id="17764-179">Raster</span><span class="sxs-lookup"><span data-stu-id="17764-179">font</span></span>](#font)     | <span data-ttu-id="17764-180">complex</span><span class="sxs-lookup"><span data-stu-id="17764-180">complex</span></span>                    | <span data-ttu-id="17764-181">Eine Beschreibung einer Schriftart.</span><span class="sxs-lookup"><span data-stu-id="17764-181">A description of a font.</span></span>                                                                             |
| [<span data-ttu-id="17764-182">Bitmap</span><span class="sxs-lookup"><span data-stu-id="17764-182">bitmap</span></span>](#bitmap)     | [<span data-ttu-id="17764-183">Bitmap</span><span class="sxs-lookup"><span data-stu-id="17764-183">bitmap</span></span>](#bitmap) | <span data-ttu-id="17764-184">href</span><span class="sxs-lookup"><span data-stu-id="17764-184">href</span></span>                       | <span data-ttu-id="17764-185">Ein Verweis auf eine externe Bilddatei.</span><span class="sxs-lookup"><span data-stu-id="17764-185">A reference to an external picture file.</span></span>                                                             |
| [<span data-ttu-id="17764-186">ve</span><span class="sxs-lookup"><span data-stu-id="17764-186">vector</span></span>](#vector)     | [<span data-ttu-id="17764-187">Ramelow</span><span class="sxs-lookup"><span data-stu-id="17764-187">v</span></span>](#vector)      | <span data-ttu-id="17764-188">complex</span><span class="sxs-lookup"><span data-stu-id="17764-188">complex</span></span>                    | <span data-ttu-id="17764-189">Eine Beschreibung eines Vektor Pfads.</span><span class="sxs-lookup"><span data-stu-id="17764-189">A description of a vector path</span></span>                                                                       |



 

<span data-ttu-id="17764-190">Die "grundlegende Darstellung" ist die höchste Genauigkeits Darstellung, die für den Vorschlag eine konforme Implementierung erfordert. Daten gehen verloren, wenn die-Implementierung nicht in der Lage ist, die Daten für die erforderliche Genauigkeit darzustellen.</span><span class="sxs-lookup"><span data-stu-id="17764-190">The "fundamental representation" is the highest precision representation that the proposal requires a conforming implementation to maintain; data will be lost if the implementation is not able to represent the data to the precision required.</span></span> <span data-ttu-id="17764-191">Die Farb-, Schriftart-und Vektor Typen entsprechen Elementen, die selbst über eine Struktur verfügen. in gewisser Hinsicht sind Sie keine grundlegenden Typen. Es ist jedoch praktisch, Sie in diesem Vorschlag als solche zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="17764-191">The color, font, and vector types correspond to elements which themselves have structure -- in a sense, they are not basic types; however, it is convenient to treat them as such within this proposal.</span></span>

<span data-ttu-id="17764-192">Jedem nicht komplexen Basistyp ist ein Element mit demselben Namen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="17764-192">Each non-complex basic type has an associated element of the same name.</span></span> <span data-ttu-id="17764-193">Diese Elementnamen sind reserviert und können nicht für andere Zwecke innerhalb von Erweiterungen verwendet werden, auch wenn die Verwendung in einem onview = "Skip"-Erweiterungs Element erfolgt.</span><span class="sxs-lookup"><span data-stu-id="17764-193">These element names are reserved and may not be used for any other purpose within extensions, even if the use is within an onview="skip" extension element.</span></span> <span data-ttu-id="17764-194">Aus diesem Grund ist es möglich, dass eine Implementierung, bei der Unbekannter XML-Code gefunden wird, eine effiziente interne Speicherung des unbekannten XML-Codes ermöglicht, solange die Werte in die "Type"-Elemente eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="17764-194">Because of this, it is possible for an implementation that encounters unknown XML to provide efficient internal storage of the unknown XML as long as the values are enclosed in the "type" elements.</span></span>


```HTML
<new:tag>1.578</new:tag>
<new:tag><v:fraction>1.578</v:fraction></new:tag>
```



<span data-ttu-id="17764-195">Im ersten vorangehenden Beispiel muss die Zeichenfolge "1,578" als Sequenz von Zeichen gespeichert werden (die-Implementierung weiß nicht, ob es sich um eine Zeichenfolge oder eine Zahl handelt); im zweiten Beispiel gibt das Bruch Element an, dass der Inhalt eine Zahl ist, sodass es in die Bruchteil-Darstellung mit hoher Genauigkeit konvertiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="17764-195">In the first example above, the string "1.578" must be stored as a sequence of characters (the implementation does not know whether it is a string or a number); in the second example, the fraction element indicates that the content is a number, thus it may be converted to the high precision fraction representation.</span></span>

<span data-ttu-id="17764-196">Komplexe Typen (einschließlich Bitmap) weisen verknüpfte Elementnamen auf, die zum Begrenzen des Werts verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="17764-196">Complex types (including bitmap) have associated element names that are used to delimit the value.</span></span> <span data-ttu-id="17764-197">Dies vereinfacht die-Verarbeitung, indem sichergestellt wird, dass die komplexeren-Element Tags mit eindeutigen Element Tags verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="17764-197">This simplifies parsing by ensuring that the more complex parsing tasks are associated with unique element tags.</span></span>

<span data-ttu-id="17764-198">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="17764-198">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="boolean"></a><span data-ttu-id="17764-199">boolean</span><span class="sxs-lookup"><span data-stu-id="17764-199">boolean</span></span>


```HTML
boolean
<!entity % boolean "#pcdata" -- or nmtoken in an attribute -- >
```



<span data-ttu-id="17764-200">Ein boolescher Wert wird als Schlüsselwort dargestellt, das den Zustand des Flags angibt.</span><span class="sxs-lookup"><span data-stu-id="17764-200">A boolean value is represented as a keyword indicating the state of the flag.</span></span> <span data-ttu-id="17764-201">Die folgenden Schlüsselwörter sind definiert.</span><span class="sxs-lookup"><span data-stu-id="17764-201">The following keywords are defined.</span></span>



| <span data-ttu-id="17764-202">Wert für true</span><span class="sxs-lookup"><span data-stu-id="17764-202">Value for true</span></span> | <span data-ttu-id="17764-203">Wert für false</span><span class="sxs-lookup"><span data-stu-id="17764-203">Value for false</span></span> |
|----------------|-----------------|
| <span data-ttu-id="17764-204">true</span><span class="sxs-lookup"><span data-stu-id="17764-204">true</span></span>           | <span data-ttu-id="17764-205">false</span><span class="sxs-lookup"><span data-stu-id="17764-205">false</span></span>           |
| <span data-ttu-id="17764-206">ja</span><span class="sxs-lookup"><span data-stu-id="17764-206">yes</span></span>            | <span data-ttu-id="17764-207">nein</span><span class="sxs-lookup"><span data-stu-id="17764-207">no</span></span>              |
| <span data-ttu-id="17764-208">on</span><span class="sxs-lookup"><span data-stu-id="17764-208">on</span></span>             | <span data-ttu-id="17764-209">aus</span><span class="sxs-lookup"><span data-stu-id="17764-209">off</span></span>             |
| <span data-ttu-id="17764-210">t</span><span class="sxs-lookup"><span data-stu-id="17764-210">t</span></span>              | <span data-ttu-id="17764-211">f</span><span class="sxs-lookup"><span data-stu-id="17764-211">f</span></span>               |
| <span data-ttu-id="17764-212">1</span><span class="sxs-lookup"><span data-stu-id="17764-212">1</span></span>              | <span data-ttu-id="17764-213">0</span><span class="sxs-lookup"><span data-stu-id="17764-213">0</span></span>               |



 

<span data-ttu-id="17764-214">Eine-Implementierung kann einen beliebigen Wert schreiben und alle Werte erkennen.</span><span class="sxs-lookup"><span data-stu-id="17764-214">An implementation may write any value and must recognize all values.</span></span> <span data-ttu-id="17764-215">Eine-Implementierung ist kostenlos, um Werte von einer Darstellung in eine andere zu ändern.</span><span class="sxs-lookup"><span data-stu-id="17764-215">An implementation is free to change values from one representation to another.</span></span>

<span data-ttu-id="17764-216">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="17764-216">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="fraction"></a><span data-ttu-id="17764-217">fraction</span><span class="sxs-lookup"><span data-stu-id="17764-217">fraction</span></span>


```HTML
fraction
<!entity % fraction "#pcdata" -- or nmtoken in an attribute -- >
```



<span data-ttu-id="17764-218">Alle numerischen Werte (d. h. Werte der dimensionlosen Mengen) in diesem Vorschlag können als ganze Zahlen gespeichert werden, indem Sie um 2 6 (65536) skaliert werden.</span><span class="sxs-lookup"><span data-stu-id="17764-218">All numeric values (i.e., values of dimensionless quantities) within this proposal can be stored as integers by scaling them by 2  6 (65536).</span></span> <span data-ttu-id="17764-219">Eine Zahl kann entweder in diesem Formular mit dem Suffix f oder als Dezimalzahl ohne Suffix angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="17764-219">A number may be given either in this form, with the suffix f or as a decimal number with no suffix.</span></span> <span data-ttu-id="17764-220">Folglich stellen die folgenden hypothetischen Elemente denselben Wert dar.</span><span class="sxs-lookup"><span data-stu-id="17764-220">Thus, the following hypothetical elements represent the same value.</span></span>


```HTML
<fillwidth>0.25</fillwidth>
<fillwidth>16384f</fillwidth>
```



<span data-ttu-id="17764-221">Eine Menge mit dem f-Suffix muss eine ganze Zahl sein. Bruchzahlen sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="17764-221">A quantity with the f suffix must be a whole number; fractional numbers are not permitted.</span></span> <span data-ttu-id="17764-222">Die resultierende Ganzzahl muss als Komplement-signierte Zahl von 32 Bit 2 dargestellt werden. Folglich ist der Gültigkeitsbereich der Darstellung 32768 (tatsächlich kleiner als 32768 und größer oder gleich-32768).</span><span class="sxs-lookup"><span data-stu-id="17764-222">The resultant integer must be representable as a 32-bit 2's complement signed number; thus, the effective range of the representation is  32768 (in fact, less than 32768 and greater than or equal to -32768.)</span></span>

<span data-ttu-id="17764-223">Eine konforme Implementierung ist erforderlich, um Werte beizubehalten, die als f-Werte ausgedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="17764-223">A conforming implementation is required to preserve values that are expressed as f values.</span></span> <span data-ttu-id="17764-224">Werte, die als Dezimalzahlen dargestellt werden, können in einen f-Wert konvertiert und auf diese Weise gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="17764-224">Values represented as decimal numbers may be converted to an f value and stored that way.</span></span> <span data-ttu-id="17764-225">Eine Anwendung ist berechtigt, intern generierte Werte in einer beliebigen entsprechenden Einheit aufzuzeichnen. ein Wert, der aus einem vorhandenen Dokument gelesen wird, muss jedoch entweder in der vollständigen ursprünglichen Genauigkeit beibehalten werden oder in einen f-Wert konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="17764-225">An application is permitted to record internally generated values in any appropriate unit; however, a value read in from an existing document must either be maintained to the full original precision or must be converted into an f value.</span></span>

<span data-ttu-id="17764-226">Wenn die Implementierung dies nicht tun kann, muss Sie den Benutzer warnen, dass Daten verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="17764-226">If the implementation is unable to do this, it must warn the user that data may be lost.</span></span> <span data-ttu-id="17764-227">(Es ist zulässig, eine solche Warnung einmalig auszugeben, wenn extern generierte Daten zum ersten Mal gefunden werden.)</span><span class="sxs-lookup"><span data-stu-id="17764-227">(It is acceptable to issue such a warning once when externally generated data is first encountered.)</span></span>

<span data-ttu-id="17764-228">Wenn ein Dezimalwert in das f-Format konvertiert wird, kann die Implementierung einen beliebigen arithmetischen Rundungs Modus verwenden. Allerdings muss eine ganze Zahl genau in das f-Format konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="17764-228">When a decimal value is converted into f format, the implementation may use any arithmetic rounding mode; however, a whole number must be converted to the f format exactly.</span></span> <span data-ttu-id="17764-229">Es wird empfohlen, dass Implementierungen durch Runden auf minus unendlich konvertiert werden und dass die konvertion immer exakt ist.</span><span class="sxs-lookup"><span data-stu-id="17764-229">It is recommended that implementations convert by rounding to minus infinity and that the convertion always be exact.</span></span>

<span data-ttu-id="17764-230">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="17764-230">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="ordinate"></a><span data-ttu-id="17764-231">g</span><span class="sxs-lookup"><span data-stu-id="17764-231">ordinate</span></span>


```HTML
ordinate
<!entity % ordinate "#pcdata" -- or nmtoken in an attribute -- >
```



<span data-ttu-id="17764-232">Die Einheiten des Koordinatensystems, das durch den Koord festgelegt wird, haben einen nominalen Typ, der als "Ordini" bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="17764-232">The units of the coordinate system established by coord are of some nominal type, which is referred to as ordinate.</span></span> <span data-ttu-id="17764-233">Dies ist ein Measure der Länge, wird jedoch nur in Bezug auf das Rechteck verwendet, das von coord festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="17764-233">This is a measure of length, but it is only used in relation to the rectangle that coord establishes.</span></span> <span data-ttu-id="17764-234">Jeder Wert des Typs "Ordinalwert" wird durch die Werte " *w* " und " *h* " des Koord und das resultierende Verhältnis skaliert, das verwendet wird, um eine tatsächliche Messung auf dem Ausgabegerät herzustellen.</span><span class="sxs-lookup"><span data-stu-id="17764-234">Any value of type ordinate will be scaled by the *w* and *h* values of the coord and the resulting ratio used to establish a real measurement on the output device.</span></span>

<span data-ttu-id="17764-235">Eine konforme Implementierung muss in der Lage sein, Ordinalwerte von bis zu 30 Bits Pluszeichen (d. h. eine 31-Bit-Ganzzahl mit Vorzeichen, keine 32-Bit-Ganzzahl mit Vorzeichen) zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="17764-235">A conforming implementation must be able to handle ordinate values of up to 30 bits plus sign (i.e., a 31-bit signed integer, not a 32-bit signed integer).</span></span> <span data-ttu-id="17764-236">Es wird jedoch empfohlen, dass Implementierungen versuchen, Koordinaten für path-und ähnliche Elemente zu entwickeln, die ungefähr 16 Bits Genauigkeit aufweisen.</span><span class="sxs-lookup"><span data-stu-id="17764-236">It is recommended, however, that implementations attempt to produce coordinates for path and similar elements that have about 16 bits of precision.</span></span> <span data-ttu-id="17764-237">Dadurch wird die Wahrscheinlichkeit eines Unterlaufs oder eines Überlaufs in einer nicht konformen Implementierung minimiert.</span><span class="sxs-lookup"><span data-stu-id="17764-237">This will minimize the chance of either underflow or overflow in a non-conforming implementation.</span></span>

<span data-ttu-id="17764-238">Ordinalwerte sind immer ganzzahlige Werte.</span><span class="sxs-lookup"><span data-stu-id="17764-238">ordinate values are always integral.</span></span> <span data-ttu-id="17764-239">Ein Dezimaltrennzeichen darf nicht in einem Wert vom Typ "ordinalpunkt" vorkommen.</span><span class="sxs-lookup"><span data-stu-id="17764-239">A decimal point may not appear in a value of type ordinate.</span></span> <span data-ttu-id="17764-240">An Werte vom Typ "Ordini" können keine Einheits spezifiatoren angehängt werden.</span><span class="sxs-lookup"><span data-stu-id="17764-240">No unit specifiers may be appended to values of type ordinate.</span></span>

<span data-ttu-id="17764-241">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="17764-241">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="length"></a><span data-ttu-id="17764-242">length</span><span class="sxs-lookup"><span data-stu-id="17764-242">length</span></span>


```HTML
length
<!entity % length "#pcdata" -- or nmtoken in an attribute -- >
```



<span data-ttu-id="17764-243">Eine Länge ist eine reale Messung oder manchmal eine Messung in Geräte Pixeln.</span><span class="sxs-lookup"><span data-stu-id="17764-243">A length is a real-world measurement or, sometimes, a measurement in device pixels.</span></span> <span data-ttu-id="17764-244">Es wird empfohlen, dass-Implementierungen die Verwendung von Geräte Pixeln (px) vermeiden.</span><span class="sxs-lookup"><span data-stu-id="17764-244">It is recommended that implementations avoid the use of device pixels (px).</span></span>

<span data-ttu-id="17764-245">Alle Standard Qualifizierer für [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1) -Einheiten sind für eine Länge zulässig.</span><span class="sxs-lookup"><span data-stu-id="17764-245">All the standard [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1) unit qualifiers are permitted on a length.</span></span> <span data-ttu-id="17764-246">Außerdem kann die Qualifizierer-Emu verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="17764-246">In addition, the qualifier emu may be used.</span></span> <span data-ttu-id="17764-247">Dieser Qualifizierer bezieht sich auf eine Einheit, d. h. auf die EWU (englische Metrik Unit). Hierbei handelt es sich um einen gemeinsamen Nenner der Mess Mengen in den Computergrafiken.</span><span class="sxs-lookup"><span data-stu-id="17764-247">This qualifier refers to a unit -- the EMU (English Metric Unit) -- which is a common denominator of the measurement quantities in widespread use in computer graphics.</span></span> <span data-ttu-id="17764-248">Der EMU ist <sup>Zoll</sup> /914400, d. h., es gibt 914400 Emu pro Zoll.</span><span class="sxs-lookup"><span data-stu-id="17764-248">The EMU is <sup>inch</sup> / 914400, i.e., there are 914400 EMU per inch.</span></span> <span data-ttu-id="17764-249">In der folgenden Tabelle ist die Anzahl der Emus in einer kleinen Anzahl von häufig auftretenden Einheiten aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="17764-249">The following table lists the number of EMUs in a small number of commonly encountered units.</span></span>



| <span data-ttu-id="17764-250">Anzahl von Emus</span><span class="sxs-lookup"><span data-stu-id="17764-250">Number of EMUs</span></span> | <span data-ttu-id="17764-251">Anzahl pro Zoll</span><span class="sxs-lookup"><span data-stu-id="17764-251">Number per Inch</span></span> | <span data-ttu-id="17764-252">Anzahl pro Millimeter</span><span class="sxs-lookup"><span data-stu-id="17764-252">Number per Millimeter</span></span> | <span data-ttu-id="17764-253">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="17764-253">Description</span></span>             |
|----------------|-----------------|-----------------------|-------------------------|
| <span data-ttu-id="17764-254">360</span><span class="sxs-lookup"><span data-stu-id="17764-254">360</span></span>            |                 | <span data-ttu-id="17764-255">0,01</span><span class="sxs-lookup"><span data-stu-id="17764-255">0.01</span></span>                  | <span data-ttu-id="17764-256">Win32-HIMETRIC</span><span class="sxs-lookup"><span data-stu-id="17764-256">Win32 HIMETRIC</span></span>          |
| <span data-ttu-id="17764-257">12700</span><span class="sxs-lookup"><span data-stu-id="17764-257">12700</span></span>          | <span data-ttu-id="17764-258">72</span><span class="sxs-lookup"><span data-stu-id="17764-258">72</span></span>              |                       | <span data-ttu-id="17764-259">Punkt</span><span class="sxs-lookup"><span data-stu-id="17764-259">"point"</span></span>                 |
| <span data-ttu-id="17764-260">635</span><span class="sxs-lookup"><span data-stu-id="17764-260">635</span></span>            | <span data-ttu-id="17764-261">1440</span><span class="sxs-lookup"><span data-stu-id="17764-261">1440</span></span>            |                       | <span data-ttu-id="17764-262">Win32-Twip</span><span class="sxs-lookup"><span data-stu-id="17764-262">Win32 TWIP</span></span>              |
| <span data-ttu-id="17764-263">762</span><span class="sxs-lookup"><span data-stu-id="17764-263">762</span></span>            | <span data-ttu-id="17764-264">1200</span><span class="sxs-lookup"><span data-stu-id="17764-264">1200</span></span>            |                       | <span data-ttu-id="17764-265">Drucker mit hoher Auflösung</span><span class="sxs-lookup"><span data-stu-id="17764-265">High-resolution printer</span></span> |



 

<span data-ttu-id="17764-266">Bruchzahlen von Emus sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="17764-266">Fractional numbers of EMUs are not permitted.</span></span> <span data-ttu-id="17764-267">Jede Messung muss als eine ganzzahlige 32-Bit-Zahl von Emus dargestellt werden. Dadurch wird die Größe eines Mess Werts auf 2348 Zoll--ungefähr 59 Meter oder 65 Meter beschränkt.</span><span class="sxs-lookup"><span data-stu-id="17764-267">Any measurement must be representable as a 32-bit signed integral number of EMUs -- this limits the magnitude of a measurement to 2348 inches -- about 59 meters or 65 yards.</span></span> <span data-ttu-id="17764-268">Da die Messungen immer auf die Größe eines Renderings auf einem nominell Bildschirm-oder Seitengröße-Ausgabegerät verweisen, liegen Sie immer innerhalb dieses Bereichs.</span><span class="sxs-lookup"><span data-stu-id="17764-268">Because the measurements always refer to the size of a rendering on a nominally screen- or page-sized output device, they will always be within this range.</span></span>

<span data-ttu-id="17764-269">Beachten Sie jedoch, dass die Darstellung für reale Messungen ungeeignet ist und dass Sie aufgezeichnet werden (z. b. zum Aufzeichnen der realen Größe eines Pfades), dass eine andere Darstellung verwendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="17764-269">Notice, however, that the representation is inappropriate for real-world measurements and that where these are recorded (for example, to record the real-world size of a path) some other representation must be used.</span></span>

<span data-ttu-id="17764-270">Eine konforme Implementierung ist erforderlich, um Werte beizubehalten, die genaue Anzahl von Emus sind.</span><span class="sxs-lookup"><span data-stu-id="17764-270">A conforming implementation is required to preserve values that are exact numbers of EMUs.</span></span> <span data-ttu-id="17764-271">Werte, die auf andere Weise dargestellt werden, können in einen Emu-Wert konvertiert und auf diese Weise gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="17764-271">Values represented in any other way may be converted to an EMU value and stored that way.</span></span> <span data-ttu-id="17764-272">Eine Anwendung ist berechtigt, intern generierte Werte in einer beliebigen entsprechenden Einheit aufzuzeichnen. ein Wert, der aus einem vorhandenen Dokument gelesen wird, muss jedoch entweder in der vollständigen ursprünglichen Genauigkeit beibehalten werden oder in einen Emu-Wert konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="17764-272">An application is permitted to record internally generated values in any appropriate unit; however, a value read in from an existing document must either be maintained to the full original precision or must be converted into an EMU value.</span></span>

<span data-ttu-id="17764-273">Wenn die Implementierung dies nicht tun kann, muss Sie den Benutzer warnen, dass Daten verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="17764-273">If the implementation is unable to do this, it must warn the user that data may be lost.</span></span> <span data-ttu-id="17764-274">(Es ist zulässig, eine solche Warnung einmalig auszugeben, wenn extern generierte Daten zum ersten Mal gefunden werden.)</span><span class="sxs-lookup"><span data-stu-id="17764-274">(It is acceptable to issue such a warning once when externally generated data is first encountered.)</span></span>

<span data-ttu-id="17764-275">In der Praxis werden für relativ wenige Messungen in diesem Vorschlag physische Längen verwendet.</span><span class="sxs-lookup"><span data-stu-id="17764-275">In practice, physical lengths are used for relatively few measurements in this proposal.</span></span> <span data-ttu-id="17764-276">Bei den Daten, die normalerweise am wichtigsten sind, handelt es sich um die Pfaddaten, die in dem Koordinatensystem codiert sind, das auf der Grundlage der Form von coord definiert ist.</span><span class="sxs-lookup"><span data-stu-id="17764-276">The data which is normally most important is the path data and this is encoded in the coordinate system defined, on a per-shape basis, by coord.</span></span>

### <a name="alternative-representations"></a><span data-ttu-id="17764-277">Alternative Darstellungen</span><span class="sxs-lookup"><span data-stu-id="17764-277">Alternative representations</span></span>

<span data-ttu-id="17764-278">Die Standardlängen Darstellungen von HTML werden durch [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#length-units) definiert.</span><span class="sxs-lookup"><span data-stu-id="17764-278">The standard length representations of HTML are defined by [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#length-units) .</span></span> <span data-ttu-id="17764-279">Relative Einheiten, mit Ausnahme des Pixels, sind in dem Kontext, in dem Längen in diesem Vorschlag verwendet werden, nicht aussagekräftig und dürfen nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="17764-279">Relative units, with the exception of the pixel, are not meaningful in the context within which lengths are used in this proposal and must not be used.</span></span> <span data-ttu-id="17764-280">Wenn das Dokument die beabsichtigte (Ziel-) Pixelgröße aufzeichnet, wird die Übersetzung von Pixel in EMU definiert. Andernfalls sollte der von [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#length-units) definierte Standardwert 90 dpi verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="17764-280">If the document records the intended (target) pixel size, this defines the translation of pixels into EMU; otherwise, the default of 90 dpi defined by [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#length-units) should be used.</span></span>

<span data-ttu-id="17764-281">Mit Ausnahme von "EMU" kann jeder Wert als Dezimal Bruch angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="17764-281">With the exception of emu, any value may be given as a decimal fraction.</span></span> <span data-ttu-id="17764-282">Wenn ein Dezimalwert in den Emu-Wert konvertiert wird, kann die Implementierung einen beliebigen arithmetischen Rundungs Modus verwenden.</span><span class="sxs-lookup"><span data-stu-id="17764-282">When a decimal value is converted to EMU, the implementation may use any arithmetic rounding mode.</span></span> <span data-ttu-id="17764-283">(Die einzige Möglichkeit für eine Erstellungs Anwendung, ein bestimmtes Ergebnis zu gewährleisten, besteht darin, Sie in der EWU anzugeben.)</span><span class="sxs-lookup"><span data-stu-id="17764-283">(The only way for an authoring application to guarantee a particular result is to specify it in emu.)</span></span>

<span data-ttu-id="17764-284">Wenn kein Einheits Spezifizierer in einem Längen Wert angegeben wird, muss die Implementierung die EWU annehmen.</span><span class="sxs-lookup"><span data-stu-id="17764-284">If no unit specifier is given in a length value, the implementation must assume emu.</span></span>

<span data-ttu-id="17764-285">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="17764-285">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="measure"></a><span data-ttu-id="17764-286">Kennzahl</span><span class="sxs-lookup"><span data-stu-id="17764-286">measure</span></span>


```HTML
measure
<!entity % measure "#pcdata" -- or nmtoken in an attribute -- >
```



<span data-ttu-id="17764-287">Ein Measure ist eine Menge, die entweder eine [Länge](#length) oder ein [Bruchteil](#fraction)aufweisen kann.</span><span class="sxs-lookup"><span data-stu-id="17764-287">A measure is a quantity that may be either a [length](#length) or a [fraction](#fraction).</span></span> <span data-ttu-id="17764-288">Dies ähnelt den HTML-und CSS-Längenmessungen, bei denen es sich in vielen Fällen entweder um physische Messungen oder Prozentsätze einer anderen Menge handeln kann.</span><span class="sxs-lookup"><span data-stu-id="17764-288">This closely resembles the HTML and CSS length measurements, which can, in many cases, either be physical measurements or percentages of some other quantity.</span></span> <span data-ttu-id="17764-289">Wenn kein Einheits Spezifizierer angegeben wird, muss der Wert als Dezimal Bruch angenommen werden (daher wird dieses Verhalten vom Bruchteil geerbt, nicht von der Länge).</span><span class="sxs-lookup"><span data-stu-id="17764-289">If no unit specifier is given, the value must be assumed to be a decimal fraction (thus, this behavior is inherited from fraction, not from length.)</span></span>

<span data-ttu-id="17764-290">Anders als bei der Länge hat ein Pixelwert eine Kontext definierte Bedeutung, sodass die Konvertierung in die EWU normalerweise ungeeignet ist.</span><span class="sxs-lookup"><span data-stu-id="17764-290">Unlike length, a pixel value has a context-defined meaning, so conversion to emu is normally inappropriate.</span></span> <span data-ttu-id="17764-291">Es gibt drei mögliche grundlegende Darstellungen, die die Implementierung beibehalten muss (d. h., eine Darstellung kann ohne Informationsverlust nicht in eine andere konvertiert werden).</span><span class="sxs-lookup"><span data-stu-id="17764-291">There are three possible fundamental representations that the implementation must maintain (i.e., one representation cannot be converted into another without loss of information).</span></span>

1.  <span data-ttu-id="17764-292">Ein Bruchteil muss im [Bruchteil](#fraction) -Format (einem "f"-Wert) beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="17764-292">A fractional value should be maintained in the [fraction](#fraction) format (an " f " value).</span></span>
2.  <span data-ttu-id="17764-293">Eine physische Länge sollte in der EWU beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="17764-293">A physical length should be maintained in EMU.</span></span>
3.  <span data-ttu-id="17764-294">Ein Pixelwert sollte als ganze Anzahl von Pixeln beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="17764-294">A pixel value should be maintained as a whole number of pixels.</span></span>

<span data-ttu-id="17764-295">Bruchzahlen von Pixeln sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="17764-295">Fractional numbers of pixels are not permitted.</span></span>

### <a name="alternative-representations"></a><span data-ttu-id="17764-296">Alternative Darstellungen</span><span class="sxs-lookup"><span data-stu-id="17764-296">Alternative representations</span></span>

<span data-ttu-id="17764-297">Alle alternativen Darstellungen von [Bruchteil](#fraction) und [Länge](#length) sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="17764-297">All the alternate representations of both [fraction](#fraction) and [length](#length) are permitted.</span></span>

<span data-ttu-id="17764-298">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="17764-298">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="angle"></a><span data-ttu-id="17764-299">angle</span><span class="sxs-lookup"><span data-stu-id="17764-299">angle</span></span>


```HTML
angle
<!entity % angle "#pcdata" -- or nmtoken in an attribute -- >
```



<span data-ttu-id="17764-300">Die grundlegende Darstellung eines Winkels ist eine Anzahl von Grad, der um 2 6 (65536) multiheftet und als ganze Zahl gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="17764-300">The fundamental representation of an angle is a number of degrees multipled by 2 6 (65536) and stored as an integer.</span></span> <span data-ttu-id="17764-301">Da der Koordinatenraum invertiert wird (positive y-Achse ist nicht mehr), ist ein Winkel im Uhrzeigersinn positiv.</span><span class="sxs-lookup"><span data-stu-id="17764-301">Because the coordinate space is inverted (positive y axis is down), a clockwise angle is positive.</span></span> <span data-ttu-id="17764-302">Eine konforme Implementierung ist erforderlich, um die vollständige Genauigkeit eines solchen Werts beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="17764-302">A conforming implementation is required to preserve the full precision of such a value.</span></span>

<span data-ttu-id="17764-303">Eine Implementierung darf einen beliebigen Bereich für Winkel verwenden und einen Winkel normalisieren (z. b. auf-180 bis + 180 oder 0 bis 360).</span><span class="sxs-lookup"><span data-stu-id="17764-303">An implementation is permitted to use any range for angles and is permitted to normalise an angle (for example to -180  to +180  or 0 to 360 ).</span></span> <span data-ttu-id="17764-304">Implementierungen müssen nicht konsistent sein. die ganzzahlige Darstellung eines Winkels darf den Bereich einer 32-Bit-Ganzzahl mit Vorzeichen jedoch nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="17764-304">Implementations are not required to be consistent; however, the integral representation of an angle must not exceed the range of a 32-bit signed integer.</span></span>

<span data-ttu-id="17764-305">Das Suffix FD wird verwendet, um diese Darstellung eines Winkels (Bruch Komma) zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="17764-305">The suffix fd is used to identify this representation of an angle (fractional degree).</span></span> <span data-ttu-id="17764-306">Beachten Sie, dass dies vom f-Suffix für einen dimensionlosen Bruchteil unterschieden wird, obwohl identische Arithmetik zur Unterstützung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="17764-306">Notice that this is distinguished from the f suffix for a dimensionless fraction although identical arithmetic can be used to support it.</span></span> <span data-ttu-id="17764-307">Der Standardwert für einen Angular-Wert ist einfache Grad, d. h. ein nicht skalierter Wert.</span><span class="sxs-lookup"><span data-stu-id="17764-307">The default for an angular value is simple degrees, i.e., an unscaled value.</span></span> <span data-ttu-id="17764-308">Dies kann auch mit dem Suffix "" (dem Grad Symbol) signalisiert werden. Diese Verwendung hängt jedoch davon ab, dass eine geeignete Dokument Codierung vorhanden ist. Folglich wird das Suffix "deg" auch als Mittelwert definiert.</span><span class="sxs-lookup"><span data-stu-id="17764-308">This may also be signalled with the suffix " " (the degree symbol); however, use of this depends on having a suitable document encoding -- consequently, the suffix deg is also defined to mean degrees.</span></span> <span data-ttu-id="17764-309">Der vollständige Satz möglicher mögliche genügt ist wie folgt.</span><span class="sxs-lookup"><span data-stu-id="17764-309">The full set of possible suffices are as follows.</span></span>



| <span data-ttu-id="17764-310">Suffix</span><span class="sxs-lookup"><span data-stu-id="17764-310">Suffix</span></span>       | <span data-ttu-id="17764-311">Konvertierungsfaktor</span><span class="sxs-lookup"><span data-stu-id="17764-311">Conversion Factor</span></span> | <span data-ttu-id="17764-312">Kommentare</span><span class="sxs-lookup"><span data-stu-id="17764-312">Comments</span></span>                               |
|--------------|-------------------|----------------------------------------|
| <span data-ttu-id="17764-313">FD</span><span class="sxs-lookup"><span data-stu-id="17764-313">fd</span></span>           | <span data-ttu-id="17764-314">1</span><span class="sxs-lookup"><span data-stu-id="17764-314">1</span></span>                 | <span data-ttu-id="17764-315">Interne Darstellung mit hoher Genauigkeit</span><span class="sxs-lookup"><span data-stu-id="17764-315">High-precision internal representation</span></span> |
| <span data-ttu-id="17764-316">keine, DEG,</span><span class="sxs-lookup"><span data-stu-id="17764-316">none, deg,</span></span>   | <span data-ttu-id="17764-317">65536</span><span class="sxs-lookup"><span data-stu-id="17764-317">65536</span></span>             | <span data-ttu-id="17764-318">Grad</span><span class="sxs-lookup"><span data-stu-id="17764-318">Degrees</span></span>                                |
| <span data-ttu-id="17764-319">rad</span><span class="sxs-lookup"><span data-stu-id="17764-319">rad</span></span>          | <span data-ttu-id="17764-320">65536pi/180</span><span class="sxs-lookup"><span data-stu-id="17764-320">65536pi/180</span></span>       | <span data-ttu-id="17764-321">Radians</span><span class="sxs-lookup"><span data-stu-id="17764-321">Radians</span></span>                                |



 

### <a name="alternative-representations"></a><span data-ttu-id="17764-322">Alternative Darstellungen</span><span class="sxs-lookup"><span data-stu-id="17764-322">Alternative representations</span></span>

<span data-ttu-id="17764-323">Die Skalierungs Transformation weist Diskontinuitäten bei ungeraden Vielfachen von 45 auf.</span><span class="sxs-lookup"><span data-stu-id="17764-323">The scaling transformation has discontinuities at odd multiples of 45 .</span></span> <span data-ttu-id="17764-324">Daher ist es äußerst wichtig für die Konvertierung von ungenauer Menge, um genau definiert zu werden.</span><span class="sxs-lookup"><span data-stu-id="17764-324">It is, therefore, extremely important for the conversion of any inexact quantity to be well defined.</span></span> <span data-ttu-id="17764-325">Aus diesem Grund wird die Arithmetik der Konvertierung für die Rundung auf minus unendlich definiert.</span><span class="sxs-lookup"><span data-stu-id="17764-325">For this reason, the arithmetic of conversion is defined to round towards minus infinity.</span></span>

<span data-ttu-id="17764-326">Da dies in einigen Implementierungen schwierig oder unmöglich sein kann, ist die Verwendung des folgenden als ein Feature der Ebene 3 definiert:</span><span class="sxs-lookup"><span data-stu-id="17764-326">Because this may be difficult or impossible to guarantee in some implementations, the use of the following is defined to be a level 3 feature:</span></span>

1.  <span data-ttu-id="17764-327">Ein beliebiger Grad Wert.</span><span class="sxs-lookup"><span data-stu-id="17764-327">Any fractional degree value.</span></span>
2.  <span data-ttu-id="17764-328">Beliebiger Bogenmaß Wert-Wert</span><span class="sxs-lookup"><span data-stu-id="17764-328">Any radian value</span></span>

<span data-ttu-id="17764-329">Folglich werden Werte mit den qualifizierten FD-Werten, nicht qualifizierten ganzzahligen Werten oder ganzzahligen Werten, die für die deg qualifiziert sind oder genau durch eine konforme Implementierung der Ebene andere Werte sind nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="17764-329">Thus, values qualified fd and unqualified integral values, or integral values qualified deg or   must be handled exactly by a conforming level 0 implementation; other values need not.</span></span> <span data-ttu-id="17764-330">Es wird dringend empfohlen, dass jede Implementierung die Konvertierung von einem Bruchteil eines Bruch Werts in einen skalierten (FD-) Grad Wert genau verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="17764-330">It is strongly recommended that any implementation handle the conversion from a fractional degree value to a scaled (fd) degree value exactly.</span></span> <span data-ttu-id="17764-331">Dies kann ohne Gleit Komma Unterstützung erfolgen.</span><span class="sxs-lookup"><span data-stu-id="17764-331">This can be done without floating point support.</span></span>

<span data-ttu-id="17764-332">Die anspruchsvolleren Anforderungen für die Konvertierung unterscheiden FD von f.</span><span class="sxs-lookup"><span data-stu-id="17764-332">The more exacting requirements for conversion distinguish fd from f.</span></span>

<span data-ttu-id="17764-333">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="17764-333">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="color"></a><span data-ttu-id="17764-334">color</span><span class="sxs-lookup"><span data-stu-id="17764-334">color</span></span>


```HTML
c
<!element c  %color;>
```



<span data-ttu-id="17764-335">Farben sind ein wesentlicher Bestandteil moderner Computergrafiken.</span><span class="sxs-lookup"><span data-stu-id="17764-335">Colors are an essential part of modern computer graphics.</span></span> <span data-ttu-id="17764-336">Der Vorschlag verwendet die etablierten Methoden zum Angeben fester Farben.</span><span class="sxs-lookup"><span data-stu-id="17764-336">The proposal uses the established methods of specifying fixed colors.</span></span> <span data-ttu-id="17764-337">Farben in Diagrammen sind jedoch selten einfache statische Farben. Sie werden oft von anderen Elementen im Diagramm abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="17764-337">However, colors in diagrams are rarely simple static colors; they are often derived from other elements in the diagram.</span></span> <span data-ttu-id="17764-338">Viele dieser Informationen sind anwendungsspezifisch, sodass dieser Vorschlag zwei grundlegende Mechanismen zur Angabe eines solchen Verhaltens bietet:</span><span class="sxs-lookup"><span data-stu-id="17764-338">Much of this information is very application-specific, so this proposal provides two very basic mechanisms to specify such behavior:</span></span>

1.  <span data-ttu-id="17764-339">Eine Farbe kann aus einer anderen Farbe in derselben Form abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="17764-339">A color may be derived from another color in the same shape.</span></span>
2.  <span data-ttu-id="17764-340">Eine kleine Anzahl von arithmetischen Vorgängen wird für das ableiten oder Ändern einer Farbe definiert.</span><span class="sxs-lookup"><span data-stu-id="17764-340">A small number of arithmetic operations are defined for deriving, or modifying, a color.</span></span>

<span data-ttu-id="17764-341">Der Prototype-Shape-Mechanismus ergänzt dies, indem es das Definieren von Prototypen ermöglicht, von welchen Farben geerbt werden können.</span><span class="sxs-lookup"><span data-stu-id="17764-341">The prototype shape mechanism supplements this by allow prototypes to be defined from which colors can be inherited.</span></span>


```HTML
color
<!entity % color "( %color-unit; | pure | %color.adjustment; )*">
```



<span data-ttu-id="17764-342">Ein Farbwert ist eine supermenge der [CSS1-Farbdefinition](https://www.w3.org/pub/WWW/TR/REC-CSS1#color-units) .</span><span class="sxs-lookup"><span data-stu-id="17764-342">A color value is a superset of the [CSS1 color definition](https://www.w3.org/pub/WWW/TR/REC-CSS1#color-units) .</span></span> <span data-ttu-id="17764-343">Mithilfe der Erweiterungen kann der RGB-Farbwert aus anderen Farben innerhalb der Form oder aus einem mit CSS1 definierten Gesamt Farbschema ermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="17764-343">The extensions allow the RGB color value to be determined from other colors within the shape or from an overall color scheme defined using CSS1.</span></span>

<span data-ttu-id="17764-344">Wenn der Wert eines Elements als Farbe definiert ist, definiert der *Inhalt* eines Elements den Farbwert mithilfe eines einzelnen farbtokens, das optional durch eine arithmetische Operation in der entsprechenden RGB-Farbe geändert wird.</span><span class="sxs-lookup"><span data-stu-id="17764-344">If the value of an element is defined to be a color, the *content* of an element defines the color value by means of a single color token optionally modified by an arithmetic operation on the corresponding RGB color.</span></span>

<span data-ttu-id="17764-345">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="17764-345">[![back to top](images/top.gif) Back to top](#top)</span></span>

### <a name="color-units"></a><span data-ttu-id="17764-346">Farbeinheiten</span><span class="sxs-lookup"><span data-stu-id="17764-346">Color units</span></span>

<span data-ttu-id="17764-347">Der vollständige Satz von farbtoken stammt aus einer Vielzahl von Quellen: HTML, CSS1 und diesem Vorschlag.</span><span class="sxs-lookup"><span data-stu-id="17764-347">The full set of color tokens come from a variety of sources: HTML, CSS1, and this proposal.</span></span> <span data-ttu-id="17764-348">Sie werden wie folgt definiert, indem Notation aus [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1) oder die für XML-Verknüpfungen definierte XPointer-Notation verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="17764-348">They are defined as follows using notation from [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1) or the XPointer notation defined for XML linking.</span></span>

<span data-ttu-id="17764-349">In den XPointer-Definitionen ist die Speicherort Quelle das Element, das den Farbwert enthält, und der Ausdruck verweist auf den gesamten Element Satz der Form, so als ob alle Base Prototype-Elemente mit der Form zusammengeführt worden wären.</span><span class="sxs-lookup"><span data-stu-id="17764-349">In the XPointer definitions, the location source is the element containing the color value, and the expression refers to the whole element set of the shape as though any base prototype elements had been merged with the shape.</span></span> <span data-ttu-id="17764-350">Wenn das entsprechende Element nicht vorhanden ist, wird an seiner Stelle der Standardwert für dieses Element verwendet.</span><span class="sxs-lookup"><span data-stu-id="17764-350">When the corresponding element does not exist, the default value for that element is used in its place.</span></span>



| <span data-ttu-id="17764-351">Color</span><span class="sxs-lookup"><span data-stu-id="17764-351">Color</span></span>            | <span data-ttu-id="17764-352">Definition</span><span class="sxs-lookup"><span data-stu-id="17764-352">Definition</span></span>                                                                                                  | <span data-ttu-id="17764-353">Ebene</span><span class="sxs-lookup"><span data-stu-id="17764-353">Level</span></span> | <span data-ttu-id="17764-354">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="17764-354">Description</span></span>                                                                                                                                                               |
|------------------|-------------------------------------------------------------------------------------------------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17764-355">name</span><span class="sxs-lookup"><span data-stu-id="17764-355">name</span></span>             | <span data-ttu-id="17764-356">Siehe unten</span><span class="sxs-lookup"><span data-stu-id="17764-356">See below</span></span>                                                                                                   | <span data-ttu-id="17764-357">0</span><span class="sxs-lookup"><span data-stu-id="17764-357">0</span></span>     | <span data-ttu-id="17764-358">HTML-Farbname, wie in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="17764-358">HTML color name, as listed in the table below.</span></span>                                                                                                                            |
| <span data-ttu-id="17764-359">\#rr' gg' g '</span><span class="sxs-lookup"><span data-stu-id="17764-359">\#rr'gg'bb'</span></span>      | <span data-ttu-id="17764-360">\#rr' gg' g '</span><span class="sxs-lookup"><span data-stu-id="17764-360">\#rr'gg'bb'</span></span>                                                                                                 | <span data-ttu-id="17764-361">0</span><span class="sxs-lookup"><span data-stu-id="17764-361">0</span></span>     | <span data-ttu-id="17764-362">Standard mäßige CSS1/sRGB-Farbdarstellung mit Werten im Bereich 0.. 255, die mit zwei hexadezimal Ziffern dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="17764-362">Standard CSS1/sRGB color representation using values in the range 0..255 represented using 2 hexadecimal digits each.</span></span>                                                     |
| <span data-ttu-id="17764-363">\#Set</span><span class="sxs-lookup"><span data-stu-id="17764-363">\#rgb</span></span>            | <span data-ttu-id="17764-364">\#RRGGBB</span><span class="sxs-lookup"><span data-stu-id="17764-364">\#rrggbb</span></span>                                                                                                    | <span data-ttu-id="17764-365">1</span><span class="sxs-lookup"><span data-stu-id="17764-365">1</span></span>     | <span data-ttu-id="17764-366">Verkürztes CSS1-Formular mit nur drei hexadezimalen Ziffern.</span><span class="sxs-lookup"><span data-stu-id="17764-366">Shortened CSS1 form with only three hexadecimal digits.</span></span>                                                                                                                   |
| <span data-ttu-id="17764-367">RGB (r, g, b)</span><span class="sxs-lookup"><span data-stu-id="17764-367">rgb(r,g,b)</span></span>       | <span data-ttu-id="17764-368">\#r selbst b</span><span class="sxs-lookup"><span data-stu-id="17764-368">\#(r)(g)(b)</span></span>                                                                                                 | <span data-ttu-id="17764-369">1</span><span class="sxs-lookup"><span data-stu-id="17764-369">1</span></span>     | <span data-ttu-id="17764-370">CSS1 RGB-Formular; die Elemente des RGB-Werts werden entsprechend der Definition in [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#color-units) konvertiert.</span><span class="sxs-lookup"><span data-stu-id="17764-370">CSS1 rgb form; the elements of the rgb value are converted as defined in [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#color-units) .</span></span>                                      |
| <span data-ttu-id="17764-371">fill</span><span class="sxs-lookup"><span data-stu-id="17764-371">fill</span></span>             | <span data-ttu-id="17764-372">Vorgänger (1, Form)</span><span class="sxs-lookup"><span data-stu-id="17764-372">ancestor(1,shape)</span></span><br/> <span data-ttu-id="17764-373">Child (1, Fill)</span><span class="sxs-lookup"><span data-stu-id="17764-373">child(1, fill)</span></span><br/> <span data-ttu-id="17764-374">Child (1, Farbe)</span><span class="sxs-lookup"><span data-stu-id="17764-374">child(1, color)</span></span><br/>                           | <span data-ttu-id="17764-375">1</span><span class="sxs-lookup"><span data-stu-id="17764-375">1</span></span>     | <span data-ttu-id="17764-376">Die Vorder grundfüllfarbe der Form.</span><span class="sxs-lookup"><span data-stu-id="17764-376">The foreground fill color of the shape.</span></span>                                                                                                                                   |
| <span data-ttu-id="17764-377">fillback</span><span class="sxs-lookup"><span data-stu-id="17764-377">fillBack</span></span>         | <span data-ttu-id="17764-378">Vorgänger (1, Form)</span><span class="sxs-lookup"><span data-stu-id="17764-378">ancestor(1,shape)</span></span><br/> <span data-ttu-id="17764-379">Child (1, Fill)</span><span class="sxs-lookup"><span data-stu-id="17764-379">child(1, fill)</span></span><br/> <span data-ttu-id="17764-380">Child (1, zurück)</span><span class="sxs-lookup"><span data-stu-id="17764-380">child(1, back)</span></span><br/> <span data-ttu-id="17764-381">Child (1, Farbe)</span><span class="sxs-lookup"><span data-stu-id="17764-381">child(1, color)</span></span><br/> | <span data-ttu-id="17764-382">1</span><span class="sxs-lookup"><span data-stu-id="17764-382">1</span></span>     | <span data-ttu-id="17764-383">Die Hintergrundfarbe der Form Füllung.</span><span class="sxs-lookup"><span data-stu-id="17764-383">The background color of the shape fill.</span></span>                                                                                                                                   |
| <span data-ttu-id="17764-384">line</span><span class="sxs-lookup"><span data-stu-id="17764-384">line</span></span>             | <span data-ttu-id="17764-385">Vorgänger (1, Form)</span><span class="sxs-lookup"><span data-stu-id="17764-385">ancestor(1,shape)</span></span><br/> <span data-ttu-id="17764-386">Child (1, Zeile)</span><span class="sxs-lookup"><span data-stu-id="17764-386">child(1, line)</span></span><br/> <span data-ttu-id="17764-387">Child (1, Farbe)</span><span class="sxs-lookup"><span data-stu-id="17764-387">child(1, color)</span></span><br/>                           | <span data-ttu-id="17764-388">1</span><span class="sxs-lookup"><span data-stu-id="17764-388">1</span></span>     | <span data-ttu-id="17764-389">Die Vorder Grundlinien Farbe der Form.</span><span class="sxs-lookup"><span data-stu-id="17764-389">The foreground line color of the shape.</span></span>                                                                                                                                   |
| <span data-ttu-id="17764-390">Lineback</span><span class="sxs-lookup"><span data-stu-id="17764-390">lineBack</span></span>         | <span data-ttu-id="17764-391">Vorgänger (1, Form)</span><span class="sxs-lookup"><span data-stu-id="17764-391">ancestor(1,shape)</span></span><br/> <span data-ttu-id="17764-392">Child (1, Zeile)</span><span class="sxs-lookup"><span data-stu-id="17764-392">child(1, line)</span></span><br/> <span data-ttu-id="17764-393">Child (1, zurück)</span><span class="sxs-lookup"><span data-stu-id="17764-393">child(1,back)</span></span> <br/> <span data-ttu-id="17764-394">Child (1, Farbe)</span><span class="sxs-lookup"><span data-stu-id="17764-394">child(1, color)</span></span><br/> | <span data-ttu-id="17764-395">1</span><span class="sxs-lookup"><span data-stu-id="17764-395">1</span></span>     | <span data-ttu-id="17764-396">Die Hintergrund Linien Farbe der Form.</span><span class="sxs-lookup"><span data-stu-id="17764-396">The background line color of the shape.</span></span>                                                                                                                                   |
| <span data-ttu-id="17764-397">lineorfill</span><span class="sxs-lookup"><span data-stu-id="17764-397">lineOrFill</span></span>       | <span data-ttu-id="17764-398">Zeile, ausfüllen</span><span class="sxs-lookup"><span data-stu-id="17764-398">line, fill</span></span>                                                                                                  | <span data-ttu-id="17764-399">1</span><span class="sxs-lookup"><span data-stu-id="17764-399">1</span></span>     | <span data-ttu-id="17764-400">Der Zeilen Wert, wenn kein Standardwert ist, andernfalls der Füllwert.</span><span class="sxs-lookup"><span data-stu-id="17764-400">The line value if not defaulted, otherwise the fill value.</span></span> <span data-ttu-id="17764-401">Dadurch wird die Farbe an der Kante der Form zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="17764-401">This effectively returns the color that is at the edge of the shape.</span></span>                                           |
| <span data-ttu-id="17764-402">fillthenline</span><span class="sxs-lookup"><span data-stu-id="17764-402">fillThenLine</span></span>     | <span data-ttu-id="17764-403">ausfüllen, Zeile</span><span class="sxs-lookup"><span data-stu-id="17764-403">fill, line</span></span>                                                                                                  | <span data-ttu-id="17764-404">1</span><span class="sxs-lookup"><span data-stu-id="17764-404">1</span></span>     | <span data-ttu-id="17764-405">Der Füllwert, wenn nicht der Standardwert, andernfalls der Zeilen Wert.</span><span class="sxs-lookup"><span data-stu-id="17764-405">The fill value if not defaulted, otherwise the line value.</span></span> <span data-ttu-id="17764-406">Dadurch wird die Haupt Form Farbe zurückgegeben (wenn die Form nicht aufgefüllt ist, ist das Ergebnis die Linien Farbe).</span><span class="sxs-lookup"><span data-stu-id="17764-406">This effectively returns the main shape color (if the shape is unfilled, the result will be the line color).</span></span>   |
| <span data-ttu-id="17764-407">shadow</span><span class="sxs-lookup"><span data-stu-id="17764-407">shadow</span></span>           | <span data-ttu-id="17764-408">Vorgänger (1, Form)</span><span class="sxs-lookup"><span data-stu-id="17764-408">ancestor(1,shape)</span></span><br/> <span data-ttu-id="17764-409">Child (1, Shadow)</span><span class="sxs-lookup"><span data-stu-id="17764-409">child(1, shadow)</span></span><br/> <span data-ttu-id="17764-410">Child (1, Farbe)</span><span class="sxs-lookup"><span data-stu-id="17764-410">child(1, color)</span></span><br/>                         | <span data-ttu-id="17764-411">2</span><span class="sxs-lookup"><span data-stu-id="17764-411">2</span></span>     | <span data-ttu-id="17764-412">Die Farbe des Schattens (Hierbei handelt es sich um eine Funktion auf Ebene 2).</span><span class="sxs-lookup"><span data-stu-id="17764-412">The color of the shadow (this is a level 2 feature).</span></span>                                                                                                                      |
| <span data-ttu-id="17764-413">scheme</span><span class="sxs-lookup"><span data-stu-id="17764-413">scheme</span></span>           | <span data-ttu-id="17764-414">Siehe unten</span><span class="sxs-lookup"><span data-stu-id="17764-414">See below</span></span>                                                                                                   | <span data-ttu-id="17764-415">1</span><span class="sxs-lookup"><span data-stu-id="17764-415">1</span></span>     | <span data-ttu-id="17764-416">Eine Schema Farbe aus dem Schema, das für das Dokument definiert ist. siehe unten.</span><span class="sxs-lookup"><span data-stu-id="17764-416">A scheme color from the scheme defined for the document; see below.</span></span>                                                                                                       |
| <span data-ttu-id="17764-417">Schema (*Index*)</span><span class="sxs-lookup"><span data-stu-id="17764-417">scheme(*index*)</span></span>  | <span data-ttu-id="17764-418">Siehe unten</span><span class="sxs-lookup"><span data-stu-id="17764-418">See below</span></span>                                                                                                   | <span data-ttu-id="17764-419">1</span><span class="sxs-lookup"><span data-stu-id="17764-419">1</span></span>     | <span data-ttu-id="17764-420">Schema Farb *Index*, beginnend bei 0; siehe unten.</span><span class="sxs-lookup"><span data-stu-id="17764-420">Scheme color *index*, starting from 0; see below.</span></span>                                                                                                                         |
| <span data-ttu-id="17764-421">this</span><span class="sxs-lookup"><span data-stu-id="17764-421">this</span></span>             | <span data-ttu-id="17764-422">Impliziert</span><span class="sxs-lookup"><span data-stu-id="17764-422">Implied</span></span>                                                                                                     | <span data-ttu-id="17764-423">2</span><span class="sxs-lookup"><span data-stu-id="17764-423">2</span></span>     | <span data-ttu-id="17764-424">Der Vorgang (Ausfüllen eines Pfads oder zeichnen) wird auf andere Weise definiert (z. b. als Bitmap), und die Farbe gibt eine "Änderung" für die Farben an, die so impliziert sind.</span><span class="sxs-lookup"><span data-stu-id="17764-424">The operation (filling a path, or drawing it) is defined in some other way (for example, as a bitmap), and the color specifies a "modification" to the colors so implied.</span></span> |
| <span data-ttu-id="17764-425">Palette (*Index*)</span><span class="sxs-lookup"><span data-stu-id="17764-425">palette(*index*)</span></span> | <span data-ttu-id="17764-426">Impliziert</span><span class="sxs-lookup"><span data-stu-id="17764-426">Implied</span></span>                                                                                                     | <span data-ttu-id="17764-427">3</span><span class="sxs-lookup"><span data-stu-id="17764-427">3</span></span>     | <span data-ttu-id="17764-428">Verhält sich auf dieselbe Weise wie diese, mit der Ausnahme, dass genau ein Eintrag in einer Bitmap-Farbtabelle identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="17764-428">Behaves in the same way as this, except that exactly one entry in a bitmap color table is identified.</span></span> <span data-ttu-id="17764-429">Nur zulässig, wenn explizit angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="17764-429">Permitted only where explicitly stated.</span></span>                             |
| <span data-ttu-id="17764-430">none</span><span class="sxs-lookup"><span data-stu-id="17764-430">none</span></span>             | \-                                                                                                          | <span data-ttu-id="17764-431">2</span><span class="sxs-lookup"><span data-stu-id="17764-431">2</span></span>     | <span data-ttu-id="17764-432">Gibt an, dass keine Farbe vorhanden ist. kann verwendet werden, um einen Zeichnungs Vorgang abzubrechen, der die Farbe verwendet.</span><span class="sxs-lookup"><span data-stu-id="17764-432">Indicates the absence of a color; may be used to cancel a drawing operation that uses the color.</span></span>                                                                          |
| <span data-ttu-id="17764-433">System</span><span class="sxs-lookup"><span data-stu-id="17764-433">system</span></span>           | <span data-ttu-id="17764-434">Siehe unten</span><span class="sxs-lookup"><span data-stu-id="17764-434">See below</span></span>                                                                                                   | <span data-ttu-id="17764-435">3</span><span class="sxs-lookup"><span data-stu-id="17764-435">3</span></span>     | <span data-ttu-id="17764-436">Eine von der Systembenutzer Oberfläche definierte Farbe.</span><span class="sxs-lookup"><span data-stu-id="17764-436">A color defined by the system user interface.</span></span>                                                                                                                             |



 

<span data-ttu-id="17764-437">Mit dieser Farbe kann ein Farbwert eine Änderung an einer Farbe angeben, die auf andere Weise abgeleitet ist. insbesondere kann ein einzelner Vorgang für alle Farben in einer Bitmap angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="17764-437">The this color allows a color value to specify a modification to a color which is derived in some other way; in particular, a single operation may be specified for all the colors in a bitmap.</span></span> <span data-ttu-id="17764-438">Die Farbe der Palette (*Index*) identifiziert einen bestimmten Eintrag in einer Palette zugeordneten Bitmap.</span><span class="sxs-lookup"><span data-stu-id="17764-438">The palette(*index*) color identifies a particular entry in a palette-mapped bitmap.</span></span> <span data-ttu-id="17764-439">Die Verwendung dieser wird nur zum Aufzeichnen eines Farbtabellen Eintrags definiert, der in einer solchen Bitmap als transparent angesehen werden sollte.</span><span class="sxs-lookup"><span data-stu-id="17764-439">Use of this is only defined for recording a color table entry that should be regarded as transparent in such a bitmap.</span></span>

<span data-ttu-id="17764-440">Die Definition eines Farbwerts darf weder direkt noch indirekt auf sich selbst verweisen.</span><span class="sxs-lookup"><span data-stu-id="17764-440">The definition of a color value must not refer to itself, either directly or indirectly.</span></span> <span data-ttu-id="17764-441">Wenn eine solche Definition fest steht, wird empfohlen, aber nicht erforderlich, dass die Implementierung den nicht definierten Wert als schwarz behandelt.</span><span class="sxs-lookup"><span data-stu-id="17764-441">If such a definition is encountered, it is recommended, but not required, that the implementation treat the undefined value as black.</span></span>

<span data-ttu-id="17764-442">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="17764-442">[![back to top](images/top.gif) Back to top](#top)</span></span>

### <a name="html-colors"></a><span data-ttu-id="17764-443">HTML-Farben</span><span class="sxs-lookup"><span data-stu-id="17764-443">HTML colors</span></span>

<span data-ttu-id="17764-444">[HTML](https://www.w3.org/TR/wd-html40-970708/types.mdl#type-color) definiert die folgenden 16 Farbnamen:</span><span class="sxs-lookup"><span data-stu-id="17764-444">[HTML](https://www.w3.org/TR/wd-html40-970708/types.mdl#type-color) defines the following sixteen color names:</span></span>



<span data-ttu-id="17764-445">Farbnamen und sRGB-Werte</span><span class="sxs-lookup"><span data-stu-id="17764-445">Color names and sRGB values</span></span>

![Beispiel für schwarze Farbe.](images/black.gif)

<span data-ttu-id="17764-447">Schwarz = " \# 000000"</span><span class="sxs-lookup"><span data-stu-id="17764-447">Black = "\#000000"</span></span>

![Beispiel für grüne Farbe.](images/green.gif)

<span data-ttu-id="17764-449">Grün = " \# 008000"</span><span class="sxs-lookup"><span data-stu-id="17764-449">Green = "\#008000"</span></span>

![Beispiel für Silver-Farbe.](images/silver.gif)

<span data-ttu-id="17764-451">Silver = " \# C0C0C0"</span><span class="sxs-lookup"><span data-stu-id="17764-451">Silver = "\#C0C0C0"</span></span>

![Beispiel für eine Kalk Farbe.](images/lime.gif)

<span data-ttu-id="17764-453">Kalk = " \# 00FF00"</span><span class="sxs-lookup"><span data-stu-id="17764-453">Lime = "\#00FF00"</span></span>

![Beispiel für graue Farbe.](images/gray.gif)

<span data-ttu-id="17764-455">Grau = " \# 808080"</span><span class="sxs-lookup"><span data-stu-id="17764-455">Gray = "\#808080"</span></span>

![Beispiel für eine Oliven Farbe.](images/olive.gif)

<span data-ttu-id="17764-457">Olive = " \# 808000"</span><span class="sxs-lookup"><span data-stu-id="17764-457">Olive = "\#808000"</span></span>

![Beispiel für weiß Farbe.](images/white.gif)

<span data-ttu-id="17764-459">Weiß = " \# FFFFFF"</span><span class="sxs-lookup"><span data-stu-id="17764-459">White = "\#FFFFFF"</span></span>

![Beispiel für ywllow Color.](images/yellow.gif)

<span data-ttu-id="17764-461">Gelb = " \# FFFF00"</span><span class="sxs-lookup"><span data-stu-id="17764-461">Yellow = "\#FFFF00"</span></span>

![Beispiel für eine kastanienbraun-Farbe.](images/maroon.gif)

<span data-ttu-id="17764-463">Maroon = " \# 800000"</span><span class="sxs-lookup"><span data-stu-id="17764-463">Maroon = "\#800000"</span></span>

![Beispiel für die Farbe der Marine.](images/navy.gif)

<span data-ttu-id="17764-465">Navy = " \# 000080"</span><span class="sxs-lookup"><span data-stu-id="17764-465">Navy = "\#000080"</span></span>

![Beispiel für rote Farbe.](images/red.gif)

<span data-ttu-id="17764-467">Rot = " \# FF0000"</span><span class="sxs-lookup"><span data-stu-id="17764-467">Red = "\#FF0000"</span></span>

![Beispiel für blaue Farbe.](images/blue.gif)

<span data-ttu-id="17764-469">Blue = " \# 0000FF"</span><span class="sxs-lookup"><span data-stu-id="17764-469">Blue = "\#0000FF"</span></span>

![Beispiel für lila Farbe.](images/purple.gif)

<span data-ttu-id="17764-471">Lila = " \# 800080"</span><span class="sxs-lookup"><span data-stu-id="17764-471">Purple = "\#800080"</span></span>

![Beispiel für eine blaugrün-Farbe.](images/teal.gif)

<span data-ttu-id="17764-473">Teal = " \# 008080"</span><span class="sxs-lookup"><span data-stu-id="17764-473">Teal = "\#008080"</span></span>

![Beispiel für die Fuchsia-Farbe.](images/fuchsia.gif)

<span data-ttu-id="17764-475">Fuchsia = " \# FF00FF"</span><span class="sxs-lookup"><span data-stu-id="17764-475">Fuchsia = "\#FF00FF"</span></span>

![Beispiel für eine Aqua-Farbe.](images/aqua.gif)

<span data-ttu-id="17764-477">Aqua = " \# 00ffff"</span><span class="sxs-lookup"><span data-stu-id="17764-477">Aqua = "\#00FFFF"</span></span>



 

<span data-ttu-id="17764-478">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="17764-478">[![back to top](images/top.gif) Back to top](#top)</span></span>

### <a name="scheme-colors"></a><span data-ttu-id="17764-479">Schema Farben</span><span class="sxs-lookup"><span data-stu-id="17764-479">Scheme colors</span></span>

<span data-ttu-id="17764-480">Die Schema Farben, auf die durch das Schema verwiesen wird, werden auf Dokument Ebene mithilfe des Meta-Tags mit dem Namensattribut "Design Color Scheme" definiert.</span><span class="sxs-lookup"><span data-stu-id="17764-480">The scheme colors referenced by scheme are defined at the document level using the meta tag with a name attribute of "Theme Color Scheme".</span></span>


```HTML
<meta name="Theme Color Scheme"
  content="rrggbb, rrggbb, rrggbb, rrggbb, rrggbb, rrggbb, rrggbb, rrggbb">
```



<span data-ttu-id="17764-481">Dieses Tag ermöglicht das Definieren von bis zu acht Schema Farben.</span><span class="sxs-lookup"><span data-stu-id="17764-481">This tag allows up to eight scheme colors to be defined.</span></span> <span data-ttu-id="17764-482">Nicht definierte Farben sollten standardmäßig auf Schwarz eingestellt werden.</span><span class="sxs-lookup"><span data-stu-id="17764-482">Undefined colors should default to black.</span></span> <span data-ttu-id="17764-483">Die Schema Farben ermöglichen das Ändern des Farbschemas, das für ein ganzes Dokument verwendet wird, indem Sie den Inhalt des Design Farbschemas ändern.</span><span class="sxs-lookup"><span data-stu-id="17764-483">The scheme colors allow the color scheme used for a complete document to be changed just by altering the Theme Color Scheme contents.</span></span> <span data-ttu-id="17764-484">Um sicherzustellen, dass die aus anderen Erstellungs Anwendungen importierten Grafiken eine konsistente Verwendung der Schema Farben machen, werden die folgenden Interpretationen definiert.</span><span class="sxs-lookup"><span data-stu-id="17764-484">To ensure that graphics imported from different authoring applications make consistent use of the scheme colors, the following interpretations are defined.</span></span> <span data-ttu-id="17764-485">Die "Verwendung" ist eine kurze Beschreibung des Zwecks, und in der Spalte "Beschreibung" finden Sie weitere Details.</span><span class="sxs-lookup"><span data-stu-id="17764-485">The "usage" is a short description of the purpose, and the "description" column provides additional details.</span></span>



| <span data-ttu-id="17764-486">Index</span><span class="sxs-lookup"><span data-stu-id="17764-486">Index</span></span> | <span data-ttu-id="17764-487">Name</span><span class="sxs-lookup"><span data-stu-id="17764-487">Name</span></span>              | <span data-ttu-id="17764-488">Verwendung</span><span class="sxs-lookup"><span data-stu-id="17764-488">Usage</span></span>                         | <span data-ttu-id="17764-489">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="17764-489">Description</span></span>                                                                                                              |
|-------|-------------------|-------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17764-490">0</span><span class="sxs-lookup"><span data-stu-id="17764-490">0</span></span>     | <span data-ttu-id="17764-491">Schema. Hintergrund</span><span class="sxs-lookup"><span data-stu-id="17764-491">scheme.background</span></span> | <span data-ttu-id="17764-492">Hintergrund</span><span class="sxs-lookup"><span data-stu-id="17764-492">Background</span></span>                    | <span data-ttu-id="17764-493">Die Farbe, die für den Hintergrund einer Grafik verwendet wird (und häufig für die gesamte Seite).</span><span class="sxs-lookup"><span data-stu-id="17764-493">The color used for the background of a graphic (and, frequently, for the whole page).</span></span>                                    |
| <span data-ttu-id="17764-494">1</span><span class="sxs-lookup"><span data-stu-id="17764-494">1</span></span>     | <span data-ttu-id="17764-495">Schema. Text</span><span class="sxs-lookup"><span data-stu-id="17764-495">scheme.text</span></span>       | <span data-ttu-id="17764-496">Text und Zeilen</span><span class="sxs-lookup"><span data-stu-id="17764-496">Text and lines</span></span>                | <span data-ttu-id="17764-497">Die Farbe für Text, der an eine Form und die Standardlinien Farbe angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="17764-497">The color for text attached to a shape and the standard line color.</span></span>                                                      |
| <span data-ttu-id="17764-498">2</span><span class="sxs-lookup"><span data-stu-id="17764-498">2</span></span>     | <span data-ttu-id="17764-499">Schema. Shadow</span><span class="sxs-lookup"><span data-stu-id="17764-499">scheme.shadow</span></span>     | <span data-ttu-id="17764-500">Shadows</span><span class="sxs-lookup"><span data-stu-id="17764-500">Shadows</span></span>                       | <span data-ttu-id="17764-501">Standard Schatten Farbe: die Farbe, die normalerweise für Form Schatten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="17764-501">Standard shadow color -- the color typically used for shape shadows.</span></span>                                                     |
| <span data-ttu-id="17764-502">3</span><span class="sxs-lookup"><span data-stu-id="17764-502">3</span></span>     | <span data-ttu-id="17764-503">Schema. Title</span><span class="sxs-lookup"><span data-stu-id="17764-503">scheme.title</span></span>      | <span data-ttu-id="17764-504">Titeltext</span><span class="sxs-lookup"><span data-stu-id="17764-504">Title text</span></span>                    | <span data-ttu-id="17764-505">Die Farbe, die für Überschriften-oder Titeltext verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="17764-505">The color to use for heading or title text.</span></span>                                                                              |
| <span data-ttu-id="17764-506">4</span><span class="sxs-lookup"><span data-stu-id="17764-506">4</span></span>     | <span data-ttu-id="17764-507">Schema. Fill</span><span class="sxs-lookup"><span data-stu-id="17764-507">scheme.fill</span></span>       | <span data-ttu-id="17764-508">Füllt</span><span class="sxs-lookup"><span data-stu-id="17764-508">Fills</span></span>                         | <span data-ttu-id="17764-509">Standard Füllfarbe: die Farbe, die normalerweise zum Auffüllen von Formen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="17764-509">Standard fill color -- the color typically used to fill shapes.</span></span>                                                          |
| <span data-ttu-id="17764-510">5</span><span class="sxs-lookup"><span data-stu-id="17764-510">5</span></span>     | <span data-ttu-id="17764-511">Schema. Akzent</span><span class="sxs-lookup"><span data-stu-id="17764-511">scheme.accent</span></span>     | <span data-ttu-id="17764-512">Betont</span><span class="sxs-lookup"><span data-stu-id="17764-512">Accent</span></span>                        | <span data-ttu-id="17764-513">Normale Hervorhebungs Farbe, die verwendet wird, um ein wichtiges Element einer Grafik hervorzuheben.</span><span class="sxs-lookup"><span data-stu-id="17764-513">Normal "highlight" color used to emphasis an important element of a graphic.</span></span>                                             |
| <span data-ttu-id="17764-514">6</span><span class="sxs-lookup"><span data-stu-id="17764-514">6</span></span>     | <span data-ttu-id="17764-515">Schema. Hyperlink</span><span class="sxs-lookup"><span data-stu-id="17764-515">scheme.hyperlink</span></span>  | <span data-ttu-id="17764-516">Akzent und Hyperlink</span><span class="sxs-lookup"><span data-stu-id="17764-516">Accent and hyperlink</span></span>          | <span data-ttu-id="17764-517">Hervorhebungs Farbe für Hyperlinks.</span><span class="sxs-lookup"><span data-stu-id="17764-517">Highlight color used for hyperlinks.</span></span> <span data-ttu-id="17764-518">Kann für andere Zwecke verwendet werden, in denen die Farbe einen Link zu anderen Informationen bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="17764-518">May be used for other purposes where the color denotes a link to other information.</span></span> |
| <span data-ttu-id="17764-519">7</span><span class="sxs-lookup"><span data-stu-id="17764-519">7</span></span>     | <span data-ttu-id="17764-520">Schema. gefolgt</span><span class="sxs-lookup"><span data-stu-id="17764-520">scheme.followed</span></span>   | <span data-ttu-id="17764-521">Link zu Akzent und gefolgt</span><span class="sxs-lookup"><span data-stu-id="17764-521">Accent and followed hyperlink</span></span> | <span data-ttu-id="17764-522">Hervorhebungs Farbe für verfolgte Hyperlinks; auch für "rückwärts"-Links geeignet.</span><span class="sxs-lookup"><span data-stu-id="17764-522">Highlight color for followed hyperlinks; also appropriate for "backwards" links.</span></span>                                         |



 

<span data-ttu-id="17764-523">Auf eine Schema Farbe kann entweder anhand des Namens oder des Indexes verwiesen werden. Daher weisen "Schema. Fill" und "Schema (4)" dieselbe Farbe auf.</span><span class="sxs-lookup"><span data-stu-id="17764-523">A scheme color may be referred to either by name or by index, thus scheme.fill and scheme(4) are the same color.</span></span>

<span data-ttu-id="17764-524">Schema Farben werden nicht am Standardschema beteiligt, wenn keine Farbe angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="17764-524">Scheme colors do not participate in the defaulting scheme if a color is not specified.</span></span> <span data-ttu-id="17764-525">Eine nicht angegebene Füll Farbe muss immer als weiß interpretiert werden, unabhängig von der Farbe der Schema Farbe 4.</span><span class="sxs-lookup"><span data-stu-id="17764-525">An unspecified fill color must always be interpreted as white, regardless of the color of scheme color 4.</span></span> <span data-ttu-id="17764-526">Die "Akzent"-Farben sollten sowohl mit dem Hintergrund (0) als auch mit den Füll Farben (4) im Gegensatz zu Text-und Titel Textfarben die gleiche Eigenschaft aufweisen.</span><span class="sxs-lookup"><span data-stu-id="17764-526">The "accent" colors should contrast with both the background (0) and the fill (4) colors, and text and title text colors should have the same property.</span></span> <span data-ttu-id="17764-527">Ein Standardverfahren besteht darin, die Akzente zu färben und den Standardtext (in der Regel Schwarz oder weiß) zu färben.</span><span class="sxs-lookup"><span data-stu-id="17764-527">One standard technique is to make the accents colored and the standard text uncolored (typically black or white).</span></span>

<span data-ttu-id="17764-528">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="17764-528">[![back to top](images/top.gif) Back to top](#top)</span></span>

### <a name="system-colors"></a><span data-ttu-id="17764-529">System Farben</span><span class="sxs-lookup"><span data-stu-id="17764-529">System colors</span></span>

<span data-ttu-id="17764-530">Anwendungen zeichnen manchmal Farben auf der Grundlage von Betriebs Systemeinstellungen innerhalb von Grafiken auf.</span><span class="sxs-lookup"><span data-stu-id="17764-530">Applications sometimes record colors based on operating system settings within graphics.</span></span> <span data-ttu-id="17764-531">Diese sind normalerweise flüchtig und müssen nicht ausgeschrieben werden. die thesystemcolor-Definitionen sind nur zur Unterstützung dieser Funktion vorhanden.</span><span class="sxs-lookup"><span data-stu-id="17764-531">Normally these are transient and need not be written out; thesystemcolor definitions exist solely to support this.</span></span> <span data-ttu-id="17764-532">Eine System Farbe wird eingeführt, indem ein entsprechendes Tag in einem neuen Namespace definiert und die entsprechenden Informationen in den Element Inhalt eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="17764-532">A system color is introduced by defining an appropriate tag in a new namespace and inserting the appropriate information in the element content.</span></span>

<span data-ttu-id="17764-533">Dieser Vorschlag definiert ein derartiges Tag, um die Windows-Benutzeroberflächen Farben zu codieren, die in der Header Datei "Winuser. h" definiert sind.</span><span class="sxs-lookup"><span data-stu-id="17764-533">This proposal defines such a tag to encode the Windows user interface colors defined in the winuser.h header file.</span></span>


```HTML
win.color
<!element win.color #pcdata>
```



<span data-ttu-id="17764-534">Der Inhalt des-Elements ist eine einzelne ganze Zahl, die den Wert der relevanten Farb \_ Definition aus Winuser. h enthält.</span><span class="sxs-lookup"><span data-stu-id="17764-534">The content of the element is a single integer which contains the value of the relevant COLOR\_ define from winuser.h.</span></span> <span data-ttu-id="17764-535">Eine ähnliche Technik kann für jede System-oder anwendungsspezifische Farbspezifikation übernommen werden.</span><span class="sxs-lookup"><span data-stu-id="17764-535">A similar technique can be adopted for any system- or application-specific color specification.</span></span> <span data-ttu-id="17764-536">Es wird dringend empfohlen, dieses Feature nur aus Gründen der Abwärtskompatibilität zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="17764-536">It is strongly recommended that this feature be used only for backward compatibility.</span></span>

<span data-ttu-id="17764-537">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="17764-537">[![back to top](images/top.gif) Back to top](#top)</span></span>

### <a name="pure-colors"></a><span data-ttu-id="17764-538">Reine Farben</span><span class="sxs-lookup"><span data-stu-id="17764-538">Pure colors</span></span>


```HTML
pure
<!elementpure empty>
```



<span data-ttu-id="17764-539">Wenn das Element <pure/> in einem Farbwert angezeigt wird, ist dies ein Hinweis darauf, dass die Farbe nicht durch ein Dithering-Muster angeblendet werden sollte.</span><span class="sxs-lookup"><span data-stu-id="17764-539">If the element <pure/> appears in a color value, it is a hint that the color should not be approximated by a dither pattern.</span></span> <span data-ttu-id="17764-540">Dies ist eine Funktion der Ebene 1, und eine konforme Implementierung muss Sie nicht berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="17764-540">This is a level 1 feature, and a conforming implementation need not honor it.</span></span> <span data-ttu-id="17764-541">Die Bezeichnung ist wichtig für Grafiken, die auf Geräten mit mittlerer Auflösung angezeigt werden, wie z. b. Video anzeigen, bei denen kleine Features (z. b. Zeilen) ein ungültiges Aliasing mit Dithering-Farben verursachen können</span><span class="sxs-lookup"><span data-stu-id="17764-541">The designation is important for graphics displayed on medium-resolution devices, such as video displays, where small features (such as lines) may cause bad aliasing with dithered colors.</span></span> <span data-ttu-id="17764-542">Auf Geräten wie Druckern, die normalerweise alle Farben außer den wenigen vollständig übersättigten Farben unterscheiden, ist das Dithering normalerweise ausreichend gut, um dieses Problem zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="17764-542">On devices such as printers, which normally dither all colors except for the few fully saturated colors, the dithering is normally sufficiently fine to avoid this problem.</span></span>

<span data-ttu-id="17764-543">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="17764-543">[![back to top](images/top.gif) Back to top](#top)</span></span>

### <a name="color-adjustments"></a><span data-ttu-id="17764-544">Farbanpassungen</span><span class="sxs-lookup"><span data-stu-id="17764-544">Color adjustments</span></span>

<span data-ttu-id="17764-545">Die Basis Farbe kann durch arithmetische Operationen für den RGB-Wert angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="17764-545">The base color may be adjusted by arithmetic operations on the RGB value.</span></span> <span data-ttu-id="17764-546">Diese Vorgänge werden mithilfe zusätzlicher Elemente innerhalb des Farbwerts definiert.</span><span class="sxs-lookup"><span data-stu-id="17764-546">These operations are defined using additional elements within the color value.</span></span> <span data-ttu-id="17764-547">Solche Anpassungen sind nur hilfreich, wenn Sie auf von anderen Elementen abgeleitete Farben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="17764-547">Such adjustments are useful only when applied to colors derived from other elements.</span></span> <span data-ttu-id="17764-548">Es ist zulässig, eine solche Anpassung für einen Wert mit fester Farbe anzugeben. Allerdings ist es für eine Implementierung zulässig, dies auf den entsprechenden RGB-Wert zu reduzieren und anstelle des Originals zu speichern.</span><span class="sxs-lookup"><span data-stu-id="17764-548">It is valid to specify such an adjustment on a fixed color value; however, an implementation is permitted to reduce this to the corresponding RGB value and store that instead of the original.</span></span>

<span data-ttu-id="17764-549">Alle in diesem Abschnitt beschriebenen Farb Anpassungs Features sind Features der Ebene 1.</span><span class="sxs-lookup"><span data-stu-id="17764-549">All the color adjustment features described in this section are level 1 features.</span></span>


```HTML
color.adjustment
<!entity % color.adjustment  -- change to make to a color --
  "( %color.op; )?, ( %color.adj; )*"
>

color.op
<!entity % color.op          -- arithmetic operation --
  "( darken | lighten | add | subtract | reverseSubtract |
  blackWhite )"
>
<!element   darken           %color.parameter;>
<!element   lighten          %color.parameter;>
<!element   add              %color.parameter;>
<!element   subtract         %color.parameter;>
<!element   reversesubtract  %color.parameter;>
<!element   blackwhite       %color.parameter;>

color.parameter
<!entity % color.parameter  "#pcdata" >

color.adj
<!entity % color.adj          -- additional adjustment to color --
  "invert | invert128 | gray"
>
<!element   invert       empty>
<!element   INVERT128    empty>
<!element   gray         empty>
```



<span data-ttu-id="17764-550">Der-Parameter der ersten sechs Vorgänge ist ein einzelner ganzzahliger numerischer Wert im Bereich von 0 bis 255.</span><span class="sxs-lookup"><span data-stu-id="17764-550">The parameter of the first six operations is a single integral numeric value in the range 0 to 255.</span></span> <span data-ttu-id="17764-551">Die Anpassung wird wie folgt für den 3x8bit-RGB-Wert durchgeführt:</span><span class="sxs-lookup"><span data-stu-id="17764-551">The adjustment is performed on the 3x8bit RGB value as follows:</span></span>

1.  <span data-ttu-id="17764-552">Wenn <gray/> angegeben wird, wird der RGB-Wert durch yyy ersetzt, wobei y der Wert für die Leuchtkraft (y) ist, der aus dem sRGB-Wert in folgendem Wert von "ITU-r BT. 709" berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="17764-552">If <gray/> is specified, the RGB value is replaced by yyy, where y is the luminance (y') value calculated from the sRGB value in following the ITU-r BT.709.</span></span> <span data-ttu-id="17764-553">Diese Berechnung lautet:</span><span class="sxs-lookup"><span data-stu-id="17764-553">This calculation is:</span></span>
    ```HTML
    y = 0 2125xr + 0 7154xg + 0 0721xb
    ```

    

2.  <span data-ttu-id="17764-554">Wenn eine Color. op-Änderung angegeben wird, wird jede Komponente entsprechend der nachfolgenden Tabelle separat angepasst.</span><span class="sxs-lookup"><span data-stu-id="17764-554">If a color.op modification is given, each component is separately adjusted according to the table below.</span></span> <span data-ttu-id="17764-555">c ist der Komponenten Wert, und p ist der Color. Parameter-Wert.</span><span class="sxs-lookup"><span data-stu-id="17764-555">c is the component value, and p is the color.parameter value.</span></span>

    | <span data-ttu-id="17764-556">Vorgang</span><span class="sxs-lookup"><span data-stu-id="17764-556">Operation</span></span>       | <span data-ttu-id="17764-557">Formel</span><span class="sxs-lookup"><span data-stu-id="17764-557">Formula</span></span>                            |
    |-----------------|------------------------------------|
    | <span data-ttu-id="17764-558">Abdunkeln</span><span class="sxs-lookup"><span data-stu-id="17764-558">darken</span></span>          | <span data-ttu-id="17764-559">c: = CXP/255</span><span class="sxs-lookup"><span data-stu-id="17764-559">c := cxp/255</span></span>                       |
    | <span data-ttu-id="17764-560">aufgehellt</span><span class="sxs-lookup"><span data-stu-id="17764-560">lighten</span></span>         | <span data-ttu-id="17764-561">c: = 255-(255-c) XP/255</span><span class="sxs-lookup"><span data-stu-id="17764-561">c := 255 - (255-c)xp/255</span></span>           |
    | <span data-ttu-id="17764-562">add</span><span class="sxs-lookup"><span data-stu-id="17764-562">add</span></span>             | <span data-ttu-id="17764-563">c: = c + p</span><span class="sxs-lookup"><span data-stu-id="17764-563">c := c + p</span></span>                         |
    | <span data-ttu-id="17764-564">Subtrahieren</span><span class="sxs-lookup"><span data-stu-id="17764-564">subtract</span></span>        | <span data-ttu-id="17764-565">c: = c-p</span><span class="sxs-lookup"><span data-stu-id="17764-565">c := c - p</span></span>                         |
    | <span data-ttu-id="17764-566">reversesubtract</span><span class="sxs-lookup"><span data-stu-id="17764-566">reversesubtract</span></span> | <span data-ttu-id="17764-567">c: = p-c</span><span class="sxs-lookup"><span data-stu-id="17764-567">c := p - c</span></span>                         |
    | <span data-ttu-id="17764-568">BlackWhite</span><span class="sxs-lookup"><span data-stu-id="17764-568">blackwhite</span></span>      | <span data-ttu-id="17764-569">Wenn c < p thenc: = 0elsec: = 255</span><span class="sxs-lookup"><span data-stu-id="17764-569">if c < p thenc := 0elsec := 255</span></span> |

    

     

    <span data-ttu-id="17764-570">In jedem Fall, wenn der berechnete Komponenten Wert c den Wert 255 überschreitet, wird 255 verwendet, und wenn der Wert kleiner als 0 ist, wird 0 verwendet.</span><span class="sxs-lookup"><span data-stu-id="17764-570">In each case, if the calculated component value, c, exceeds 255, then 255 is used, and if it is less than 0, then 0 is used.</span></span>

3.  <span data-ttu-id="17764-571">Wenn <INVERT128/> angegeben wird, wird der Wert 128 subtrahiert oder jeder Komponente hinzugefügt, je nachdem, ob die Komponente kleiner als 128 ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="17764-571">If <INVERT128/> is given, the value 128 is subtracted or added to each component according to whether the component is less than 128 or not.</span></span>
    ```HTML
    if c < 128
        then
       c := c + 128
    else
       c := c - 128
    ```

    

4.  <span data-ttu-id="17764-572">Wenn <invert/> angegeben wird, wird jede Komponente durch 255 abzüglich des Werts der Komponente ersetzt.</span><span class="sxs-lookup"><span data-stu-id="17764-572">If <invert/> is given, each component is replaced by 255 minus the value of the component.</span></span>
    ```HTML
    c := 255-c
    ```

    

<span data-ttu-id="17764-573">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="17764-573">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="font"></a><span data-ttu-id="17764-574">font</span><span class="sxs-lookup"><span data-stu-id="17764-574">font</span></span>


```HTML
font
<!element font any>
<!attlist font 
   style     cdata  #implied>
```



<span data-ttu-id="17764-575">Eine Schriftart wird mithilfe eines style-Attributs identifiziert, wie in [CSS1 section 5,2 (Schriftart Eigenschaften)](https://www.w3.org/pub/WWW/TR/REC-CSS1#font-properties) definiert.</span><span class="sxs-lookup"><span data-stu-id="17764-575">A font is identified using a style attribute as defined in [CSS1 section 5.2 (font properties)](https://www.w3.org/pub/WWW/TR/REC-CSS1#font-properties) .</span></span> <span data-ttu-id="17764-576">Der Text des Schriftart Elements ist derzeit nicht definiert, kann aber in Zukunft verwendet werden, um Standard Schriftart Informationen zu codieren.</span><span class="sxs-lookup"><span data-stu-id="17764-576">The body of the font element is, at present, undefined but may be used in the future to encode standard font information.</span></span> <span data-ttu-id="17764-577">Anfängliche Implementierungen dieses Vorschlags sollten die Informationen beibehalten, aber nicht interpretieren.</span><span class="sxs-lookup"><span data-stu-id="17764-577">Initial implementations of this proposal should preserve but not interpret the information.</span></span>

<span data-ttu-id="17764-578">Es ist zu beachten, dass in der Zukunft Unterstützung für Out-of-Line-Schriftart Informationen (herunterladbare Schriftarten oder freigegebene Schriftart Ressourcen) hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="17764-578">It is conceivable that support will be added in the future for out-of-line font information (downloadable fonts, or shared font resources).</span></span> <span data-ttu-id="17764-579">Dies erfolgt durch ein XML-Link-Element innerhalb des Inhalts des Font-Elements, wodurch die Abwärtskompatibilität mit anfänglichen Implementierungen sichergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="17764-579">This will be done by an XML-link element within the content of the font element, ensuring backward compatbility with initial implementations.</span></span>

<span data-ttu-id="17764-580">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="17764-580">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="bitmap"></a><span data-ttu-id="17764-581">Bitmap</span><span class="sxs-lookup"><span data-stu-id="17764-581">bitmap</span></span>


```HTML
bitmap
<!element   bitmap   empty>
<!attlist   bitmap
   XML-link    cdata               #fixed "simple"
   href        cdata               #REQUIRED
   title       cdata               #implied
   behavior    cdata               #implied
   show        (embed|replace|new) #fixed "embed"
   inline      (true|false)        #fixed "true"
   actuate     (auto|user)         #fixed "auto"
>
```



<span data-ttu-id="17764-582">Das Bitmap-Element ermöglicht einen Verweis auf eine Out-of-Line-Bildressource (normalerweise eine Bitmap), die in einer Grafik enthalten sein soll.</span><span class="sxs-lookup"><span data-stu-id="17764-582">The bitmap element allows a reference to an out-of-line picture resource (normally a bitmap) to be included in a graphic.</span></span>

<span data-ttu-id="17764-583">Bitmap ist eine Funktion der Ebene 1.</span><span class="sxs-lookup"><span data-stu-id="17764-583">bitmap is a level 1 feature.</span></span>

<span data-ttu-id="17764-584">Das Behavior-Attribut kann verwendet werden, um anzugeben, wie die Bitmap von einer Bearbeitungs Anwendung behandelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="17764-584">The behavior attribute may be used to indicate how the bitmap should be handled by an editing application.</span></span> <span data-ttu-id="17764-585">Der Wert kann eines oder beide der folgenden Token sein.</span><span class="sxs-lookup"><span data-stu-id="17764-585">The value may be one or both of the following tokens.</span></span>



| <span data-ttu-id="17764-586">Token</span><span class="sxs-lookup"><span data-stu-id="17764-586">Token</span></span>    | <span data-ttu-id="17764-587">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="17764-587">Description</span></span>                                                                                                                                                                                                                                                                             |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17764-588">gesondert</span><span class="sxs-lookup"><span data-stu-id="17764-588">separate</span></span> | <span data-ttu-id="17764-589">Markiert die Bitmap als separate Entität, die nicht als integraler Bestandteil des Dokuments angesehen werden sollte.</span><span class="sxs-lookup"><span data-stu-id="17764-589">Marks the bitmap as a separate entity, which should not be regarded as an integral part of the document.</span></span> <span data-ttu-id="17764-590">Die Bitmap sollte nicht im Dokument aufbewahrt werden.</span><span class="sxs-lookup"><span data-stu-id="17764-590">The bitmap should not be kept with the document.</span></span> <span data-ttu-id="17764-591">Wenn das Dokument kopiert wird, sollte die Bitmap nicht kopiert werden. Wenn das Dokument verschoben wird, sollte die Bitmap nicht mit dem Dokument verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="17764-591">If the document is copied, the bitmap should not be copied; if the document is moved, the bitmap should not be moved with it.</span></span> |
| <span data-ttu-id="17764-592">original</span><span class="sxs-lookup"><span data-stu-id="17764-592">original</span></span> | <span data-ttu-id="17764-593">Das Title-Attribut identifiziert den ursprünglichen Speicherort der Bitmap als URL. Andernfalls wird die Bedeutung von Title nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="17764-593">The title attribute identifies the original location of the bitmap as a URL; otherwise, the meaning of title is not specified.</span></span>                                                                                                                                                          |



 

<span data-ttu-id="17764-594">Diese Werte sind beide Hinweise zum erwarteten Verhalten.</span><span class="sxs-lookup"><span data-stu-id="17764-594">These values are both hints as to the expected behavior.</span></span> <span data-ttu-id="17764-595">Die separate Option bezieht sich auf das Verhalten der Daten, auf die von href verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="17764-595">The separate option refers to the behavior of the data referred to by href.</span></span> <span data-ttu-id="17764-596">Wenn sowohl "separat" als auch "Original" angegeben sind, wird erwartet, dass die Anwendung den href-URI ignoriert und die Bitmap aus den ursprünglichen Daten neu generiert.</span><span class="sxs-lookup"><span data-stu-id="17764-596">If both separate and original are given, the application is expected to disregard the href URI and regenerate the bitmap from the original data.</span></span> <span data-ttu-id="17764-597">Wenn nur "Original" angegeben wird, wird davon ausgegangen, dass die Anwendung den href-URI verwendet, um die Bitmap zu suchen, aber dem Benutzer die Möglichkeit gibt, Sie erneut zu generieren.</span><span class="sxs-lookup"><span data-stu-id="17764-597">If only original is given, the application is expected to use the href URI to find the bitmap but may give the user the option of regenerating it.</span></span>

<span data-ttu-id="17764-598">Es ist zulässig, dass der href-URI und das Title-Attribut denselben (lexikalischen) Wert haben. Dies ist angemessen, wenn die referenzierte Bitmap nicht "gespeichert mit" dem Dokument ist.</span><span class="sxs-lookup"><span data-stu-id="17764-598">It is valid to make the href URI and the title attribute the same (lexical) value -- this is appropriate if the referenced bitmap is not "stored with" the document.</span></span> <span data-ttu-id="17764-599">Es ist (obwohl nicht erforderlich), dass href für die eigene Kopie der Bitmap des Dokuments verwendet wird. diese kann gelöscht werden, wenn die verweisenden Formen gelöscht werden, und dieser Titel wird verwendet, um eine freigegebene Kopie anzugeben.</span><span class="sxs-lookup"><span data-stu-id="17764-599">It is intended (though not required) that href be used for the document's own copy of the bitmap -- which may be deleted if the referencing shapes are deleted -- and that title be used to indicate a shared copy.</span></span> <span data-ttu-id="17764-600">Wenn beide denselben Wert enthalten, gibt es daher keine Dokument spezifische Kopie.</span><span class="sxs-lookup"><span data-stu-id="17764-600">Thus, if both contain the same value there is no document-specific copy.</span></span>

<span data-ttu-id="17764-601">Anwendungen ignorieren den Hinweis möglicherweise, wenn er nicht in das tatsächliche Speichermodell der XML-Daten passt.</span><span class="sxs-lookup"><span data-stu-id="17764-601">Applications may disregard the hint if it does not fit in with the actual storage model of the XML data.</span></span>

<span data-ttu-id="17764-602">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="17764-602">[![back to top](images/top.gif) Back to top](#top)</span></span>

### <a name="picture-file-formats"></a><span data-ttu-id="17764-603">Bild Dateiformate</span><span class="sxs-lookup"><span data-stu-id="17764-603">Picture file formats</span></span>

<span data-ttu-id="17764-604">Im Zusammenhang mit diesem Vorschlag sind externe Daten entweder eine Bitmap oder eine Datei, die zum Herstellen einer Bitmap verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="17764-604">Within the context of this proposal, external data is invariably either a bitmap or a file which is used to produce a bitmap.</span></span> <span data-ttu-id="17764-605">Auf renderebene 0 muss kein externes Bitmap-Format unterstützt werden--Pfade können nur mit voll Tonfarben gefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="17764-605">At render level 0, no external bitmap format need be supported -- paths may only be filled with solid colors.</span></span> <span data-ttu-id="17764-606">Bitmaps müssen unterstützt werden, um den vollständigen Satz von Füllungen der Rendering-Ebene 1 zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="17764-606">To render the full set of render level 1 fills, bitmaps need to be supported.</span></span> <span data-ttu-id="17764-607">Renderstufe 1 umfasst nur die folgenden Formate:</span><span class="sxs-lookup"><span data-stu-id="17764-607">Render level 1 includes (only) the following formats:</span></span>

1.  <span data-ttu-id="17764-608">Jff, d. h. ISO/IEC 10918 Formatierungsdaten, die in eine Datei mit dem JFI-Header eingebettet sind (die nach dem Soi-Ersteller als bestimmter APP0 Marker angesehen werden können) und einschließen (nur) den Bereich von JPEG-Formaten, die vom IJG V6-Code unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="17764-608">JFIF, i.e. ISO/IEC 10918 format data embedded within a file with the JFIF header (which may be regarded as a particular APP0 marker after the SOI maker) and including (only) the range of JPEG formats supported by the IJG v6 code.</span></span>
2.  <span data-ttu-id="17764-609">PNG, gemäß der Spezifikation der PNG-Version 1,0.</span><span class="sxs-lookup"><span data-stu-id="17764-609">PNG, as defined by the PNG version 1.0 specification.</span></span>

<span data-ttu-id="17764-610">Die Rendering-Ebene 2 bietet auch Unterstützung für Folgendes:</span><span class="sxs-lookup"><span data-stu-id="17764-610">Render level 2 also includes support for the following:</span></span>

-   <span data-ttu-id="17764-611">GIF, wie von der von Compuserv in 1987 veröffentlichten GIF-Spezifikation (normalerweise als "GIF87a" bezeichnet) definiert.</span><span class="sxs-lookup"><span data-stu-id="17764-611">GIF, as defined by the GIF specification published by CompuServ in 1987 (normally referred to as "GIF87a").</span></span> <span data-ttu-id="17764-612">GIF89a muss auch auf dieser Ebene unterstützt werden, unterliegt der Einschränkung, dass die Daten keine Erweiterungs Blöcke enthalten dürfen, die eine Interpretation benötigen, um die Bitmap außer der Grafik Steuerelement-extensionswithouta-Anforderung für eine Benutzereingabe oder eine Verzögerungszeit anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="17764-612">GIF89a must also be supported at this level, subject to the restriction that the data must not contain any extension blocks that need interpretation to display the bitmap other than graphics control extensionswithouta requirement for user input or a delay time.</span></span> <span data-ttu-id="17764-613">Dies ermöglicht das Einschließen von Kommentaren, jedoch nicht die nur-Text-Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="17764-613">This allows comments to be included, but not the plain text extension.</span></span> <span data-ttu-id="17764-614">Eine Anwendung kann Anwendungs Erweiterungen (0x21, 0xFF) einfügen, aber mit der Terminologie dieses Vorschlags dürfen diese nur die Bearbeitung, nicht das Rendering und Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="17764-614">An application may insert application (0x21, 0xFF) extensions but, using the terminology of this proposal, these must contain only editing, not rendering, data.</span></span>

<span data-ttu-id="17764-615">Jedes andere Datenformat, das in der Grafik verwendet wird, erzwingt, dass diese Grafik mindestens die Bearbeitungs Ebene 3 und möglicherweise die Renderingebene Ebene 3 (wenn die Daten zum Rendern der Grafik erforderlich sind).</span><span class="sxs-lookup"><span data-stu-id="17764-615">Any other data format used in the graphic forces that graphic to be at least editing level 3 and possibly rendering level 3 (if the data is necessary to render the graphic).</span></span> <span data-ttu-id="17764-616">Es wird empfohlen, die unterstützten Formate zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="17764-616">An application is encouraged to publish the formats which it supports.</span></span> <span data-ttu-id="17764-617">Microsoft Office unterstützt z. b. die folgenden zusätzlichen Formate nativ und kann daher Bearbeitungsdaten in dieser Form schreiben:</span><span class="sxs-lookup"><span data-stu-id="17764-617">For example, Microsoft Office supports the following additional formats natively and may therefore write editing data in this form:</span></span>

1.  <span data-ttu-id="17764-618">WMF--Windows-Metadatei (Win 3,1-Format)</span><span class="sxs-lookup"><span data-stu-id="17764-618">WMF -- Windows metafile (Win 3.1 format)</span></span>
2.  <span data-ttu-id="17764-619">EMF--Windows "Enhanced"-Metadatei (Win32-Format)</span><span class="sxs-lookup"><span data-stu-id="17764-619">EMF -- Windows "enhanced" metafile (Win32 format)</span></span>
3.  <span data-ttu-id="17764-620">PICT-Mac OS QuickDraw-PICT-Datei (alle Versionen, aber ohne QuickTime-Einträge oder andere Erweiterungen)</span><span class="sxs-lookup"><span data-stu-id="17764-620">PICT -- Mac OS QuickDraw PICT file (all versions but with no QuickTime records or other extensions)</span></span>
4.  <span data-ttu-id="17764-621">BMP--Windows-Bitmap-Dateiformat, "OS/2" (bitmapcore), BitmapInfo, BITMAPV4 und BITMAPV5 Formate</span><span class="sxs-lookup"><span data-stu-id="17764-621">BMP -- Windows bitmap file format, "os/2" (BITMAPCORE), BITMAPINFO, BITMAPV4, and BITMAPV5 formats</span></span>

<span data-ttu-id="17764-622">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="17764-622">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="vector"></a><span data-ttu-id="17764-623">Vektor</span><span class="sxs-lookup"><span data-stu-id="17764-623">vector</span></span>


```HTML
v
<!element v "( #pcdata | p )*">
```



<span data-ttu-id="17764-624">Ein Vektorgrafik Pfad wird als "pcdata" codiert.</span><span class="sxs-lookup"><span data-stu-id="17764-624">A vector graphic path is encoded as pcdata.</span></span> <span data-ttu-id="17764-625">Der Inhalt des v-Elements wird gemischt und enthält eine Vektor Pfad Beschreibung, die optional mit p-Elementen parametrisiert wird.</span><span class="sxs-lookup"><span data-stu-id="17764-625">The content of the v element is mixed, containing a vector path description optionally parameterized with p elements.</span></span>

[<span data-ttu-id="17764-626">Zurück zur VML-Übersicht</span><span class="sxs-lookup"><span data-stu-id="17764-626">Back to the VML overview</span></span>](web-workshop---specs---standards----how-to-use-vml-on-web-pages.md)

 

