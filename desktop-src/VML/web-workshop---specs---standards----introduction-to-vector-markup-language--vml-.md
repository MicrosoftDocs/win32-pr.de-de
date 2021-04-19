---
title: Vector Markup Language (VML)
description: Vector Markup Language (VML)
ms.assetid: 1f30d60f-3d4f-43e4-9a2b-424a5ee8f852
keywords:
- Vector Markup Language (VML), Informationen zu
- VML (Vector Markup Language), Informationen zu
- Vektorgrafiken, Informationen zu
- Vektorgrafiken, Vector Markup Language (VML)
- Vector Markup Language (VML), World Wide Web Consortium (W3C)
- VML (Vector Markup Language), World Wide Web Consortium (W3C)
- Vektorgrafiken, World Wide Web Consortium (W3C)
- Vektorgrafiken, VML-Vorteile
- Vector Markup Language (VML), Vorteile
- VML (Vector Markup Language), Vorteile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0ba51fd041f36915eaafe20201876653f597e04
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106364272"
---
# <a name="vector-markup-language-vml"></a><span data-ttu-id="1a97f-113">Vector Markup Language (VML)</span><span class="sxs-lookup"><span data-stu-id="1a97f-113">Vector Markup Language (VML)</span></span>

<span data-ttu-id="1a97f-114">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="1a97f-114">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="1a97f-115">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="1a97f-115">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!NOTE]
> <span data-ttu-id="1a97f-116">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="1a97f-116">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="1a97f-117">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="1a97f-117">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="1a97f-118">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="1a97f-118">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="1a97f-119">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="1a97f-119">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

<span data-ttu-id="1a97f-120">Vector Markup Language (VML) ist ein XML-basiertes Exchange-, Bearbeitungs-und Übermittlungs Format für hochwertige Vektorgrafiken im Web, das die Anforderungen von Produktivitäts-und Grafik Entwurfs Experten erfüllt.</span><span class="sxs-lookup"><span data-stu-id="1a97f-120">Vector Markup Language (VML) is an XML-based exchange, editing, and delivery format for high-quality vector graphics on the Web that meets the needs of both productivity users and graphic design professionals.</span></span> <span data-ttu-id="1a97f-121">XML ist eine neue, einfache, flexible und offene textbasierte Sprache, die HTML ergänzt.</span><span class="sxs-lookup"><span data-stu-id="1a97f-121">XML is an emerging simple, flexible, and open text-based language that complements HTML.</span></span> <span data-ttu-id="1a97f-122">(Ausführliche Informationen zu XML finden Sie im [XML-Abschnitt](/documentation/?frame=true) der MSDN Library.)</span><span class="sxs-lookup"><span data-stu-id="1a97f-122">(See the [XML section](/documentation/?frame=true) of the MSDN Library for detailed information on XML.)</span></span>

<span data-ttu-id="1a97f-123">VML wird derzeit von Microsoft Internet Explorer Version 5,0 oder höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1a97f-123">VML is currently supported by Microsoft Internet Explorer version 5.0 or later.</span></span>

