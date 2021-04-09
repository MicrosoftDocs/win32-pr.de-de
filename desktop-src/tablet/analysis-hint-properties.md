---
description: 'Definiert Global Unique Identifier (GUIDs) für Eigenschaften eines Analyse Hinweis Knotens (siehe icontextnode:: GetType).'
ms.assetid: 8300c792-a741-49de-a03b-f4840ea5d647
title: Eigenschaften des Analysis-Hinweises (iaguid. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_AHP_ALLOWPARTIALDICTIONARYTERMS
- GUID_AHP_ANALYSISHINTNAME
- GUID_AHP_COERCETOFACTOID
- GUID_AHP_ENABLEDUNICODECHARACTERRANGES
- GUID_AHP_FACTOID
- GUID_AHP_GUIDE
- GUID_AHP_PREFIXTEXT
- GUID_AHP_SUFFIXTEXT
- GUID_AHP_TOPINKBREAKSONLY
- GUID_AHP_WORDLIST
- GUID_AHP_WORDMODE
api_type:
- HeaderDef
api_location:
- iaguid.h
ms.openlocfilehash: 8a7a25cfa94bb7f2354418ded2b35e3137364901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958638"
---
# <a name="analysis-hint-properties"></a><span data-ttu-id="ae671-103">Eigenschaften des Analyse Hinweises</span><span class="sxs-lookup"><span data-stu-id="ae671-103">Analysis Hint Properties</span></span>

<span data-ttu-id="ae671-104">Definiert Global Unique Identifier (GUIDs) für Eigenschaften eines Analyse Hinweis Knotens (siehe [**icontextnode:: GetType**](icontextnode-gettype.md)).</span><span class="sxs-lookup"><span data-stu-id="ae671-104">Defines globally unique identifiers (GUIDs) for properties of an analysis hint node (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span>

<span data-ttu-id="ae671-105">In der folgenden Tabelle werden die von den einzelnen Konstanten referenzierten Informationen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ae671-105">The following table describes information referenced by each constant.</span></span>



| <span data-ttu-id="ae671-106">Konstante</span><span class="sxs-lookup"><span data-stu-id="ae671-106">Constant</span></span>                                                                                                                                                                                                                                  | <span data-ttu-id="ae671-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ae671-107">Description</span></span>                                                                                                                                               |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_AHP_ALLOWPARTIALDICTIONARYTERMS"></span><span id="guid_ahp_allowpartialdictionaryterms"></span><dl> <span data-ttu-id="ae671-108"><dt>**GUID \_ AHP \_ allowpartialdiktattionaryterms**</dt></span><span class="sxs-lookup"><span data-stu-id="ae671-108"><dt>**GUID\_AHP\_ALLOWPARTIALDICTIONARYTERMS**</dt></span></span> </dl>       | <span data-ttu-id="ae671-109">Gibt an, ob partielle Wörterbuch Begriffe in einem Analyse Hinweis zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="ae671-109">Whether partial dictionary terms are allowed on an analysis hint.</span></span><br/>                                                                              |
| <span id="GUID_AHP_ANALYSISHINTNAME"></span><span id="guid_ahp_analysishintname"></span><dl> <span data-ttu-id="ae671-110"><dt>**GUID \_ AHP \_ analysishintname**</dt></span><span class="sxs-lookup"><span data-stu-id="ae671-110"><dt>**GUID\_AHP\_ANALYSISHINTNAME**</dt></span></span> </dl>                                        | <span data-ttu-id="ae671-111">Der Name eines Analyse Hinweises.</span><span class="sxs-lookup"><span data-stu-id="ae671-111">The name of an analysis hint.</span></span><br/>                                                                                                                  |
| <span id="GUID_AHP_COERCETOFACTOID"></span><span id="guid_ahp_coercetofactoid"></span><dl> <span data-ttu-id="ae671-112"><dt>**GUID \_ AHP \_ coercetofaktoid**</dt></span><span class="sxs-lookup"><span data-stu-id="ae671-112"><dt>**GUID\_AHP\_COERCETOFACTOID**</dt></span></span> </dl>                                           | <span data-ttu-id="ae671-113">Gibt an, ob der Ink Analyzer seine Analyse von frei Hand Eingaben innerhalb des Hinweis Bereichs auf das Faktoid beschränkt.</span><span class="sxs-lookup"><span data-stu-id="ae671-113">Whether the ink analyzer limits its analysis of ink within the hint's area to conform to the factoid.</span></span><br/>                                          |
| <span id="GUID_AHP_ENABLEDUNICODECHARACTERRANGES"></span><span id="guid_ahp_enabledunicodecharacterranges"></span><dl> <span data-ttu-id="ae671-114"><dt>**GUID \_ AHP \_ enabledunicode~ terranges**</dt></span><span class="sxs-lookup"><span data-stu-id="ae671-114"><dt>**GUID\_AHP\_ENABLEDUNICODECHARACTERRANGES**</dt></span></span> </dl> | <span data-ttu-id="ae671-115">Der-Hinweis enthält ein Zeichen Array, das den eingeschränkten Satz von unterstützter Unicode-Zeichensätze darstellt, die von diesem InkRecognizer unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="ae671-115">The hint contains an array of characters that represent the restricted set of supported unicode character set supported by this InkRecognizer.</span></span><br/> |
| <span id="GUID_AHP_FACTOID"></span><span id="guid_ahp_factoid"></span><dl> <span data-ttu-id="ae671-116"><dt>**GUID- \_ AHP- \_ Faktoid**</dt></span><span class="sxs-lookup"><span data-stu-id="ae671-116"><dt>**GUID\_AHP\_FACTOID**</dt></span></span> </dl>                                                                   | <span data-ttu-id="ae671-117">Die Faktoid eines Analyse Hinweises.</span><span class="sxs-lookup"><span data-stu-id="ae671-117">The factoid on an analysis hint.</span></span><br/>                                                                                                               |
| <span id="GUID_AHP_GUIDE"></span><span id="guid_ahp_guide"></span><dl> <span data-ttu-id="ae671-118"><dt>**GUID- \_ AHP- \_ Leitfaden**</dt></span><span class="sxs-lookup"><span data-stu-id="ae671-118"><dt>**GUID\_AHP\_GUIDE**</dt></span></span> </dl>                                                                         | <span data-ttu-id="ae671-119">Die [**inkanalysiserkenzerguide**](inkanalysisrecognizerguide.md) -Struktur, die den Leitfaden für einen Analyse Hinweis darstellt.</span><span class="sxs-lookup"><span data-stu-id="ae671-119">The [**InkAnalysisRecognizerGuide**](inkanalysisrecognizerguide.md) structure that represents the guide for an analysis hint.</span></span><br/>                 |
| <span id="GUID_AHP_PREFIXTEXT"></span><span id="guid_ahp_prefixtext"></span><dl> <span data-ttu-id="ae671-120"><dt>**GUID \_ AHP \_ PrefixText**</dt></span><span class="sxs-lookup"><span data-stu-id="ae671-120"><dt>**GUID\_AHP\_PREFIXTEXT**</dt></span></span> </dl>                                                          | <span data-ttu-id="ae671-121">Der Präfix Text eines Analyse Hinweises.</span><span class="sxs-lookup"><span data-stu-id="ae671-121">The prefix text on an analysis hint.</span></span><br/>                                                                                                           |
| <span id="GUID_AHP_SUFFIXTEXT"></span><span id="guid_ahp_suffixtext"></span><dl> <span data-ttu-id="ae671-122"><dt>**GUID- \_ AHP- \_ SuffixText**</dt></span><span class="sxs-lookup"><span data-stu-id="ae671-122"><dt>**GUID\_AHP\_SUFFIXTEXT**</dt></span></span> </dl>                                                          | <span data-ttu-id="ae671-123">Der Suffixtext eines Analyse Hinweises.</span><span class="sxs-lookup"><span data-stu-id="ae671-123">The suffix text on an analysis hint.</span></span><br/>                                                                                                           |
| <span id="GUID_AHP_TOPINKBREAKSONLY"></span><span id="guid_ahp_topinkbreaksonly"></span><dl> <span data-ttu-id="ae671-124"><dt>**GUID \_ AHP \_ TopInkBreaksOnly**</dt></span><span class="sxs-lookup"><span data-stu-id="ae671-124"><dt>**GUID\_AHP\_TOPINKBREAKSONLY**</dt></span></span> </dl>                                        | <span data-ttu-id="ae671-125">Gibt an, ob die mehrere Segmentationen in den frei Hand Erkennungs Ergebnissen deaktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="ae671-125">Whether the multiple segmentations in the ink recognition results are disabled.</span></span><br/>                                                                |
| <span id="GUID_AHP_WORDLIST"></span><span id="guid_ahp_wordlist"></span><dl> <span data-ttu-id="ae671-126"><dt>**GUID- \_ AHP- \_ WordList**</dt></span><span class="sxs-lookup"><span data-stu-id="ae671-126"><dt>**GUID\_AHP\_WORDLIST**</dt></span></span> </dl>                                                                | <span data-ttu-id="ae671-127">Das Zeichen folgen Array, das die Wortliste für einen Analyse Hinweis darstellt.</span><span class="sxs-lookup"><span data-stu-id="ae671-127">The array of strings that represents the word list for an analysis hint.</span></span><br/>                                                                       |
| <span id="GUID_AHP_WORDMODE"></span><span id="guid_ahp_wordmode"></span><dl> <span data-ttu-id="ae671-128"><dt>**GUID- \_ AHP- \_ wordmode**</dt></span><span class="sxs-lookup"><span data-stu-id="ae671-128"><dt>**GUID\_AHP\_WORDMODE**</dt></span></span> </dl>                                                                | <span data-ttu-id="ae671-129">Gibt an, ob die frei Hand Analyseergebnisse von einzelnen Wörtern für einen Analyse Hinweis auf Ergebnisse mit mehreren Wörtern priorisiert.</span><span class="sxs-lookup"><span data-stu-id="ae671-129">Whether the ink analyzer prioritizes single-word results over multiple-word results for an analysis hint.</span></span><br/>                                      |



## <a name="remarks"></a><span data-ttu-id="ae671-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ae671-130">Remarks</span></span>

<span data-ttu-id="ae671-131">Diese GUIDs werden verwendet, um Eigenschaften zu identifizieren, die von [**iinkanalyzer**](iinkanalyzer.md) für einen Kontext Knoten des Analyse Hinweises festgelegt werden können (siehe [**icontextnode:: GetType**](icontextnode-gettype.md)).</span><span class="sxs-lookup"><span data-stu-id="ae671-131">These GUIDs are used to identify properties that the [**IInkAnalyzer**](iinkanalyzer.md) can set on an analysis hint context node (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span>

<span data-ttu-id="ae671-132">Informationen zum Anzeigen oder Festlegen von Eigenschaften eines [**icontextnode**](icontextnode.md) im Allgemeinen finden Sie unter [Kontext Knoten Eigenschaften](context-node-properties.md).</span><span class="sxs-lookup"><span data-stu-id="ae671-132">To get or set properties of an [**IContextNode**](icontextnode.md) in general, see [Context Node Properties](context-node-properties.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ae671-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ae671-133">Requirements</span></span>



| <span data-ttu-id="ae671-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ae671-134">Requirement</span></span> | <span data-ttu-id="ae671-135">Wert</span><span class="sxs-lookup"><span data-stu-id="ae671-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ae671-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ae671-136">Minimum supported client</span></span><br/> | <span data-ttu-id="ae671-137">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ae671-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ae671-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ae671-138">Minimum supported server</span></span><br/> | <span data-ttu-id="ae671-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ae671-139">None supported</span></span><br/>                                                           |
| <span data-ttu-id="ae671-140">Header</span><span class="sxs-lookup"><span data-stu-id="ae671-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae671-141"><dt>Iaguid. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae671-141"><dt>Iaguid.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae671-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ae671-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae671-143">Kontext Knoten Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ae671-143">Context Node Properties</span></span>](context-node-properties.md)
</dt> <dt>

[<span data-ttu-id="ae671-144">Kontext Knoten Typen</span><span class="sxs-lookup"><span data-stu-id="ae671-144">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="ae671-145">**Iinkanalyzer:: feateanalysishint-Methode**</span><span class="sxs-lookup"><span data-stu-id="ae671-145">**IInkAnalyzer::CreateAnalysisHint Method**</span></span>](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[<span data-ttu-id="ae671-146">**Iinkanalyzer:: getanalysishintsbyname-Methode**</span><span class="sxs-lookup"><span data-stu-id="ae671-146">**IInkAnalyzer::GetAnalysisHintsByName Method**</span></span>](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[<span data-ttu-id="ae671-147">**Icontextnode:: ContainsPropertyData**</span><span class="sxs-lookup"><span data-stu-id="ae671-147">**IContextNode::ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)
</dt> <dt>

[<span data-ttu-id="ae671-148">**Icontextnode:: GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="ae671-148">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="ae671-149">**Icontextnode:: GetPropertyDataIds**</span><span class="sxs-lookup"><span data-stu-id="ae671-149">**IContextNode::GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)
</dt> <dt>

[<span data-ttu-id="ae671-150">**Icontextnode:: loadpropertiesdata**</span><span class="sxs-lookup"><span data-stu-id="ae671-150">**IContextNode::LoadPropertiesData**</span></span>](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="ae671-151">**Icontextnode:: RemovePropertyData**</span><span class="sxs-lookup"><span data-stu-id="ae671-151">**IContextNode::RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)
</dt> <dt>

[<span data-ttu-id="ae671-152">**Icontextnode:: savepropertiesdata**</span><span class="sxs-lookup"><span data-stu-id="ae671-152">**IContextNode::SavePropertiesData**</span></span>](icontextnode-savepropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="ae671-153">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="ae671-153">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




