---
title: HTML-Zwischenablage Format
description: In diesem Abschnitt wird das HTML-Zwischenablage Format erläutert.
ms.assetid: e891393f-234f-4c94-b581-c4e5f885d2ab
keywords:
- Windows-Benutzeroberfläche, Zwischenablage
- Zwischenablage, Daten werden abgeschnitten
- Zwischenablage, Kopieren von Daten
- Zwischenablage, Einfügen von Daten
- Zwischenablage, Formate
- Zwischenablage, HTML-Format
- Zwischenablage, HTML-Text wird abgeschnitten
- Zwischenablage, Einfügen von HTML-Text
- CF_HTML Format der Zwischenablage
- Zwischenablage, CF_HTML Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75cdcd9c2fc982a7cbde38bba4b7dec6738f1793
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037135"
---
# <a name="html-clipboard-format"></a><span data-ttu-id="5390b-113">HTML-Zwischenablage Format</span><span class="sxs-lookup"><span data-stu-id="5390b-113">HTML Clipboard Format</span></span>

<span data-ttu-id="5390b-114">Die Anforderungen für die Übertragung von HTML-Text mithilfe der Zwischenablage unterscheiden sich je nach Szenario.</span><span class="sxs-lookup"><span data-stu-id="5390b-114">The requirements for transferring HTML text by means of the clipboard differ depending on scenario.</span></span> <span data-ttu-id="5390b-115">In diesem Artikel geht es um das Ausschnitten und Einfügen von Fragmenten eines HTML-Dokuments.</span><span class="sxs-lookup"><span data-stu-id="5390b-115">This article is concerned with cutting and pasting fragments of an HTML document.</span></span> <span data-ttu-id="5390b-116">Möglicherweise gibt es Anforderungen zum übertragen ganzer HTML-Dokumente über die Zwischenablage. Dieser Artikel wird jedoch durch eine Anforderung zum Übertragen von Fragmenten aus ausgewähltem HTML-Text gesteuert.</span><span class="sxs-lookup"><span data-stu-id="5390b-116">There may be requirements for transferring entire HTML documents through the clipboard; however, this article is driven by a requirement to transfer fragments of selected HTML text.</span></span> <span data-ttu-id="5390b-117">Eine Methode, die erfordert, dass das gesamte HTML-Dokument in die Zwischenablage kopiert wird, wird daher als zu schwer zu schwer zu betrachten.</span><span class="sxs-lookup"><span data-stu-id="5390b-117">As such, a method that required the entire HTML document to be copied to the clipboard is seen as too heavyweight.</span></span>

<span data-ttu-id="5390b-118">Das Format der CF \_ -HTML-Zwischenablage ermöglicht, dass ein Fragment von unformatiertem HTML-Text und dessen Kontext als ASCII in der Zwischenablage gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="5390b-118">The CF\_HTML clipboard format allows a fragment of raw HTML text and its context to be stored on the clipboard as ASCII.</span></span> <span data-ttu-id="5390b-119">Dies ermöglicht es, dass der Kontext des HTML-Fragments, der aus allen vorangehenden umgebenden Tags besteht, von einer Anwendung überprüft werden muss, damit die umgebenden Tags des HTML-Fragments mit ihren Attributen vermerkt werden können.</span><span class="sxs-lookup"><span data-stu-id="5390b-119">This allows the context of the HTML fragment, which consists of all preceding surrounding tags, to be examined by an application so that the surrounding tags of the HTML fragment can be noted with their attributes.</span></span> <span data-ttu-id="5390b-120">Obwohl es Anwendungen gibt, wie solche Fragmente interpretiert werden können, sind hier einige grundlegende Richtlinien auf der Grundlage von IE4-/MSHTML-Implementierungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="5390b-120">Although it is up to applications to decide how to interpret such fragments, some basic guidelines are included here based on IE4/MSHTML implementations.</span></span>

<span data-ttu-id="5390b-121">Der offizielle Name der Zwischenablage (die von RegisterClipboardFormat verwendete Zeichenfolge) ist das HTML-Format.</span><span class="sxs-lookup"><span data-stu-id="5390b-121">The official name of the clipboard (the string used by RegisterClipboardFormat) is HTML Format.</span></span>

