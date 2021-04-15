---
title: Die documentsummaryinformation-und UserDefined-Eigenschaften Sätze
description: Ein "documentsummaryinformation"-und ein benutzerdefinierter Eigenschaften Satz ist eine Erweiterung für den Eigenschaften Satz für Zusammenfassungs Informationen. Beide Eigenschaften Sätze können gleichzeitig vorhanden sein.
ms.assetid: c6d4e2bc-f7f6-429d-aa91-432d833c69d1
keywords:
- Documentsummaryinformation
- Benutzerdefinierte Eigenschaften Sätze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 411c6081ec098539baa2b26b6594d04216f5b455
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515722"
---
# <a name="the-documentsummaryinformation-and-userdefined-property-sets"></a><span data-ttu-id="d4052-106">Die documentsummaryinformation-und UserDefined-Eigenschaften Sätze</span><span class="sxs-lookup"><span data-stu-id="d4052-106">The DocumentSummaryInformation and UserDefined Property Sets</span></span>

<span data-ttu-id="d4052-107">Ein " **documentsummaryinformation** "-und ein **benutzerdefinierter** Eigenschaften Satz ist eine Erweiterung für [den Eigenschaften Satz für Zusammenfassungs Informationen](the-summary-information-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="d4052-107">A **DocumentSummaryInformation** and **UserDefined** property set is an extension to [the Summary Information property set](the-summary-information-property-set.md).</span></span> <span data-ttu-id="d4052-108">Beide Eigenschaften Sätze können gleichzeitig vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="d4052-108">Both property sets can exist simultaneously.</span></span>

<span data-ttu-id="d4052-109">Der Name des Streams, der den **documentsummaryinformation** -Eigenschaften Satz enthält, ist **" \\ 005documentsummaryinformation"**.</span><span class="sxs-lookup"><span data-stu-id="d4052-109">The name of the stream that contains the **DocumentSummaryInformation** property set is **"\\005DocumentSummaryInformation"**.</span></span> <span data-ttu-id="d4052-110">Der Format Bezeichner (fmtid) für den **documentsummaryinformation** -Eigenschaften Satz ist **D5CDD502-2E9C-101B-9397-08002B2CF9AE**.</span><span class="sxs-lookup"><span data-stu-id="d4052-110">The format identifier (FMTID) for the **DocumentSummaryInformation** property set is **D5CDD502-2E9C-101B-9397-08002B2CF9AE**.</span></span>

<span data-ttu-id="d4052-111">Die Deklaration für diesen Wert ist in den bereitgestellten Header Dateien als **fmtid \_ docsummaryinformation** verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d4052-111">The declaration for this value is available in the provided header files as **FMTID\_DocSummaryInformation**.</span></span> <span data-ttu-id="d4052-112">Weitere Informationen finden Sie unter [Namen in IStorage](names-in-istorage.md), [Eigenschaften Satz für Zusammenfassungs Informationen](the-summary-information-property-set.md), [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) und [Format](format-identifiers.md)Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="d4052-112">For more information, see [Names in IStorage](names-in-istorage.md), [The Summary Information Property Set](the-summary-information-property-set.md), [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) and [Format Identifiers](format-identifiers.md).</span></span>

<span data-ttu-id="d4052-113">Dieser Stream verfügt auch über einen separaten Abschnitt für die benutzerdefinierten benutzerdefinierten Eigenschaften, wie in den Eigenschaften Sätzen **documentsummaryinformation** und **UserDefined** .</span><span class="sxs-lookup"><span data-stu-id="d4052-113">This stream also has a separate section for the custom-user-defined properties as in the **DocumentSummaryInformation** and **UserDefined** property sets.</span></span> <span data-ttu-id="d4052-114">Dieser Abschnitt wird in der [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) -Schnittstelle als separater Eigenschaften Satz mit der folgenden fmtid angezeigt (verfügbar als **fmtid \_ UserDefinedProperties**): **D5CDD505-2E9C-101B-9397-08002B2CF9AE**.</span><span class="sxs-lookup"><span data-stu-id="d4052-114">This section appears in the [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) interface as a separate property set, with the following FMTID (available as **FMTID\_UserDefinedProperties**): **D5CDD505-2E9C-101B-9397-08002B2CF9AE**.</span></span>

<span data-ttu-id="d4052-115">Diese beiden Eigenschaften Sätze sind die einzigen, für die ein einzelner Stream mehrere Eigenschaften Sätze enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="d4052-115">These two property sets are the only ones for which a single stream can hold multiple property sets.</span></span> <span data-ttu-id="d4052-116">Die Tatsache, dass sich diese zwei Eigenschafts Sätze in einem einzigen Stream befinden, wirkt sich auf das Verhalten der **IPropertySetStorage** -Schnittstelle aus.</span><span class="sxs-lookup"><span data-stu-id="d4052-116">The fact that these two property sets are in a single stream affects the behavior of the **IPropertySetStorage** interface.</span></span> <span data-ttu-id="d4052-117">Weitere Informationen finden Sie unter [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage).</span><span class="sxs-lookup"><span data-stu-id="d4052-117">For more information, see [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage).</span></span>

<span data-ttu-id="d4052-118">In der folgenden Tabelle werden die hinzugefügten Eigenschaften für den **documentsummaryinformation** -und den **UserDefined** -Eigenschaften Satz aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="d4052-118">The following table lists the added properties to the **DocumentSummaryInformation** and **UserDefined** property set.</span></span> <span data-ttu-id="d4052-119">Wie im **SummaryInformation** -Eigenschaften Satz werden die Namen in der Regel nicht im Eigenschaften Satz gespeichert, sondern aus dem Eigenschaften Bezeichner abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="d4052-119">As in the **SummaryInformation** property set, the names are not typically stored in the property set, but are inferred from the property identifier.</span></span>



| <span data-ttu-id="d4052-120">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="d4052-120">Property name</span></span>      | <span data-ttu-id="d4052-121">Eigenschaftsbezeichner</span><span class="sxs-lookup"><span data-stu-id="d4052-121">Property identifier</span></span>     | <span data-ttu-id="d4052-122">Eigenschafts Bezeichnerwert</span><span class="sxs-lookup"><span data-stu-id="d4052-122">Property identifier value</span></span> | <span data-ttu-id="d4052-123">Varianttyp</span><span class="sxs-lookup"><span data-stu-id="d4052-123">VARIANT type</span></span>                      |
|--------------------|-------------------------|---------------------------|-----------------------------------|
| <span data-ttu-id="d4052-124">Category</span><span class="sxs-lookup"><span data-stu-id="d4052-124">Category</span></span>           | <span data-ttu-id="d4052-125">**piddsi- \_ Kategorie**</span><span class="sxs-lookup"><span data-stu-id="d4052-125">**PIDDSI\_CATEGORY**</span></span>    | <span data-ttu-id="d4052-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="d4052-126">0x00000002</span></span>                | <span data-ttu-id="d4052-127">**VT \_ LPSTR**</span><span class="sxs-lookup"><span data-stu-id="d4052-127">**VT\_LPSTR**</span></span>                     |
| <span data-ttu-id="d4052-128">PresentationTarget</span><span class="sxs-lookup"><span data-stu-id="d4052-128">PresentationTarget</span></span> | <span data-ttu-id="d4052-129">**piddsi- \_ präformat**</span><span class="sxs-lookup"><span data-stu-id="d4052-129">**PIDDSI\_PRESFORMAT**</span></span>  | <span data-ttu-id="d4052-130">0x00000003</span><span class="sxs-lookup"><span data-stu-id="d4052-130">0x00000003</span></span>                | <span data-ttu-id="d4052-131">**VT \_ LPSTR**</span><span class="sxs-lookup"><span data-stu-id="d4052-131">**VT\_LPSTR**</span></span>                     |
| <span data-ttu-id="d4052-132">Byte</span><span class="sxs-lookup"><span data-stu-id="d4052-132">Bytes</span></span>              | <span data-ttu-id="d4052-133">**piddsi \_ byteCount**</span><span class="sxs-lookup"><span data-stu-id="d4052-133">**PIDDSI\_BYTECOUNT**</span></span>   | <span data-ttu-id="d4052-134">0x00000004</span><span class="sxs-lookup"><span data-stu-id="d4052-134">0x00000004</span></span>                | <span data-ttu-id="d4052-135">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="d4052-135">**VT\_I4**</span></span>                        |
| <span data-ttu-id="d4052-136">Linien</span><span class="sxs-lookup"><span data-stu-id="d4052-136">Lines</span></span>              | <span data-ttu-id="d4052-137">**piddsi \_ LineCount**</span><span class="sxs-lookup"><span data-stu-id="d4052-137">**PIDDSI\_LINECOUNT**</span></span>   | <span data-ttu-id="d4052-138">0x00000005</span><span class="sxs-lookup"><span data-stu-id="d4052-138">0x00000005</span></span>                | <span data-ttu-id="d4052-139">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="d4052-139">**VT\_I4**</span></span>                        |
| <span data-ttu-id="d4052-140">Absätze</span><span class="sxs-lookup"><span data-stu-id="d4052-140">Paragraphs</span></span>         | <span data-ttu-id="d4052-141">**piddsi- \_ Parser**</span><span class="sxs-lookup"><span data-stu-id="d4052-141">**PIDDSI\_PARCOUNT**</span></span>    | <span data-ttu-id="d4052-142">0x00000006</span><span class="sxs-lookup"><span data-stu-id="d4052-142">0x00000006</span></span>                | <span data-ttu-id="d4052-143">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="d4052-143">**VT\_I4**</span></span>                        |
| <span data-ttu-id="d4052-144">Folien</span><span class="sxs-lookup"><span data-stu-id="d4052-144">Slides</span></span>             | <span data-ttu-id="d4052-145">**piddsi- \_ diascount**</span><span class="sxs-lookup"><span data-stu-id="d4052-145">**PIDDSI\_SLIDECOUNT**</span></span>  | <span data-ttu-id="d4052-146">0x00000007</span><span class="sxs-lookup"><span data-stu-id="d4052-146">0x00000007</span></span>                | <span data-ttu-id="d4052-147">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="d4052-147">**VT\_I4**</span></span>                        |
| <span data-ttu-id="d4052-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="d4052-148">Notes</span></span>              | <span data-ttu-id="d4052-149">**piddsi- \_ noteCount**</span><span class="sxs-lookup"><span data-stu-id="d4052-149">**PIDDSI\_NOTECOUNT**</span></span>   | <span data-ttu-id="d4052-150">0x00000008</span><span class="sxs-lookup"><span data-stu-id="d4052-150">0x00000008</span></span>                | <span data-ttu-id="d4052-151">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="d4052-151">**VT\_I4**</span></span>                        |
| <span data-ttu-id="d4052-152">Hiddenfolien</span><span class="sxs-lookup"><span data-stu-id="d4052-152">HiddenSlides</span></span>       | <span data-ttu-id="d4052-153">**piddsi \_ hiddencount**</span><span class="sxs-lookup"><span data-stu-id="d4052-153">**PIDDSI\_HIDDENCOUNT**</span></span> | <span data-ttu-id="d4052-154">0x00000009</span><span class="sxs-lookup"><span data-stu-id="d4052-154">0x00000009</span></span>                | <span data-ttu-id="d4052-155">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="d4052-155">**VT\_I4**</span></span>                        |
| <span data-ttu-id="d4052-156">Mmclips</span><span class="sxs-lookup"><span data-stu-id="d4052-156">MMClips</span></span>            | <span data-ttu-id="d4052-157">**piddsi \_ mmclipcount**</span><span class="sxs-lookup"><span data-stu-id="d4052-157">**PIDDSI\_MMCLIPCOUNT**</span></span> | <span data-ttu-id="d4052-158">0x0000000A</span><span class="sxs-lookup"><span data-stu-id="d4052-158">0x0000000A</span></span>                | <span data-ttu-id="d4052-159">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="d4052-159">**VT\_I4**</span></span>                        |
| <span data-ttu-id="d4052-160">Scalecrop</span><span class="sxs-lookup"><span data-stu-id="d4052-160">ScaleCrop</span></span>          | <span data-ttu-id="d4052-161">**piddsi- \_ Skala**</span><span class="sxs-lookup"><span data-stu-id="d4052-161">**PIDDSI\_SCALE**</span></span>       | <span data-ttu-id="d4052-162">0x0000000b</span><span class="sxs-lookup"><span data-stu-id="d4052-162">0x0000000B</span></span>                | <span data-ttu-id="d4052-163">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="d4052-163">**VT\_BOOL**</span></span>                      |
| <span data-ttu-id="d4052-164">Headingpaare</span><span class="sxs-lookup"><span data-stu-id="d4052-164">HeadingPairs</span></span>       | <span data-ttu-id="d4052-165">**piddsi \_ headingpair**</span><span class="sxs-lookup"><span data-stu-id="d4052-165">**PIDDSI\_HEADINGPAIR**</span></span> | <span data-ttu-id="d4052-166">0x0000000c</span><span class="sxs-lookup"><span data-stu-id="d4052-166">0x0000000C</span></span>                | <span data-ttu-id="d4052-167">**VT \_ Variant** \| **VT- \_ Vektor**</span><span class="sxs-lookup"><span data-stu-id="d4052-167">**VT\_VARIANT** \| **VT\_VECTOR**</span></span> |
| <span data-ttu-id="d4052-168">Titlesofparts</span><span class="sxs-lookup"><span data-stu-id="d4052-168">TitlesofParts</span></span>      | <span data-ttu-id="d4052-169">**piddsi \_ docparts**</span><span class="sxs-lookup"><span data-stu-id="d4052-169">**PIDDSI\_DOCPARTS**</span></span>    | <span data-ttu-id="d4052-170">0x0000000d</span><span class="sxs-lookup"><span data-stu-id="d4052-170">0x0000000D</span></span>                | <span data-ttu-id="d4052-171">**VT \_ Vector** \| **VT \_ LPSTR**</span><span class="sxs-lookup"><span data-stu-id="d4052-171">**VT\_VECTOR** \| **VT\_LPSTR**</span></span>   |
| <span data-ttu-id="d4052-172">Manager</span><span class="sxs-lookup"><span data-stu-id="d4052-172">Manager</span></span>            | <span data-ttu-id="d4052-173">**piddsi- \_ Manager**</span><span class="sxs-lookup"><span data-stu-id="d4052-173">**PIDDSI\_MANAGER**</span></span>     | <span data-ttu-id="d4052-174">0x0000000e</span><span class="sxs-lookup"><span data-stu-id="d4052-174">0x0000000E</span></span>                | <span data-ttu-id="d4052-175">**VT \_ LPSTR**</span><span class="sxs-lookup"><span data-stu-id="d4052-175">**VT\_LPSTR**</span></span>                     |
| <span data-ttu-id="d4052-176">Company</span><span class="sxs-lookup"><span data-stu-id="d4052-176">Company</span></span>            | <span data-ttu-id="d4052-177">**piddsi- \_ Unternehmen**</span><span class="sxs-lookup"><span data-stu-id="d4052-177">**PIDDSI\_COMPANY**</span></span>     | <span data-ttu-id="d4052-178">0x0000000f</span><span class="sxs-lookup"><span data-stu-id="d4052-178">0x0000000F</span></span>                | <span data-ttu-id="d4052-179">**VT \_ LPSTR**</span><span class="sxs-lookup"><span data-stu-id="d4052-179">**VT\_LPSTR**</span></span>                     |
| <span data-ttu-id="d4052-180">Linksupdedate</span><span class="sxs-lookup"><span data-stu-id="d4052-180">LinksUpToDate</span></span>      | <span data-ttu-id="d4052-181">**piddsi \_ linksdirty**</span><span class="sxs-lookup"><span data-stu-id="d4052-181">**PIDDSI\_LINKSDIRTY**</span></span>  | <span data-ttu-id="d4052-182">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d4052-182">0x00000010</span></span>                | <span data-ttu-id="d4052-183">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="d4052-183">**VT\_BOOL**</span></span>                      |



 

<span data-ttu-id="d4052-184">Diese Eigenschaften haben folgende Verwendungsmöglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="d4052-184">These properties have the following uses:</span></span>

<dl> <dt>

<span data-ttu-id="d4052-185"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Kategorie</span><span class="sxs-lookup"><span data-stu-id="d4052-185"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Category</span></span>
</dt> <dd>

<span data-ttu-id="d4052-186">Eine vom Benutzer eingegebene Text Zeichenfolge, die angibt, zu welcher Kategorie die Datei gehört (Memo, Vorschlag usw.).</span><span class="sxs-lookup"><span data-stu-id="d4052-186">A text string typed by the user that indicates what category the file belongs to (memo, proposal, and so on).</span></span> <span data-ttu-id="d4052-187">Es ist hilfreich, um Dateien desselben Typs zu suchen.</span><span class="sxs-lookup"><span data-stu-id="d4052-187">It is useful for finding files of same type.</span></span>

</dd> <dt>

<span data-ttu-id="d4052-188"><span id="PresentationTarget"></span><span id="presentationtarget"></span><span id="PRESENTATIONTARGET"></span>PresentationTarget</span><span class="sxs-lookup"><span data-stu-id="d4052-188"><span id="PresentationTarget"></span><span id="presentationtarget"></span><span id="PRESENTATIONTARGET"></span>PresentationTarget</span></span>
</dt> <dd>

<span data-ttu-id="d4052-189">Zielformat für die Präsentation (35mm, Drucker, Video usw.).</span><span class="sxs-lookup"><span data-stu-id="d4052-189">Target format for presentation (35mm, printer, video, and so on).</span></span>

</dd> <dt>

<span data-ttu-id="d4052-190"><span id="Bytes"></span><span id="bytes"></span><span id="BYTES"></span>Satz</span><span class="sxs-lookup"><span data-stu-id="d4052-190"><span id="Bytes"></span><span id="bytes"></span><span id="BYTES"></span>Bytes</span></span>
</dt> <dd>

<span data-ttu-id="d4052-191">Die Anzahl von Bytes.</span><span class="sxs-lookup"><span data-stu-id="d4052-191">Number of bytes.</span></span>

</dd> <dt>

<span data-ttu-id="d4052-192"><span id="Lines"></span><span id="lines"></span><span id="LINES"></span>Betreff</span><span class="sxs-lookup"><span data-stu-id="d4052-192"><span id="Lines"></span><span id="lines"></span><span id="LINES"></span>Lines</span></span>
</dt> <dd>

<span data-ttu-id="d4052-193">Anzahl der Zeilen.</span><span class="sxs-lookup"><span data-stu-id="d4052-193">Number of lines.</span></span>

</dd> <dt>

<span data-ttu-id="d4052-194"><span id="Paragraphs"></span><span id="paragraphs"></span><span id="PARAGRAPHS"></span>355</span><span class="sxs-lookup"><span data-stu-id="d4052-194"><span id="Paragraphs"></span><span id="paragraphs"></span><span id="PARAGRAPHS"></span>Paragraphs</span></span>
</dt> <dd>

<span data-ttu-id="d4052-195">Anzahl von Absätzen.</span><span class="sxs-lookup"><span data-stu-id="d4052-195">Number of paragraphs.</span></span>

</dd> <dt>

<span data-ttu-id="d4052-196"><span id="Slides"></span><span id="slides"></span><span id="SLIDES"></span>Führten</span><span class="sxs-lookup"><span data-stu-id="d4052-196"><span id="Slides"></span><span id="slides"></span><span id="SLIDES"></span>Slides</span></span>
</dt> <dd>

<span data-ttu-id="d4052-197">Anzahl der Folien.</span><span class="sxs-lookup"><span data-stu-id="d4052-197">Number of slides.</span></span>

</dd> <dt>

<span data-ttu-id="d4052-198"><span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="d4052-198"><span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>Notes</span></span>
</dt> <dd>

<span data-ttu-id="d4052-199">Anzahl der Seiten, die Notizen enthalten.</span><span class="sxs-lookup"><span data-stu-id="d4052-199">Number of pages that contain notes.</span></span>

</dd> <dt>

<span data-ttu-id="d4052-200"><span id="HiddenSlides"></span><span id="hiddenslides"></span><span id="HIDDENSLIDES"></span>Hiddenfolien</span><span class="sxs-lookup"><span data-stu-id="d4052-200"><span id="HiddenSlides"></span><span id="hiddenslides"></span><span id="HIDDENSLIDES"></span>HiddenSlides</span></span>
</dt> <dd>

<span data-ttu-id="d4052-201">Anzahl der ausgeblendeten Folien.</span><span class="sxs-lookup"><span data-stu-id="d4052-201">Number of slides that are hidden.</span></span>

</dd> <dt>

<span data-ttu-id="d4052-202"><span id="MMClips"></span><span id="mmclips"></span><span id="MMCLIPS"></span>Mmclips</span><span class="sxs-lookup"><span data-stu-id="d4052-202"><span id="MMClips"></span><span id="mmclips"></span><span id="MMCLIPS"></span>MMClips</span></span>
</dt> <dd>

<span data-ttu-id="d4052-203">Anzahl der Sound-oder Videoclips.</span><span class="sxs-lookup"><span data-stu-id="d4052-203">Number of sound or video clips.</span></span>

</dd> <dt>

<span data-ttu-id="d4052-204"><span id="ScaleCrop"></span><span id="scalecrop"></span><span id="SCALECROP"></span>Scalecrop</span><span class="sxs-lookup"><span data-stu-id="d4052-204"><span id="ScaleCrop"></span><span id="scalecrop"></span><span id="SCALECROP"></span>ScaleCrop</span></span>
</dt> <dd>

<span data-ttu-id="d4052-205">Legen Sie diese Einstellung auf true (-1) fest, wenn die Skalierung der Miniaturansicht gewünscht wird.</span><span class="sxs-lookup"><span data-stu-id="d4052-205">Set to True (-1) when scaling of the thumbnail is desired.</span></span> <span data-ttu-id="d4052-206">Wenn nicht festgelegt, ist das Zuschneiden erwünscht.</span><span class="sxs-lookup"><span data-stu-id="d4052-206">If not set, cropping is desired.</span></span>

</dd> <dt>

<span data-ttu-id="d4052-207"><span id="HeadingPairs"></span><span id="headingpairs"></span><span id="HEADINGPAIRS"></span>Headingpaare</span><span class="sxs-lookup"><span data-stu-id="d4052-207"><span id="HeadingPairs"></span><span id="headingpairs"></span><span id="HEADINGPAIRS"></span>HeadingPairs</span></span>
</dt> <dd>

<span data-ttu-id="d4052-208">Intern verwendete Eigenschaft, die die Gruppierung verschiedener Dokument Teile und die Anzahl der Elemente in jeder Gruppe angibt.</span><span class="sxs-lookup"><span data-stu-id="d4052-208">Internally used property indicating the grouping of different document parts and the number of items in each group.</span></span> <span data-ttu-id="d4052-209">Die Titel der Dokument Teile werden in der **titlesofparts** -Eigenschaft gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d4052-209">The titles of the document parts are stored in the **TitlesofParts** property.</span></span> <span data-ttu-id="d4052-210">Die **headingpairs** -Eigenschaft wird als Vektor von Varianten in sich wiederholenden Paaren von **VT \_ LPSTR** (oder **VT \_ LPWSTR**) und **VT \_ I4** -Werten gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d4052-210">The **HeadingPairs** property is stored as a vector of variants, in repeating pairs of **VT\_LPSTR** (or **VT\_LPWSTR**) and **VT\_I4** values.</span></span> <span data-ttu-id="d4052-211">Der **VT \_ LPSTR** -Wert stellt einen Überschriften Namen dar, und der **VT \_ I4** -Wert gibt die Anzahl der Dokument Teile unter dieser Überschrift an.</span><span class="sxs-lookup"><span data-stu-id="d4052-211">The **VT\_LPSTR** value represents a heading name, and the **VT\_I4** value indicates the count of document parts under that heading.</span></span>

</dd> <dt>

<span data-ttu-id="d4052-212"><span id="TitlesofParts"></span><span id="titlesofparts"></span><span id="TITLESOFPARTS"></span>Titlesofparts</span><span class="sxs-lookup"><span data-stu-id="d4052-212"><span id="TitlesofParts"></span><span id="titlesofparts"></span><span id="TITLESOFPARTS"></span>TitlesofParts</span></span>
</dt> <dd>

<span data-ttu-id="d4052-213">Namen der Dokument Teile.</span><span class="sxs-lookup"><span data-stu-id="d4052-213">Names of document parts.</span></span>

</dd> <dt>

<span data-ttu-id="d4052-214"><span id="Manager"></span><span id="manager"></span><span id="MANAGER"></span>Dienst</span><span class="sxs-lookup"><span data-stu-id="d4052-214"><span id="Manager"></span><span id="manager"></span><span id="MANAGER"></span>Manager</span></span>
</dt> <dd>

<span data-ttu-id="d4052-215">Manager des Projekts.</span><span class="sxs-lookup"><span data-stu-id="d4052-215">Manager of the project.</span></span>

</dd> <dt>

<span data-ttu-id="d4052-216"><span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Geschäfts</span><span class="sxs-lookup"><span data-stu-id="d4052-216"><span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Company</span></span>
</dt> <dd>

<span data-ttu-id="d4052-217">Firmenname.</span><span class="sxs-lookup"><span data-stu-id="d4052-217">Company name.</span></span>

</dd> <dt>

<span data-ttu-id="d4052-218"><span id="LinksUpToDate"></span><span id="linksuptodate"></span><span id="LINKSUPTODATE"></span>Linksupdedate</span><span class="sxs-lookup"><span data-stu-id="d4052-218"><span id="LinksUpToDate"></span><span id="linksuptodate"></span><span id="LINKSUPTODATE"></span>LinksUpToDate</span></span>
</dt> <dd>

<span data-ttu-id="d4052-219">Boolescher Wert, der angibt, ob die benutzerdefinierten Verknüpfungen für alle Anwendungen durch übermäßiges Rauschen behindert werden.</span><span class="sxs-lookup"><span data-stu-id="d4052-219">Boolean value to indicate whether the custom links are hampered by excessive noise, for all applications.</span></span>

> [!Note]  
> <span data-ttu-id="d4052-220">Wie in 12,3 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d4052-220">As described in 12.3.</span></span> <span data-ttu-id="d4052-221">Das serialisierte Format für Eigenschafts Sätze der OLE 2,0-Entwurfs Spezifikation, Vektor Elemente in den Eigenschaften **headingproperties** und **titlesofparts** sollten an 32-Bit-Begrenzungen innerhalb des Eigenschaften Satzes ausgerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="d4052-221">Serialized Format for Property Sets of the OLE 2.0 Design Specification, vector elements in the **HeadingPairs** and **TitlesofParts** properties should be aligned on 32 bit boundaries within the property set.</span></span> <span data-ttu-id="d4052-222">In den Eigenschaften Sätzen **documentsummaryinformation** und **User Defined** müssen diese Elemente jedoch gepackt werden, wenn die Codepage des Eigenschaften Satzes nicht Unicode ist.</span><span class="sxs-lookup"><span data-stu-id="d4052-222">However, in the **DocumentSummaryInformation** and **UserDefined** property sets, when the code page of the property set is not Unicode, these elements must be packed.</span></span>

 

</dd> </dl>

<span data-ttu-id="d4052-223">Der **benutzerdefinierte** Eigenschaften Satz kann verwendet werden, um alle Eigenschaften zu speichern.</span><span class="sxs-lookup"><span data-stu-id="d4052-223">The **UserDefined** property set can be used to hold any properties.</span></span> <span data-ttu-id="d4052-224">In der Regel wird es verwendet, um benannte Eigenschaften zu speichern, die von einem Benutzer erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="d4052-224">Typically, it is used to store named properties created by a user.</span></span>

 

 