<span data-ttu-id="1a97f-124">VML wurde dem W3C als Standard für Vektorgrafiken im Web vorgeschlagen (siehe [Vector Markup Language (VML)](https://www.w3.org/TR/NOTE-VML)).</span><span class="sxs-lookup"><span data-stu-id="1a97f-124">VML has been proposed to the W3C as a standard for vector graphics on the Web (see [Vector Markup Language (VML)](https://www.w3.org/TR/NOTE-VML)).</span></span> <span data-ttu-id="1a97f-125">Microsoft führt weiterhin die Kosten für die Entwicklung und Implementierung von XML-basierten Technologien ein, die mit führenden Branchenpartnern (Autodesk, Hewlett-Packard, Macromedia, Visio) und dem W3C arbeiten, um webbasierte Standards voranzutreiben.</span><span class="sxs-lookup"><span data-stu-id="1a97f-125">Microsoft is continuing to lead the charge in the development and implementation of XML-based technologies, working with leading industry partners (AutoDesk, Hewlett-Packard, Macromedia, Visio) and the W3C to advance Web-based standards.</span></span> <span data-ttu-id="1a97f-126">Wir gehen davon aus, dass Sie mit dem W3C arbeiten, um letztendlich ein Standardformat für Vektorgrafiken im Web zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="1a97f-126">We expect to work with the W3C to ultimately drive to one standard format for vector graphics on the Web.</span></span>

<span data-ttu-id="1a97f-127">VML wird auch von Microsoft Office 2000 oder höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1a97f-127">VML is also supported by Microsoft Office 2000 or later.</span></span> <span data-ttu-id="1a97f-128">Zum Erstellen von VML-Grafiken können Microsoft Word, Microsoft Excel und Microsoft PowerPoint verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1a97f-128">Microsoft Word, Microsoft Excel, and Microsoft PowerPoint can be used to create VML graphics.</span></span>

### <a name="using-vml"></a><span data-ttu-id="1a97f-129">Verwenden von VML</span><span class="sxs-lookup"><span data-stu-id="1a97f-129">Using VML</span></span>

<span data-ttu-id="1a97f-130">Um VML in ihren Webseiten zu verwenden, verwenden Sie ein Style-Element, um das VML-Verhalten zu importieren, wie im folgenden Code gezeigt.</span><span class="sxs-lookup"><span data-stu-id="1a97f-130">To use VML in your web pages, use a style element to import the VML behavior, as shown in the following code.</span></span>

```
<style>v\: * { behavior:url(#default#VML); display:inline-block }</style>
```

<span data-ttu-id="1a97f-131">Deklarieren Sie als nächstes den VML-Namespace, wie im folgenden Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="1a97f-131">Next, declare the VML namespace, as shown in the following code sample.</span></span>

```
<xml:namespace ns="urn:schemas-microsoft-com:vml" prefix="v" />
```

<span data-ttu-id="1a97f-132">Fügen Sie schließlich VML-Elemente hinzu, um visuelle Effekte zu definieren.</span><span class="sxs-lookup"><span data-stu-id="1a97f-132">Finally, add VML elements to define visuals effects.</span></span> <span data-ttu-id="1a97f-133">Der folgende VML-Code erstellt z. b. ein rotes Oval.</span><span class="sxs-lookup"><span data-stu-id="1a97f-133">For example, the following VML code creates a red oval.</span></span>

```
<v:oval style="width:100pt;height:50pt" fillcolor="red">
</v:oval>
```

> [!NOTE]
> <span data-ttu-id="1a97f-134">Um optimale Ergebnisse zu erhalten, wenn Sie Dokumente im Strict-Modus verwenden, stellen Sie sicher, dass Ihr Markup gültig und wohl geformt ist.</span><span class="sxs-lookup"><span data-stu-id="1a97f-134">For best results when using strict mode documents, be sure that your markup is valid and well-formed.</span></span> <span data-ttu-id="1a97f-135">Weitere Informationen finden Sie unter! DOCTYPE-Referenzseite.</span><span class="sxs-lookup"><span data-stu-id="1a97f-135">For more information, please see the !DOCTYPE reference page.</span></span>


### <a name="benefits-of-vml"></a><span data-ttu-id="1a97f-136">Vorteile von VML</span><span class="sxs-lookup"><span data-stu-id="1a97f-136">Benefits of VML</span></span>

-   <span data-ttu-id="1a97f-137">VML vereinfacht das Erstellen von Produktivitäts Benutzern und Autoren.</span><span class="sxs-lookup"><span data-stu-id="1a97f-137">VML makes authoring easier for productivity users and authors.</span></span> <span data-ttu-id="1a97f-138">Der Austausch ermöglicht den Austausch (per Ausschneiden und Einfügen) und die anschließende Bearbeitung von Vektorgrafiken zwischen einer Vielzahl von Produktivitäts-und Entwurfs Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="1a97f-138">It facilitates the exchange (via cut and paste) and subsequent editing of vector graphics between a wide variety of productivity and design applications.</span></span>
-   <span data-ttu-id="1a97f-139">VML bietet schnellere grafische Downloads und eine bessere Benutzer Leistung.</span><span class="sxs-lookup"><span data-stu-id="1a97f-139">VML provides faster graphic downloads and a better user experience.</span></span> <span data-ttu-id="1a97f-140">Sie ermöglicht die Bereitstellung hochwertiger, vollständig integrierter, skalierbarer Vektorgrafiken im Web in einem geöffneten textbasierten Format.</span><span class="sxs-lookup"><span data-stu-id="1a97f-140">It allows the delivery of high-quality, fully integrated, scalable vector graphics to the Web, in an open text-based format.</span></span> <span data-ttu-id="1a97f-141">Anstatt auf Grafiken als externe Dateien zu verweisen, werden VML-Grafiken Inline mit der HTML-Seite geliefert, sodass Sie mit der Benutzerinteraktion interagieren und skalieren können.</span><span class="sxs-lookup"><span data-stu-id="1a97f-141">Rather than referencing graphics as external files, VML graphics are delivered inline with the HTML page, allowing them to interact and scale with user interaction.</span></span>
-   <span data-ttu-id="1a97f-142">VML ist offen und auf Standards basiert.</span><span class="sxs-lookup"><span data-stu-id="1a97f-142">VML is open and standards-based.</span></span> <span data-ttu-id="1a97f-143">Es handelt sich um ein XML-basiertes Format.</span><span class="sxs-lookup"><span data-stu-id="1a97f-143">It is an XML-based format.</span></span> <span data-ttu-id="1a97f-144">XML 1,0 ist eine offene, einfache, textbasierte Sprache zum beschreiben strukturierter Daten im Web und ergänzt HTML für die Anzeige.</span><span class="sxs-lookup"><span data-stu-id="1a97f-144">XML 1.0 is an open, simple, text-based language for describing structured data on the Web, and complements HTML for display.</span></span> <span data-ttu-id="1a97f-145">VML unterstützt auch andere W3C-Standards, wie z. b. Cascading Stylesheets 2,0 (CSS), das Stil Informationen und 2D-Positionierung angibt, sowie das Dokumentobjektmodell (DOM), mit dem Entwickler konsistent mit Seitenelementen als Objekte interagieren können.</span><span class="sxs-lookup"><span data-stu-id="1a97f-145">VML also supports other W3C standards, such as Cascading Style Sheets 2.0 (CSS), which specifies style information and 2-D positioning, as well as the Document Object Model (DOM), which allows developers to interact consistently with page elements as objects.</span></span>

### <a name="for-additional-information"></a><span data-ttu-id="1a97f-146">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1a97f-146">For additional information</span></span>

<span data-ttu-id="1a97f-147">Sehen Sie sich die Links unten an:</span><span class="sxs-lookup"><span data-stu-id="1a97f-147">See the links below:</span></span>

-   <span data-ttu-id="1a97f-148">Antworten auf häufig gestellte Fragen zu VML finden Sie in den häufig gestellten Fragen zu [VML](frequently-asked-questions-about-vml.md).</span><span class="sxs-lookup"><span data-stu-id="1a97f-148">For answers to frequently asked questions about VML, see the [VML FAQ](frequently-asked-questions-about-vml.md).</span></span>
-   <span data-ttu-id="1a97f-149">Ein Tutorial zur Verwendung von VML auf Webseiten finden Sie unter Gewusst [wie: Verwenden von VML auf Webseiten](web-workshop---specs---standards----how-to-use-vml-on-web-pages.md), das die an das W3C gesendete [VML-Spezifikation](https://www.w3.org/TR/NOTE-datetime.html) ergänzt.</span><span class="sxs-lookup"><span data-stu-id="1a97f-149">For a tutorial on using VML on Web pages, see [How to Use VML on Web Pages](web-workshop---specs---standards----how-to-use-vml-on-web-pages.md), which complements the [VML specification](https://www.w3.org/TR/NOTE-datetime.html) submitted to the W3C.</span></span>
-   <span data-ttu-id="1a97f-150">Informationen zu VML-Datentypen finden Sie im Dokument [grundlegende VML-Typen](basic-vml-types.md) .</span><span class="sxs-lookup"><span data-stu-id="1a97f-150">For information on VML data types, see the [Basic VML Types](basic-vml-types.md) document.</span></span>
-   <span data-ttu-id="1a97f-151">Eine umfassende Referenz zu VML, einschließlich Informationen zur Verwendung von VML mit Tags und Skripterstellung, finden Sie in der [VML-Referenz](msdn-online-vml-introduction.md).</span><span class="sxs-lookup"><span data-stu-id="1a97f-151">For the complete reference on VML, including information on how to use VML with tags as well as scripting, see the [VML Reference](msdn-online-vml-introduction.md).</span></span>