-   [<span data-ttu-id="5390b-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5390b-122">Description</span></span>](#description)
-   [<span data-ttu-id="5390b-123">Szenarios</span><span class="sxs-lookup"><span data-stu-id="5390b-123">Scenarios</span></span>](#scenarios)

## <a name="description"></a><span data-ttu-id="5390b-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5390b-124">Description</span></span>

<span data-ttu-id="5390b-125">CF \_ HTML ist vollständig Text formatiert (unter anderem im HTML-Geist, und verwendet UTF-8) und enthält eine `description` , eine optionale und `context` im Kontext der `fragment` .</span><span class="sxs-lookup"><span data-stu-id="5390b-125">CF\_HTML is entirely text format (to be, among other things, in the HTML spirit, and uses UTF-8) and includes a `description`, an optional `context`, and, within the context, the `fragment`.</span></span>

<span data-ttu-id="5390b-126">Im folgenden finden Sie ein Beispiel für eine Zwischenablage:</span><span class="sxs-lookup"><span data-stu-id="5390b-126">The following is an example of a clipboard:</span></span>


```
Version:0.9
    StartHTML:71
    EndHTML:170
    StartFragment:140
    EndFragment:160
    StartSelection:140
    EndSelection:160
    <!DOCTYPE>
    <HTML>
    <HEAD>
    <TITLE> The HTML Clipboard</TITLE>
    <BASE HREF="https://sample/specs">
    </HEAD>
    <BODY>
    <UL>
    <!--StartFragment -->
    <LI> The Fragment </LI>
    <!--EndFragment -->
    </UL>
    </BODY>
    </HTML>
```



<span data-ttu-id="5390b-127">Die Beschreibung enthält die Versionsnummer und Offsets der Zwischenablage, die angeben, wo der Kontext und das Fragment beginnen und enden.</span><span class="sxs-lookup"><span data-stu-id="5390b-127">The description includes the clipboard version number and offsets, indicating where the context and the fragment start and end.</span></span> <span data-ttu-id="5390b-128">Die Beschreibung ist eine Liste von ASCII-Text Schlüsselwörtern (min/Maj ist nicht aussagekräftig), gefolgt von einer Zeichenfolge und getrennt durch einen Doppelpunkt (:).</span><span class="sxs-lookup"><span data-stu-id="5390b-128">The description is a list of ASCII text keywords (min/maj is not meaningful) followed by a string and separated by a colon (:).</span></span>

<span data-ttu-id="5390b-129">**Version**: die Versionsnummer der Zwischenablage.</span><span class="sxs-lookup"><span data-stu-id="5390b-129">**Version**: vv version number of the clipboard.</span></span> <span data-ttu-id="5390b-130">Die Start Version ist 0,9.</span><span class="sxs-lookup"><span data-stu-id="5390b-130">Starting version is 0.9.</span></span>

<span data-ttu-id="5390b-131">**StartHTML**: byteCount vom Anfang der Zwischenablage bis zum Anfang des Kontexts oder-1, wenn kein Kontext angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5390b-131">**StartHTML**: bytecount from the beginning of the clipboard to the start of the context, or -1 if no context.</span></span>

<span data-ttu-id="5390b-132">**EndHTML**: byteCount vom Anfang der Zwischenablage bis zum Ende des Kontexts oder-1, wenn kein Kontext angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5390b-132">**EndHTML**: bytecount from the beginning of the clipboard to the end of the context, or -1 if no context.</span></span>

<span data-ttu-id="5390b-133">**StartFragment**: byteCount vom Anfang der Zwischenablage bis zum Anfang des Fragments.</span><span class="sxs-lookup"><span data-stu-id="5390b-133">**StartFragment**: bytecount from the beginning of the clipboard to the start of the fragment.</span></span>

<span data-ttu-id="5390b-134">**EndFragment**: byteCount vom Anfang der Zwischenablage bis zum Ende des Fragments.</span><span class="sxs-lookup"><span data-stu-id="5390b-134">**EndFragment**: bytecount from the beginning of the clipboard to the end of the fragment.</span></span>

<span data-ttu-id="5390b-135">**Startselection**: byteCount vom Anfang der Zwischenablage bis zum Anfang der Auswahl.</span><span class="sxs-lookup"><span data-stu-id="5390b-135">**StartSelection**: bytecount from the beginning of the clipboard to the start of the selection.</span></span>

<span data-ttu-id="5390b-136">**Endselection**: byteCount vom Anfang der Zwischenablage bis zum Ende der Auswahl.</span><span class="sxs-lookup"><span data-stu-id="5390b-136">**EndSelection**: bytecount from the beginning of the clipboard to the end of the selection.</span></span>

<span data-ttu-id="5390b-137">Die Schlüsselwörter startselection und endselection sind optional und müssen weggelassen werden, wenn Sie nicht möchten, dass die Anwendung diese Informationen generiert.</span><span class="sxs-lookup"><span data-stu-id="5390b-137">The StartSelection and EndSelection keywords are optional and must both be omitted if you do not want the application to generate this information.</span></span>

<span data-ttu-id="5390b-138">Weitere Informationen zu dieser Art können später hinzugefügt werden, da der HTML-Code bei starthtmloffset beginnt.</span><span class="sxs-lookup"><span data-stu-id="5390b-138">Other information of this kind could be added here later, since the HTML starts at the StartHTMLoffset.</span></span> <span data-ttu-id="5390b-139">Beispielsweise könnten später mehrere Paare von StartFragment/EndFragment hinzugefügt werden, um die nicht zusammenhängende Auswahl von Fragmenten zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="5390b-139">For example, multiple pairs of StartFragment / EndFragment could be added later to support noncontiguous selection of fragments.</span></span>

<span data-ttu-id="5390b-140">Um die Vorteile der Programme zu erzeugen, die bytecounts erzeugen, könnte bytecounts von Nullen aufgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="5390b-140">For the convenience of the programs generating the bytecounts, bytecounts could be left padded by zeros.</span></span> <span data-ttu-id="5390b-141">Programme, die die byteCount-Elemente erzeugen, können z. b. willkürlich die zehn (10) Nullen für jedes Schlüsselwort (StartHTML: 0000000000) beeinflussen und dann, wenn die exakte StartHTML-byteCount bekannt ist (z. b. 71), die entsprechende Anzahl der Nullen durch byteCount (StartHTML: 0000000071)</span><span class="sxs-lookup"><span data-stu-id="5390b-141">For example, programs generating the bytecounts could arbitrarily affect ten (10) zeros to each keyword (StartHTML: 0000000000) and then, when the exact StartHTML bytecount is known (say, 71), the program can replace the appropriate number of zeros by the bytecount (StartHTML: 0000000071).</span></span>

<span data-ttu-id="5390b-142">Der einzige Zeichensatz, der von der Zwischenablage unterstützt wird, ist Unicode in der UTF-8-Codierung.</span><span class="sxs-lookup"><span data-stu-id="5390b-142">The only character set supported by the clipboard is Unicode in its UTF-8 encoding.</span></span> <span data-ttu-id="5390b-143">Da die ersten Zeichen von UTF-8 und ASCII Stimmen, ist die Beschreibung immer ASCII, aber die Bytes des Kontexts (beginnend bei StartHTML) können alle anderen Zeichen verwenden, die in UTF-8 codiert sind.</span><span class="sxs-lookup"><span data-stu-id="5390b-143">Because the first characters of UTF-8 and ASCII match, the description is always ASCII, but the bytes of the context (starting at StartHTML) could be using any other characters coded in UTF-8.</span></span>

<span data-ttu-id="5390b-144">Das Zeilenende im Header des Zwischenablage Formats könnte CR, CR/LF oder LF lauten.</span><span class="sxs-lookup"><span data-stu-id="5390b-144">End of lines in the clipboard format header could be CR or CR/LF or LF.</span></span>

<span data-ttu-id="5390b-145">Das Fragment enthält reines, gültiges HTML, das den Bereich darstellt, den der Benutzer ausgewählt hat (z. b. zum Kopieren).</span><span class="sxs-lookup"><span data-stu-id="5390b-145">The fragment contains pure, valid HTML representing the area the user has selected (to Copy, for example).</span></span> <span data-ttu-id="5390b-146">Diese enthält den markierten Text sowie die öffnenden Tags und Attribute eines beliebigen Elements, das über ein Endtag im ausgewählten Text verfügt, sowie Endtags am Ende des Fragments für beliebige Starttags.</span><span class="sxs-lookup"><span data-stu-id="5390b-146">This contains the selected text plus the opening tags and attributes of any element that has an end tag within the selected text, and end tags at the end of the fragment for any start tag included.</span></span> <span data-ttu-id="5390b-147">Dies sind alle Informationen, die für das einfache Einfügen eines HTML-Fragments erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="5390b-147">This is all information required for basic pasting of an HTML fragment.</span></span>

<span data-ttu-id="5390b-148">Dem Fragment sollten die HTML-Kommentare vorangestellt und gefolgt werden.</span><span class="sxs-lookup"><span data-stu-id="5390b-148">The fragment should be preceded and followed by the HTML comments</span></span> <!--StartFragment--> <span data-ttu-id="5390b-149">und</span><span class="sxs-lookup"><span data-stu-id="5390b-149">and</span></span> <!--EndFragment--> <span data-ttu-id="5390b-150">(kein Platz zwischen dem!--und dem Text zulässig), um bequem anzugeben, wo das Fragment beginnt und endet.</span><span class="sxs-lookup"><span data-stu-id="5390b-150">(no space allowed between the !-- and the text) to conveniently indicate where the fragment starts and ends.</span></span> <span data-ttu-id="5390b-151">Daher wird der Beginn und das Ende des Fragments durch das vorhanden sein dieser Kommentare und durch Start Fragment und EndFragment-Byte Anzahl in der Beschreibung angegeben.</span><span class="sxs-lookup"><span data-stu-id="5390b-151">Thus the start and end of the fragment are indicated by the presence of these comments and by StartFragment and EndFragment byte counts in the description.</span></span> <span data-ttu-id="5390b-152">Diese Informationen werden von den Tools erwartet.</span><span class="sxs-lookup"><span data-stu-id="5390b-152">Tools are expected to produce this information.</span></span> <span data-ttu-id="5390b-153">Diese Redundanz wurde eingeführt, um schnell den Anfang des Fragments (aus der Byte Anzahl) zu finden und die Position des Fragments direkt in der HTML-Struktur zu markieren.</span><span class="sxs-lookup"><span data-stu-id="5390b-153">This redundancy has been introduced to be able to rapidly find the start of the fragment (from the byte count) and mark the position of the fragment directly in the HTML tree.</span></span>

<span data-ttu-id="5390b-154">Die Auswahl gibt im Fragment den exakten HTML-Bereich an, den der Benutzer ausgewählt hat (z. b. zum Kopieren).</span><span class="sxs-lookup"><span data-stu-id="5390b-154">The selection indicates inside the fragment the exact HTML area the user has selected (to Copy, for example).</span></span> <span data-ttu-id="5390b-155">Dadurch werden dem Fragment Weitere Informationen hinzugefügt, indem der genaue markierte Text angegeben wird, ohne dass die öffnenden Tags und Endtags hinzugefügt wurden, um sicherzustellen, dass das Fragment wohl geformt ist.</span><span class="sxs-lookup"><span data-stu-id="5390b-155">This adds more information to the fragment by indicating the exact selected text, without the opening tags and end tags that have been added to ensure the fragment is well-formed HTML.</span></span>

<span data-ttu-id="5390b-156">Die Auswahl ist optional, da genügend Informationen im Fragment für das einfache Einfügen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="5390b-156">The selection is optional, as sufficient information is included in the fragment for basic pasting.</span></span> <span data-ttu-id="5390b-157">Wenn die Auswahl nicht gespeichert wird, werden sowohl startselection als auch endselection nicht in der Kopfzeile gespeichert.</span><span class="sxs-lookup"><span data-stu-id="5390b-157">If the selection is not stored, both StartSelection and EndSelection are not stored in the header.</span></span>

<span data-ttu-id="5390b-158">Der Kontext ist ein gültiges, umfassendes HTML-Dokument.</span><span class="sxs-lookup"><span data-stu-id="5390b-158">The context is a valid, complete HTML document.</span></span> <span data-ttu-id="5390b-159">Dieser Artikel enthält das Fragment und alle vorangehenden Tags (Start-und Endtags; diese vorangehenden Tags stellen alle übergeordneten Knoten des Fragments dar, bis zum HTML-Knoten).</span><span class="sxs-lookup"><span data-stu-id="5390b-159">This article contains the fragment and all preceding surrounding tags (start and end tags; these preceding surrounding tags represent all the parent nodes of the fragment, until the HTML node).</span></span> <span data-ttu-id="5390b-160">Der Artikel enthält auch den kompletten Head und ermöglicht das Einschließen der Basis-und Titel Elemente, damit diese zusätzlichen Informationen abgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="5390b-160">The article also contains the complete HEAD, and allows the BASE and TITLE elements, for example, to be included so this additional information can be obtained.</span></span> <span data-ttu-id="5390b-161">Eine Anwendung, die ein HTML-Fragment in die Zwischenablage kopiert, kann ein Basiselement erstellen, das in den Kontext aufgenommen werden soll, wenn ein solches Element nicht bereits vorhanden ist, sodass partielle URLs im Fragment aufgelöst werden können.</span><span class="sxs-lookup"><span data-stu-id="5390b-161">An application copying a fragment of HTML to the clipboard can choose to create a BASE element to include in the context if such an element is not already present so that partial URLs in the fragment can be resolved.</span></span>

<span data-ttu-id="5390b-162">Der Kontext ist optional, da genügend Informationen im Fragment enthalten sind, um ein einfaches Einfügen eines HTML-Fragments durchführen zu können.</span><span class="sxs-lookup"><span data-stu-id="5390b-162">The context is optional, as sufficient information is included in the fragment for basic pasting of an HTML fragment to take place.</span></span> <span data-ttu-id="5390b-163">Wenn der Kontext nicht gespeichert wird, wird nur das Fragment und StartHTML = EndHTML =-1 gespeichert.</span><span class="sxs-lookup"><span data-stu-id="5390b-163">If the context is not stored, the fragment only is stored and the StartHTML=EndHTML=-1.</span></span>

## <a name="scenarios"></a><span data-ttu-id="5390b-164">Szenarien</span><span class="sxs-lookup"><span data-stu-id="5390b-164">Scenarios</span></span>

<span data-ttu-id="5390b-165">In den folgenden Szenarien wird beschrieben, wie der HTML-Editor von IE4/MSHTML HTML-Ausschneiden und Einfügen behandelt. andere Anwendungen können diese Szenarien verwenden oder nicht.</span><span class="sxs-lookup"><span data-stu-id="5390b-165">The following scenarios describe how the IE4/MSHTML HTML editor handles HTML cut and paste; other applications may or may not follow these scenarios.</span></span> <span data-ttu-id="5390b-166">Das hier beschriebene Zwischenablage Format soll Flexibilität bei der Funktionsweise einer Anwendung ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="5390b-166">The clipboard format described here is intended to allow flexibility for how an application chooses to function.</span></span> <span data-ttu-id="5390b-167">(In diesen Szenarien werden nur gute HTML-Code angezeigt, d. h. keine überlappenden Tags.)</span><span class="sxs-lookup"><span data-stu-id="5390b-167">(These scenarios show only good HTML, that is, no overlapping tags.)</span></span>

1.  <span data-ttu-id="5390b-168">Einfaches Fragment von HTML.</span><span class="sxs-lookup"><span data-stu-id="5390b-168">Simple Fragment of HTML.</span></span>
    -   -   <span data-ttu-id="5390b-169">HTML-Text:</span><span class="sxs-lookup"><span data-stu-id="5390b-169">HTML text:</span></span>

            <span data-ttu-id="5390b-170"><BODY>Dies <B>ist normal, wenn dies Fett </B>formatiert ist. Dies wird <I> <B> </B>kursiv</I> formatiert.</BODY></span><span class="sxs-lookup"><span data-stu-id="5390b-170"><BODY>This is normal <B>This is bold </B><I><B>This is bold italic </B>This is italic </I></BODY></span></span>

        -   <span data-ttu-id="5390b-171">Angezeigt als:</span><span class="sxs-lookup"><span data-stu-id="5390b-171">Appears as:</span></span>

            <span data-ttu-id="5390b-172">Dies **ist normal, wenn dies Fett** formatiert ist.    \*    Dies wird kursiv formatiert \*</span><span class="sxs-lookup"><span data-stu-id="5390b-172">This is normal **This is bold**  \***This is bold italic**  This is italic\*</span></span>

        -   <span data-ttu-id="5390b-173">Der Text zwischen \* \* wird ausgewählt und in die Zwischenablage kopiert:</span><span class="sxs-lookup"><span data-stu-id="5390b-173">The text between the \*\* is selected and copied to the clipboard:</span></span>

            <span data-ttu-id="5390b-174">Dies **ist normal, wenn dies fett formatiert** \* \*     \* **ist** und   dieses \* \* \* *kursiv* formatiert ist.</span><span class="sxs-lookup"><span data-stu-id="5390b-174">This is normal **This is** \*\* **bold**   \***This is bold italic**  This\*\*\* *is italic*</span></span>

        -   <span data-ttu-id="5390b-175">Dies erfolgt in der Zwischenablage (Beachten Sie, dass es sich um eine IE4/MSHTML-Interpretation handelt):</span><span class="sxs-lookup"><span data-stu-id="5390b-175">This is what will be on the clipboard (note this is IE4/MSHTML's interpretation):</span></span>

            <span data-ttu-id="5390b-176">Version: 0.9</span><span class="sxs-lookup"><span data-stu-id="5390b-176">Version:0.9</span></span>

            <span data-ttu-id="5390b-177">StartHTML: 71</span><span class="sxs-lookup"><span data-stu-id="5390b-177">StartHTML:71</span></span>

            <span data-ttu-id="5390b-178">EndHTML: 160</span><span class="sxs-lookup"><span data-stu-id="5390b-178">EndHTML:160</span></span>

            <span data-ttu-id="5390b-179">StartFragment: 130</span><span class="sxs-lookup"><span data-stu-id="5390b-179">StartFragment:130</span></span>

            <span data-ttu-id="5390b-180">EndFragment: 150</span><span class="sxs-lookup"><span data-stu-id="5390b-180">EndFragment:150</span></span>

            <span data-ttu-id="5390b-181">**Startselection: 130**</span><span class="sxs-lookup"><span data-stu-id="5390b-181">**StartSelection:130**</span></span>

            <span data-ttu-id="5390b-182">**Endselection: 150**</span><span class="sxs-lookup"><span data-stu-id="5390b-182">**EndSelection:150**</span></span>

            <!DOCTYPE ...>

            <BODY>

            <!-- StartFragment -->>

            <span data-ttu-id="5390b-183">**<B>Fett</B>formatiert <I><B></B></I>**</span><span class="sxs-lookup"><span data-stu-id="5390b-183">**<B>bold</B><I><B>This is bold italic</B>This</I>**</span></span>

            <!-- EndFragment -->

            </BODY>

            </HTML>

        -   <span data-ttu-id="5390b-184">In diesem Szenario werden nur das Body-Tag und das HTML-Tag im Kontext angezeigt, wenn es dem ausgewählten Fragment vorangestellt ist.</span><span class="sxs-lookup"><span data-stu-id="5390b-184">In this scenario only the BODY tag and the HTML tag appear in the context as it precedes the selected fragment.</span></span> <span data-ttu-id="5390b-185">Beachten Sie, dass Starttags und Endtags in den Kontext eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="5390b-185">Note that start tags and end tags are included in the context.</span></span> <span data-ttu-id="5390b-186">Die Auswahl, die durch startselection und endselection getrennt ist, wird in Fett Schrift angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5390b-186">The selection, as delimited by StartSelection and EndSelection, is shown in bold.</span></span>

2.  <span data-ttu-id="5390b-187">Fragment einer Tabelle in HTML.</span><span class="sxs-lookup"><span data-stu-id="5390b-187">Fragment of a table in HTML.</span></span>
    -   -   <span data-ttu-id="5390b-188">HTML-Text:</span><span class="sxs-lookup"><span data-stu-id="5390b-188">HTML text:</span></span>

            <BODY><TABLE BORDER><TR><TH ROWSPAN=2><span data-ttu-id="5390b-189">Head1</span><span class="sxs-lookup"><span data-stu-id="5390b-189">Head1</span></span></TH><TD><span data-ttu-id="5390b-190">Element 1</span><span class="sxs-lookup"><span data-stu-id="5390b-190">Item 1</span></span></TD><TD><span data-ttu-id="5390b-191">Item 2</span><span class="sxs-lookup"><span data-stu-id="5390b-191">Item 2</span></span></TD><TD><span data-ttu-id="5390b-192">Element 3</span><span class="sxs-lookup"><span data-stu-id="5390b-192">Item 3</span></span></TD><TD><span data-ttu-id="5390b-193">Element 4</span><span class="sxs-lookup"><span data-stu-id="5390b-193">Item 4</span></span></TD></TR><TR><TD><span data-ttu-id="5390b-194">Element 5</span><span class="sxs-lookup"><span data-stu-id="5390b-194">Item 5</span></span></TD><TD><span data-ttu-id="5390b-195">Element 6</span><span class="sxs-lookup"><span data-stu-id="5390b-195">Item 6</span></span></TD><TD><span data-ttu-id="5390b-196">Element 7</span><span class="sxs-lookup"><span data-stu-id="5390b-196">Item 7</span></span></TD><TD><span data-ttu-id="5390b-197">Element 8</span><span class="sxs-lookup"><span data-stu-id="5390b-197">Item 8</span></span></TD></TR><TR><TH><span data-ttu-id="5390b-198">Head2</span><span class="sxs-lookup"><span data-stu-id="5390b-198">Head2</span></span></TH><TD><span data-ttu-id="5390b-199">Element 9</span><span class="sxs-lookup"><span data-stu-id="5390b-199">Item 9</span></span></TD><TD><span data-ttu-id="5390b-200">Element 10</span><span class="sxs-lookup"><span data-stu-id="5390b-200">Item 10</span></span></TD><TD><span data-ttu-id="5390b-201">Element 11</span><span class="sxs-lookup"><span data-stu-id="5390b-201">Item 11</span></span></TD><TD><span data-ttu-id="5390b-202">Element 12</span><span class="sxs-lookup"><span data-stu-id="5390b-202">Item 12</span></span></TD></TR></TABLE></BODY>

        -   <span data-ttu-id="5390b-203">Angezeigt als: ></span><span class="sxs-lookup"><span data-stu-id="5390b-203">Appears as: ></span></span><TABLE BORDER><TR><TH ROWSPAN=2><span data-ttu-id="5390b-204">Head1</span><span class="sxs-lookup"><span data-stu-id="5390b-204">Head1</span></span></TH><TD><span data-ttu-id="5390b-205">Element 1</span><span class="sxs-lookup"><span data-stu-id="5390b-205">Item 1</span></span></TD><TD><span data-ttu-id="5390b-206">Item 2</span><span class="sxs-lookup"><span data-stu-id="5390b-206">Item 2</span></span></TD><TD><span data-ttu-id="5390b-207">Element 3</span><span class="sxs-lookup"><span data-stu-id="5390b-207">Item 3</span></span></TD><TD><span data-ttu-id="5390b-208">Element 4</span><span class="sxs-lookup"><span data-stu-id="5390b-208">Item 4</span></span></TD></TR><TR><TD><span data-ttu-id="5390b-209">Element 5</span><span class="sxs-lookup"><span data-stu-id="5390b-209">Item 5</span></span></TD><TD><span data-ttu-id="5390b-210">Element 6</span><span class="sxs-lookup"><span data-stu-id="5390b-210">Item 6</span></span></TD><TD><span data-ttu-id="5390b-211">Element 7</span><span class="sxs-lookup"><span data-stu-id="5390b-211">Item 7</span></span></TD><TD><span data-ttu-id="5390b-212">Element 8</span><span class="sxs-lookup"><span data-stu-id="5390b-212">Item 8</span></span></TD></TR><TR><TH><span data-ttu-id="5390b-213">Head2</span><span class="sxs-lookup"><span data-stu-id="5390b-213">Head2</span></span></TH><TD><span data-ttu-id="5390b-214">Element 9</span><span class="sxs-lookup"><span data-stu-id="5390b-214">Item 9</span></span></TD><TD><span data-ttu-id="5390b-215">Element 10</span><span class="sxs-lookup"><span data-stu-id="5390b-215">Item 10</span></span></TD><TD><span data-ttu-id="5390b-216">Element 11</span><span class="sxs-lookup"><span data-stu-id="5390b-216">Item 11</span></span></TD><TD><span data-ttu-id="5390b-217">Element 12</span><span class="sxs-lookup"><span data-stu-id="5390b-217">Item 12</span></span></TD></TR></TABLE><span data-ttu-id="5390b-218"><! \[ CDATA\[\]\]></span><span class="sxs-lookup"><span data-stu-id="5390b-218"><!\[CDATA\[\]\]></span></span>
        -   <span data-ttu-id="5390b-219">Die Elemente Element 6, Item7, Element 10 und Element 11 der Tabelle werden als Block ausgewählt und in die Zwischenablage kopiert.</span><span class="sxs-lookup"><span data-stu-id="5390b-219">The Item 6, Item7, Item 10, and Item 11 elements of the table are selected as a block and copied to the clipboard.</span></span>
        -   <span data-ttu-id="5390b-220">Dies erfolgt in der Zwischenablage (Beachten Sie, dass es sich um eine IE4/MSHTML-Interpretation handelt):</span><span class="sxs-lookup"><span data-stu-id="5390b-220">This is what will be on the clipboard (note this is IE4/MSHTML's interpretation):</span></span>

            <!DOCTYPE ...>

            <HTML><BODY><TABLE BORDER>

            <!--StartFragment-->

            <span data-ttu-id="5390b-221">**<TR><TD>Element 6 </TD> <TD> Element 7 </TD> </TR> <TR> <TD> Element 10 </TD> <TD> Element 11</TD></TR>**</span><span class="sxs-lookup"><span data-stu-id="5390b-221">**<TR><TD>Item 6</TD><TD>Item 7</TD></TR><TR><TD>Item 10</TD><TD>Item 11</TD></TR>**</span></span>

            <!--EndFragment-->

            </TABLE>

            </BODY></HTML>The selection, as delimited by StartSelection and EndSelection, is shown in bold.

3.  <span data-ttu-id="5390b-222">Einfügen eines Fragments einer geordneten Liste in Klartext.</span><span class="sxs-lookup"><span data-stu-id="5390b-222">Pasting a fragment of an ordered list into plain text.</span></span>
    -   -   <span data-ttu-id="5390b-223">HTML-Text:</span><span class="sxs-lookup"><span data-stu-id="5390b-223">HTML text:</span></span>

            <BODY><OL TYPE = a><LI><span data-ttu-id="5390b-224">Element 1</span><span class="sxs-lookup"><span data-stu-id="5390b-224">Item 1</span></span><LI><span data-ttu-id="5390b-225">Item 2</span><span class="sxs-lookup"><span data-stu-id="5390b-225">Item 2</span></span><LI><span data-ttu-id="5390b-226">Element 3</span><span class="sxs-lookup"><span data-stu-id="5390b-226">Item 3</span></span><LI><span data-ttu-id="5390b-227">Element 4</span><span class="sxs-lookup"><span data-stu-id="5390b-227">Item 4</span></span><LI><span data-ttu-id="5390b-228">Element 5</span><span class="sxs-lookup"><span data-stu-id="5390b-228">Item 5</span></span><LI><span data-ttu-id="5390b-229">Element 6</span><span class="sxs-lookup"><span data-stu-id="5390b-229">Item 6</span></span></OL></BODY>

        -   <span data-ttu-id="5390b-230">Angezeigt als:</span><span class="sxs-lookup"><span data-stu-id="5390b-230">Appears as:</span></span>
            1.  <span data-ttu-id="5390b-231">Element 1</span><span class="sxs-lookup"><span data-stu-id="5390b-231">Item 1</span></span>
            2.  <span data-ttu-id="5390b-232">Item 2</span><span class="sxs-lookup"><span data-stu-id="5390b-232">Item 2</span></span>
            3.  <span data-ttu-id="5390b-233">Element 3</span><span class="sxs-lookup"><span data-stu-id="5390b-233">Item 3</span></span>
            4.  <span data-ttu-id="5390b-234">Element 4</span><span class="sxs-lookup"><span data-stu-id="5390b-234">Item 4</span></span>
            5.  <span data-ttu-id="5390b-235">Element 5</span><span class="sxs-lookup"><span data-stu-id="5390b-235">Item 5</span></span>
            6.  <span data-ttu-id="5390b-236">Element 6</span><span class="sxs-lookup"><span data-stu-id="5390b-236">Item 6</span></span>
        -   <span data-ttu-id="5390b-237">Der Benutzer wählt die Elemente 3 bis 5 aus und kopiert sie in die Zwischenablage.</span><span class="sxs-lookup"><span data-stu-id="5390b-237">The user selects and copies items 3 through 5 to the clipboard.</span></span> <span data-ttu-id="5390b-238">Der folgende HTML-Code befindet sich in der Zwischenablage:</span><span class="sxs-lookup"><span data-stu-id="5390b-238">The following HTML is in the clipboard:</span></span>

            <span data-ttu-id="5390b-239"><DOCTYPE... ><HTML><BODY></span><span class="sxs-lookup"><span data-stu-id="5390b-239"><DOCTYPE...><HTML><BODY></span></span><OL TYPE = a>

            <!-- StartFragment-->

            <span data-ttu-id="5390b-240">**<LI>Element 3, Element <LI> 4, <LI> Element 5**</span><span class="sxs-lookup"><span data-stu-id="5390b-240">**<LI>Item 3<LI>Item 4<LI>Item 5**</span></span>

            <!-- EndFragment-->

            </OL></BODY></HTML>

            <span data-ttu-id="5390b-241">Die Auswahl, die durch startselection und endselection getrennt ist, wird fett formatiert angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5390b-241">The selection, as delimited by StartSelection and EndSelection, is show in bold.</span></span>

        -   <span data-ttu-id="5390b-242">Wenn dieses Fragment nun in ein leeres Dokument eingefügt wird, wird der folgende HTML-Code erstellt:</span><span class="sxs-lookup"><span data-stu-id="5390b-242">If this fragment is now pasted into an empty document, the following HTML will be created:</span></span>

            <BODY><OL TYPE = a><LI><span data-ttu-id="5390b-243">Element 3</span><span class="sxs-lookup"><span data-stu-id="5390b-243">Item 3</span></span><LI><span data-ttu-id="5390b-244">Element 4</span><span class="sxs-lookup"><span data-stu-id="5390b-244">Item 4</span></span><LI><span data-ttu-id="5390b-245">Element 5</span><span class="sxs-lookup"><span data-stu-id="5390b-245">Item 5</span></span></OL></BODY>

        -   <span data-ttu-id="5390b-246">Folgendes wird angezeigt:</span><span class="sxs-lookup"><span data-stu-id="5390b-246">Appearing as:</span></span>
            1.  <span data-ttu-id="5390b-247">Element 3</span><span class="sxs-lookup"><span data-stu-id="5390b-247">Item 3</span></span>
            2.  <span data-ttu-id="5390b-248">Element 4</span><span class="sxs-lookup"><span data-stu-id="5390b-248">Item 4</span></span>
            3.  <span data-ttu-id="5390b-249">Element 5</span><span class="sxs-lookup"><span data-stu-id="5390b-249">Item 5</span></span>

4.  <span data-ttu-id="5390b-250">Einfügen eines teilweise ausgewählten Bereichs.</span><span class="sxs-lookup"><span data-stu-id="5390b-250">Pasting a partially selected region.</span></span>
    -   -   <span data-ttu-id="5390b-251">HTML-Text:</span><span class="sxs-lookup"><span data-stu-id="5390b-251">HTML text:</span></span>

            <P> <span data-ttu-id="5390b-252">IE4/MSHTML ist ein WYSIWYG-Editor, der Folgendes unterstützt:</span><span class="sxs-lookup"><span data-stu-id="5390b-252">IE4/MSHTML is a WYSIWYG Editor that supports :</span></span><UL><LI><span data-ttu-id="5390b-253">Ausschneiden</span><span class="sxs-lookup"><span data-stu-id="5390b-253">Cut</span></span><LI><span data-ttu-id="5390b-254">Kopieren</span><span class="sxs-lookup"><span data-stu-id="5390b-254">Copy</span></span><LI><span data-ttu-id="5390b-255">Einfügen</span><span class="sxs-lookup"><span data-stu-id="5390b-255">Paste</span></span></UL><P><span data-ttu-id="5390b-256">Dies ist ein großartiges Tool!</span><span class="sxs-lookup"><span data-stu-id="5390b-256">This is a Great Tool !</span></span>

        -   <span data-ttu-id="5390b-257">Angezeigt als: IE4/MSHTML ist ein WYSIWYG-Editor, der Folgendes unterstützt:</span><span class="sxs-lookup"><span data-stu-id="5390b-257">Appears as:IE4/MSHTML is a WYSIWYG Editor that supports :</span></span>
            -   -   <span data-ttu-id="5390b-258">Ausschneiden</span><span class="sxs-lookup"><span data-stu-id="5390b-258">Cut</span></span>
                -   <span data-ttu-id="5390b-259">Kopieren</span><span class="sxs-lookup"><span data-stu-id="5390b-259">Copy</span></span>
                -   <span data-ttu-id="5390b-260">Einfügen</span><span class="sxs-lookup"><span data-stu-id="5390b-260">Paste</span></span>

        -   <span data-ttu-id="5390b-261">Der Benutzer wählt aus "WYSIWYG" bis "Cop" aus. Der folgende HTML-Code befindet sich in der Zwischenablage:</span><span class="sxs-lookup"><span data-stu-id="5390b-261">The user selects from "WYSIWYG" until "Cop".The following HTML is in the clipboard:</span></span>

            <span data-ttu-id="5390b-262"><DOCTYPE... ><HTML><BODY></span><span class="sxs-lookup"><span data-stu-id="5390b-262"><DOCTYPE...><HTML><BODY></span></span>

            <!-- StartFragment-->

            <P>

            <span data-ttu-id="5390b-263">**WYSIWYG-Editor, der**</span><span class="sxs-lookup"><span data-stu-id="5390b-263">**WYSIWYG Editor, which supports**</span></span>

            <span data-ttu-id="5390b-264">**<UL><LI>COP Ausschneiden <LI>**</span><span class="sxs-lookup"><span data-stu-id="5390b-264">**<UL><LI>Cut<LI>Cop**</span></span>

            </UL>

            <!-- EndFragment-->

            </BODY></HTML>The selection, as delimited by StartSelection and EndSelection, is shown in bold.

     
    -   -   <span data-ttu-id="5390b-265">Der Benutzer wählt zwischen "OPY" und "groß" aus.</span><span class="sxs-lookup"><span data-stu-id="5390b-265">The user selects from "opy" until "Great".</span></span>

            <span data-ttu-id="5390b-266">Der folgende HTML-Code befindet sich in der Zwischenablage:</span><span class="sxs-lookup"><span data-stu-id="5390b-266">The following HTML is in the clipboard:</span></span>

            <span data-ttu-id="5390b-267"><DOCTYPE... ><HTML><BODY></span><span class="sxs-lookup"><span data-stu-id="5390b-267"><DOCTYPE...><HTML><BODY></span></span>

            <!-- StartFragment-->

            <UL><LI>

            <span data-ttu-id="5390b-268">**OPY <LI> Einfügen </UL> <P> Dies ist ein hervorragend.**</span><span class="sxs-lookup"><span data-stu-id="5390b-268">**opy<LI>Paste</UL><P> This is a Great**</span></span>

            </P>

            <!-- EndFragment-->

            </BODY></HTML>

            <span data-ttu-id="5390b-269">Die Auswahl, die durch startselection und endselection getrennt ist, wird in Fett Schrift angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5390b-269">The selection, as delimited by StartSelection and EndSelection, is shown in bold.</span></span>

 

 




