---
description: Diese Konstanten definieren Werte, die den Typ von icontextnode-Objekten angeben.
ms.assetid: 333db79e-f503-4545-84fd-7c1a39a96728
title: Kontext Knoten Typen (iaguid. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_CNT_ANALYSISHINT
- GUID_CNT_CUSTOMRECOGNIZER
- GUID_CNT_IMAGE
- GUID_CNT_INKBULLET
- GUID_CNT_INKDRAWING
- GUID_CNT_INKWORD
- GUID_CNT_LINE
- GUID_CNT_OBJECT
- GUID_CNT_PARAGRAPH
- GUID_CNT_ROOT
- GUID_CNT_TEXTWORD
- GUID_CNT_UNCLASSIFIEDINKNODE
api_type:
- HeaderDef
api_location:
- iaguid.h
ms.openlocfilehash: 918b7cf818ebcedc98f45bff7c41ee66ad4d1592
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127816"
---
# <a name="context-node-types"></a><span data-ttu-id="09835-103">Kontext Knoten Typen</span><span class="sxs-lookup"><span data-stu-id="09835-103">Context Node Types</span></span>

<span data-ttu-id="09835-104">Diese Konstanten definieren Werte, die den Typ von [**icontextnode**](icontextnode.md) -Objekten angeben.</span><span class="sxs-lookup"><span data-stu-id="09835-104">These constants define values that specify the type of [**IContextNode**](icontextnode.md) objects.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="09835-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="09835-105">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="09835-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="09835-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_ANALYSISHINT"></span><span id="guid_cnt_analysishint"></span><dl> <span data-ttu-id="09835-107"><dt><strong>GUID_CNT_ANALYSISHINT</strong></dt> <dt>(AnalysisHint)</dt> </span><span class="sxs-lookup"><span data-stu-id="09835-107"><dt><strong>GUID_CNT_ANALYSISHINT</strong></dt> <dt>(AnalysisHint)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="09835-108">Stellt einen Knoten dar, der zusätzliche Kontextinformationen für einen Bereich enthält, den der <a href="iinkanalyzer.md"><strong>iinkanalyzer</strong></a> verwendet, um die Analyse zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="09835-108">Represents a node that contains additional context information for a region that the <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> uses to improve its analysis.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_CUSTOMRECOGNIZER"></span><span id="guid_cnt_customrecognizer"></span><dl> <span data-ttu-id="09835-109"><dt><strong>GUID_CNT_CUSTOMRECOGNIZER</strong></dt> <dt>(customerkenzer)</dt> </span><span class="sxs-lookup"><span data-stu-id="09835-109"><dt><strong>GUID_CNT_CUSTOMRECOGNIZER</strong></dt> <dt>(CustomRecognizer)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="09835-110">Stellt einen Knoten dar, der für einen einzelnen Erkennungs Vorgang verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="09835-110">Represents a node used for a single recognition operation.</span></span><br/> <span data-ttu-id="09835-111">Alle Striche und Knoten, die sich in einem benutzerdefinierten Erkennungs Knoten befinden, werden von einem unabhängigen Erkennungs Vorgang erkannt und nicht von <a href="iinkanalyzer.md"><strong>iinkanalyzer</strong></a>analysiert.</span><span class="sxs-lookup"><span data-stu-id="09835-111">All strokes and nodes that are within a custom recognizer node are recognized by an independent recognition operation and are not analyzed by the <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a>.</span></span><br/> <span data-ttu-id="09835-112">Ein benutzerdefinierter Erkennungs Knoten muss das direkt untergeordnete Element des Stamm Knotens von Ink Analyzer sein.</span><span class="sxs-lookup"><span data-stu-id="09835-112">A custom recognizer node must be the direct child of ink analyzer's root node.</span></span><br/> <span data-ttu-id="09835-113">Ein benutzerdefinierter Erkennungs Knoten kann die folgenden Typen von untergeordneten Elementen enthalten:</span><span class="sxs-lookup"><span data-stu-id="09835-113">A custom recognizer node can contain the following types of child elements:</span></span><br/>
<ul>
<li><span data-ttu-id="09835-114">Eine beliebige Anzahl von unclassimeedink-Knoten.</span><span class="sxs-lookup"><span data-stu-id="09835-114">Any number of UnclassifiedInk nodes.</span></span></li>
<li><span data-ttu-id="09835-115">Eine beliebige Anzahl von Objekt Knoten.</span><span class="sxs-lookup"><span data-stu-id="09835-115">Any number of Object nodes.</span></span></li>
<li><span data-ttu-id="09835-116">Eine beliebige Anzahl von Zeilen Knoten.</span><span class="sxs-lookup"><span data-stu-id="09835-116">Any number of Line nodes.</span></span></li>
<li><span data-ttu-id="09835-117">Beliebig viele inkWord-Knoten.</span><span class="sxs-lookup"><span data-stu-id="09835-117">Any number of InkWord nodes.</span></span></li>
<li><span data-ttu-id="09835-118">Eine beliebige Anzahl von Knoten mit einem unbekannten GUID-Wert.</span><span class="sxs-lookup"><span data-stu-id="09835-118">Any number of nodes with an unknown Guid value.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_IMAGE"></span><span id="guid_cnt_image"></span><dl> <span data-ttu-id="09835-119"><dt><strong>GUID_CNT_IMAGE</strong></dt> <dt>(Bild)</dt> </span><span class="sxs-lookup"><span data-stu-id="09835-119"><dt><strong>GUID_CNT_IMAGE</strong></dt> <dt>(Image)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="09835-120">Stellt einen Knoten für einen zweidimensionalen Bereich dar, in dem alle Non-Ink-Bilder im Dokument vorhanden sein können.</span><span class="sxs-lookup"><span data-stu-id="09835-120">Represents a node for a two-dimensional region where any non-ink images can exist in the document.</span></span><br/> <span data-ttu-id="09835-121">Der <a href="iinkanalyzer.md"><strong>iinkanalyzer</strong></a> erzeugt keine Bild Knoten.</span><span class="sxs-lookup"><span data-stu-id="09835-121">The <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> does not produce image nodes.</span></span> <span data-ttu-id="09835-122">Verwenden Sie <a href="icontextnode-createsubnode.md"><strong>icontextnode:: kreatesubnode</strong></a> , um der Kontext Knoten Struktur einen Bild Knoten hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="09835-122">Use <a href="icontextnode-createsubnode.md"><strong>IContextNode::CreateSubNode</strong></a> to add an image node to the context node tree.</span></span> <span data-ttu-id="09835-123">Der <strong>iinkanalyzer</strong> verwendet dann die vom Knoten Image definierten Bereiche, um zu bestimmen, ob frei Hand Eingaben das nicht-frei Hand Bild kommentieren.</span><span class="sxs-lookup"><span data-stu-id="09835-123">The <strong>IInkAnalyzer</strong> then uses the regions defined by the image node to determine if any ink annotates the non-ink image.</span></span><br/> <span data-ttu-id="09835-124">Ein Bild Knoten darf keine untergeordneten Elemente aufweisen.</span><span class="sxs-lookup"><span data-stu-id="09835-124">An image node cannot have any child elements.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_INKBULLET"></span><span id="guid_cnt_inkbullet"></span><dl> <span data-ttu-id="09835-125"><dt><strong>GUID_CNT_INKBULLET</strong></dt> <dt>(InkBullet)</dt> </span><span class="sxs-lookup"><span data-stu-id="09835-125"><dt><strong>GUID_CNT_INKBULLET</strong></dt> <dt>(InkBullet)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="09835-126">Der InkBullet ContextNodeType stellt eine Auflistung von Strichen dar, die ein Aufzählungs Zeichen in einer Aufzählung bilden.</span><span class="sxs-lookup"><span data-stu-id="09835-126">The InkBullet ContextNodeType represents a collection of strokes that make up a bullet in a bulleted list.</span></span><br/> <span data-ttu-id="09835-127">Ein ContextNode des Typs "InkBullet" kann keine untergeordneten Elemente aufweisen.</span><span class="sxs-lookup"><span data-stu-id="09835-127">A ContextNode of type InkBullet cannot have any children.</span></span> <span data-ttu-id="09835-128">Es kann nur ein untergeordnetes Element eines Absatz-ContextNode sein.</span><span class="sxs-lookup"><span data-stu-id="09835-128">It can only be a child of a Paragraph ContextNode.</span></span> <span data-ttu-id="09835-129">Nur eine InkBullet kann in einem einzelnen Absatz ContextNode angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="09835-129">Only one InkBullet can appear in a single Paragraph ContextNode.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_INKDRAWING"></span><span id="guid_cnt_inkdrawing"></span><dl> <span data-ttu-id="09835-130"><dt><strong>GUID_CNT_INKDRAWING</strong></dt> <dt>(InkDrawing)</dt> </span><span class="sxs-lookup"><span data-stu-id="09835-130"><dt><strong>GUID_CNT_INKDRAWING</strong></dt> <dt>(InkDrawing)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="09835-131">Stellt einen Knoten für eine Auflistung von Strichen dar, die eine Zeichnung bilden.</span><span class="sxs-lookup"><span data-stu-id="09835-131">Represents a node for a collection of strokes that constitutes a drawing.</span></span><br/> <span data-ttu-id="09835-132">Zeichnungen sind Striche, die als Formen oder abstrakte Skizzen bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="09835-132">Drawings are strokes that are determined to be shapes or abstract sketches.</span></span> <span data-ttu-id="09835-133">Dabei handelt es sich im Allgemeinen um alle Striche, die nicht als Schreibvorgänge klassifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="09835-133">They are generally any strokes that are not classified as writing strokes.</span></span><br/> <span data-ttu-id="09835-134">Ein Ink-Zeichnungs Knoten darf keine untergeordneten Elemente aufweisen.</span><span class="sxs-lookup"><span data-stu-id="09835-134">An ink drawing node cannot have any child elements.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_INKWORD"></span><span id="guid_cnt_inkword"></span><dl> <span data-ttu-id="09835-135"><dt><strong>GUID_CNT_INKWORD</strong></dt> <dt>(InkWord)</dt> </span><span class="sxs-lookup"><span data-stu-id="09835-135"><dt><strong>GUID_CNT_INKWORD</strong></dt> <dt>(InkWord)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="09835-136">Stellt einen Knoten für eine Auflistung von Strichen dar, die eine logische Gruppierung zum bilden eines erkennbaren Worts bilden.</span><span class="sxs-lookup"><span data-stu-id="09835-136">Represents a node for a collection of strokes that constitutes a logical grouping to form a recognizable word.</span></span><br/> <span data-ttu-id="09835-137">Ein Ink Word-Knoten darf keine untergeordneten Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="09835-137">An ink word node cannot contain any child elements.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_LINE"></span><span id="guid_cnt_line"></span><dl> <span data-ttu-id="09835-138"><dt><strong>GUID_CNT_LINE</strong></dt> <dt>(Zeile)</dt> </span><span class="sxs-lookup"><span data-stu-id="09835-138"><dt><strong>GUID_CNT_LINE</strong></dt> <dt>(Line)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="09835-139">Stellt einen Knoten für eine Zeile von Wörtern dar.</span><span class="sxs-lookup"><span data-stu-id="09835-139">Represents a node for a line of words.</span></span><br/> <span data-ttu-id="09835-140">Ein Zeilen Knoten kann die folgenden Typen von untergeordneten Elementen enthalten:</span><span class="sxs-lookup"><span data-stu-id="09835-140">A line node can contain the following types of child elements:</span></span><br/>
<ul>
<li><span data-ttu-id="09835-141">Beliebig viele frei Hand Wort Knoten.</span><span class="sxs-lookup"><span data-stu-id="09835-141">Any number of ink word nodes.</span></span></li>
<li><span data-ttu-id="09835-142">Eine beliebige Anzahl von Text Word-Knoten.</span><span class="sxs-lookup"><span data-stu-id="09835-142">Any number of text word nodes.</span></span></li>
<li><span data-ttu-id="09835-143">Eine beliebige Anzahl von Knoten mit einem unbekannten <strong>GUID</strong> -Wert.</span><span class="sxs-lookup"><span data-stu-id="09835-143">Any number of nodes with an unknown <strong>GUID</strong> value.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_OBJECT"></span><span id="guid_cnt_object"></span><dl> <span data-ttu-id="09835-144"><dt><strong>GUID_CNT_OBJECT</strong></dt> <dt>(Objekt)</dt> </span><span class="sxs-lookup"><span data-stu-id="09835-144"><dt><strong>GUID_CNT_OBJECT</strong></dt> <dt>(Object)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="09835-145">Stellt einen Knoten für ein Objekt dar, das von einem &quot; benutzerdefinierten Objekterkennungsmodul zurückgegeben wird &quot; .</span><span class="sxs-lookup"><span data-stu-id="09835-145">Represents a node for an object that is returned from an &quot;object&quot; custom recognizer.</span></span><br/> <span data-ttu-id="09835-146">Ein Objekt Knoten kann keine untergeordneten Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="09835-146">An object node cannot contain any child elements.</span></span><br/> <span data-ttu-id="09835-147">Nur benutzerdefinierte Erkennungs Knoten können Objekt Knoten enthalten.</span><span class="sxs-lookup"><span data-stu-id="09835-147">Only custom recognizer nodes can contain object nodes.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_PARAGRAPH"></span><span id="guid_cnt_paragraph"></span><dl> <span data-ttu-id="09835-148"><dt><strong>GUID_CNT_PARAGRAPH</strong></dt> <dt>(Absatz)</dt> </span><span class="sxs-lookup"><span data-stu-id="09835-148"><dt><strong>GUID_CNT_PARAGRAPH</strong></dt> <dt>(Paragraph)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="09835-149">Stellt einen Knoten für eine Auflistung von Knoten dar, die eine logische Gruppierung von Zeilen bilden.</span><span class="sxs-lookup"><span data-stu-id="09835-149">Represents a node for a collection of nodes that constitutes a logical grouping of lines.</span></span><br/> <span data-ttu-id="09835-150">Die genaue Definition eines Absatzes wird von den analysierten Engines bestimmt.</span><span class="sxs-lookup"><span data-stu-id="09835-150">The exact definition of a paragraph is determined by the analyzing engines.</span></span> <span data-ttu-id="09835-151">Im Allgemeinen enthält ein Absatz Gruppen von Zeilen, die sich wiederholen, wenn das Feld, das die Zeilen enthält, geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="09835-151">In general, a paragraph contains groups of lines that would reflow together if the box that contains the lines were resized.</span></span><br/> <span data-ttu-id="09835-152">Ein Absatz Knoten kann die folgenden Typen von untergeordneten Elementen enthalten:</span><span class="sxs-lookup"><span data-stu-id="09835-152">A paragraph node can contain the following types of child elements:</span></span><br/>
<ul>
<li><span data-ttu-id="09835-153">Beliebig viele Freihand-Aufzählungs Knoten.</span><span class="sxs-lookup"><span data-stu-id="09835-153">Any number of ink bullet nodes.</span></span></li>
<li><span data-ttu-id="09835-154">Eine beliebige Anzahl von Zeilen Knoten.</span><span class="sxs-lookup"><span data-stu-id="09835-154">Any number of line nodes.</span></span></li>
<li><span data-ttu-id="09835-155">Eine beliebige Anzahl von Knoten mit einem unbekannten <strong>GUID</strong> -Wert.</span><span class="sxs-lookup"><span data-stu-id="09835-155">Any number of nodes with an unknown <strong>GUID</strong> value.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_ROOT"></span><span id="guid_cnt_root"></span><dl> <span data-ttu-id="09835-156"><dt><strong>GUID_CNT_ROOT</strong></dt> <dt>(root)</dt> </span><span class="sxs-lookup"><span data-stu-id="09835-156"><dt><strong>GUID_CNT_ROOT</strong></dt> <dt>(Root)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="09835-157">Stellt einen Knoten für den obersten Knoten einer Struktur von Knoten dar, die die Ergebnisse der frei Hand Analyse beschreiben.</span><span class="sxs-lookup"><span data-stu-id="09835-157">Represents a node for the top node of a tree of nodes that describe the results of ink analysis.</span></span><br/> <span data-ttu-id="09835-158">Stamm Knoten werden in der Regel von der <a href="iinkanalyzer-getrootnode.md"><strong>Methoden Methode iinkanalyzer:: GetRootNode</strong></a> abgerufen.</span><span class="sxs-lookup"><span data-stu-id="09835-158">Root nodes are generally obtained from the <a href="iinkanalyzer-getrootnode.md"><strong>IInkAnalyzer::GetRootNode Method</strong></a> method.</span></span><br/> <span data-ttu-id="09835-159">Ein Stamm Knoten kann die folgenden Typen von untergeordneten Elementen enthalten:</span><span class="sxs-lookup"><span data-stu-id="09835-159">A root node can contain the following types of child elements:</span></span><br/>
<ul>
<li><span data-ttu-id="09835-160">Eine beliebige Anzahl von Analyse Hinweis Knoten.</span><span class="sxs-lookup"><span data-stu-id="09835-160">Any number of analysis hint nodes.</span></span></li>
<li><span data-ttu-id="09835-161">Eine beliebige Anzahl von benutzerdefinierten Erkennungs Knoten.</span><span class="sxs-lookup"><span data-stu-id="09835-161">Any number of custom recognizer nodes.</span></span></li>
<li><span data-ttu-id="09835-162">Beliebig viele Bild Knoten.</span><span class="sxs-lookup"><span data-stu-id="09835-162">Any number of image nodes.</span></span></li>
<li><span data-ttu-id="09835-163">Eine beliebige Anzahl von frei Hand Zeichnungs Knoten.</span><span class="sxs-lookup"><span data-stu-id="09835-163">Any number of ink drawing nodes.</span></span></li>
<li><span data-ttu-id="09835-164">Eine beliebige Anzahl von Schreib Regions Knoten.</span><span class="sxs-lookup"><span data-stu-id="09835-164">Any number of writing region nodes.</span></span></li>
<li><span data-ttu-id="09835-165">Eine beliebige Anzahl von nicht klassifizierten frei Hand Knoten.</span><span class="sxs-lookup"><span data-stu-id="09835-165">Any number of unclassified ink nodes.</span></span></li>
<li><span data-ttu-id="09835-166">Eine beliebige Anzahl von Knoten mit einem unbekannten <strong>GUID</strong> -Wert.</span><span class="sxs-lookup"><span data-stu-id="09835-166">Any number of nodes with an unknown <strong>GUID</strong> value.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_TEXTWORD"></span><span id="guid_cnt_textword"></span><dl> <span data-ttu-id="09835-167"><dt><strong>GUID_CNT_TEXTWORD</strong></dt> <dt>(textword)</dt> </span><span class="sxs-lookup"><span data-stu-id="09835-167"><dt><strong>GUID_CNT_TEXTWORD</strong></dt> <dt>(TextWord)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="09835-168">Stellt einen Knoten für den zweidimensionalen Bereich dar, in dem ein nicht frei Hand Text im Dokument vorhanden sein kann.</span><span class="sxs-lookup"><span data-stu-id="09835-168">Represents a node for the two-dimensional region where any non-ink text can exist in the document.</span></span><br/> <span data-ttu-id="09835-169">Der <a href="iinkanalyzer.md"><strong>iinkanalyzer</strong></a> erzeugt keine Text Wort Knoten.</span><span class="sxs-lookup"><span data-stu-id="09835-169">The <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> does not produce text word nodes.</span></span> <span data-ttu-id="09835-170">Verwenden Sie <a href="icontextnode-createsubnode.md"><strong>icontextnode:: kreatesubnode</strong></a> , um der Kontext Knoten Struktur einen Text Wort Knoten hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="09835-170">Use <a href="icontextnode-createsubnode.md"><strong>IContextNode::CreateSubNode</strong></a> to add a text word node to the context node tree.</span></span> <span data-ttu-id="09835-171">Der <strong>iinkanalyzer</strong> verwendet dann die vom Text Word-Knoten definierten Regionen, um zu bestimmen, ob frei Hand Eingaben den nicht frei Hand Text kommentieren.</span><span class="sxs-lookup"><span data-stu-id="09835-171">The <strong>IInkAnalyzer</strong> then uses the regions defined by the text word node to determine if any ink annotates the non-ink text.</span></span><br/> <span data-ttu-id="09835-172">Zukünftige erkenungen können die von einem Text Word-Knoten definierte Region verwenden, um zu bestimmen, ob frei Hand Eingaben das nicht frei Hand Wort kommentieren.</span><span class="sxs-lookup"><span data-stu-id="09835-172">Future recognizers may use the region defined by a text word node to determine if any ink annotates the non-ink word.</span></span><br/> <span data-ttu-id="09835-173">Ein Text Word-Knoten darf keine untergeordneten Elemente aufweisen.</span><span class="sxs-lookup"><span data-stu-id="09835-173">A text word node cannot have any child elements</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_UNCLASSIFIEDINKNODE"></span><span id="guid_cnt_unclassifiedinknode"></span><dl> <span data-ttu-id="09835-174"><dt><strong>GUID_CNT_UNCLASSIFIEDINKNODE</strong></dt> <dt>(unclassimeedink)</dt> </span><span class="sxs-lookup"><span data-stu-id="09835-174"><dt><strong>GUID_CNT_UNCLASSIFIEDINKNODE</strong></dt> <dt>(UnclassifiedInk)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="09835-175">Stellt einen Knoten für alle Striche dar, die noch nicht klassifiziert oder erkannt wurden.</span><span class="sxs-lookup"><span data-stu-id="09835-175">Represents a node for any strokes that have not yet been classified or recognized.</span></span><br/> <span data-ttu-id="09835-176">Ein nicht klassifizierter Ink-Knoten darf keine untergeordneten Elemente aufweisen.</span><span class="sxs-lookup"><span data-stu-id="09835-176">An unclassified ink node cannot have any child elements.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="09835-177">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="09835-177">Remarks</span></span>

<span data-ttu-id="09835-178">Weitere Informationen zu den verschiedenen Kontext Knoten Typen finden Sie unter [Übersicht](ink-analysis-overview.md)über die Ink-Analyse.</span><span class="sxs-lookup"><span data-stu-id="09835-178">For more information about the different context node types, see [Ink Analysis Overview](ink-analysis-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="09835-179">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="09835-179">Requirements</span></span>



| <span data-ttu-id="09835-180">Anforderung</span><span class="sxs-lookup"><span data-stu-id="09835-180">Requirement</span></span> | <span data-ttu-id="09835-181">Wert</span><span class="sxs-lookup"><span data-stu-id="09835-181">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="09835-182">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="09835-182">Minimum supported client</span></span><br/> | <span data-ttu-id="09835-183">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="09835-183">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="09835-184">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="09835-184">Minimum supported server</span></span><br/> | <span data-ttu-id="09835-185">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="09835-185">None supported</span></span><br/>                                                           |
| <span data-ttu-id="09835-186">Header</span><span class="sxs-lookup"><span data-stu-id="09835-186">Header</span></span><br/>                   | <dl> <span data-ttu-id="09835-187"><dt>Iaguid. h</dt></span><span class="sxs-lookup"><span data-stu-id="09835-187"><dt>Iaguid.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09835-188">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="09835-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09835-189">**Icontextnode:: kreatepartiallypopulatedsubnode**</span><span class="sxs-lookup"><span data-stu-id="09835-189">**IContextNode::CreatePartiallyPopulatedSubNode**</span></span>](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[<span data-ttu-id="09835-190">**Icontextnode:: "kreatesubnode"**</span><span class="sxs-lookup"><span data-stu-id="09835-190">**IContextNode::CreateSubNode**</span></span>](icontextnode-createsubnode.md)
</dt> <dt>

[<span data-ttu-id="09835-191">**Icontextnode:: GetType**</span><span class="sxs-lookup"><span data-stu-id="09835-191">**IContextNode::GetType**</span></span>](icontextnode-gettype.md)
</dt> <dt>

[<span data-ttu-id="09835-192">**Iinkanalyzer:: feateanalysishint-Methode**</span><span class="sxs-lookup"><span data-stu-id="09835-192">**IInkAnalyzer::CreateAnalysisHint Method**</span></span>](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[<span data-ttu-id="09835-193">**Iinkanalyzer:: kreatecustomerkenzer-Methode**</span><span class="sxs-lookup"><span data-stu-id="09835-193">**IInkAnalyzer::CreateCustomRecognizer Method**</span></span>](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="09835-194">**Iinkanalyzer:: findnodesoft ype-Methode**</span><span class="sxs-lookup"><span data-stu-id="09835-194">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="09835-195">**Iinkanalyzer:: findnodesoft ypeer forstrokes-Methode**</span><span class="sxs-lookup"><span data-stu-id="09835-195">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="09835-196">**Iinkanalyzer:: findnodesoft ypeinsubtree-Methode**</span><span class="sxs-lookup"><span data-stu-id="09835-196">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="09835-197">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="09835-197">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




