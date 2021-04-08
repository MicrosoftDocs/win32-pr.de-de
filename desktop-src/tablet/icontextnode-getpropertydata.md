---
description: Ruft anwendungsspezifische Daten oder andere Eigenschafts Daten für den angegebenen Bezeichner ab.
ms.assetid: eaf95ff8-7b31-4c05-aa49-0c3bb9e996c0
title: 'Icontextnode:: GetPropertyData-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetPropertyData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 381d137dd73056a2a6f4c2e9cd3746f9f16c5b2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751848"
---
# <a name="icontextnodegetpropertydata-method"></a><span data-ttu-id="55fc1-103">Icontextnode:: GetPropertyData-Methode</span><span class="sxs-lookup"><span data-stu-id="55fc1-103">IContextNode::GetPropertyData method</span></span>

<span data-ttu-id="55fc1-104">Ruft anwendungsspezifische Daten oder andere Eigenschafts Daten für den angegebenen Bezeichner ab.</span><span class="sxs-lookup"><span data-stu-id="55fc1-104">Retrieves application-specific data or other property data for the specified identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="55fc1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="55fc1-105">Syntax</span></span>


```C++
HRESULT GetPropertyData(
  [in]      const GUID  *pPropertyDataId,
  [in, out]       ULONG *pulPropertyDataSize,
  [out]           BYTE  **ppbPropertyData
);
```



## <a name="parameters"></a><span data-ttu-id="55fc1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="55fc1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55fc1-107">*ppropertydataid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="55fc1-107">*pPropertyDataId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55fc1-108">Der Bezeichner für die Daten.</span><span class="sxs-lookup"><span data-stu-id="55fc1-108">The identifier for the data.</span></span>

</dd> <dt>

<span data-ttu-id="55fc1-109">*pulpropertydatasize* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="55fc1-109">*pulPropertyDataSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="55fc1-110">Die Größe der Daten in Bytes.</span><span class="sxs-lookup"><span data-stu-id="55fc1-110">The size of the data in bytes.</span></span> <span data-ttu-id="55fc1-111">Der Wert, der an die Übergabe erfolgt, wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="55fc1-111">The value that is passed in is not used.</span></span>

</dd> <dt>

<span data-ttu-id="55fc1-112">*ppbpropertydata* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="55fc1-112">*ppbPropertyData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="55fc1-113">Ein Zeiger auf ein Array von 8-Bit-Ganzzahlen ohne Vorzeichen, das die Eigenschaften Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="55fc1-113">A pointer to an 8-bit unsigned integer array that contains the property data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55fc1-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="55fc1-114">Return value</span></span>

<span data-ttu-id="55fc1-115">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="55fc1-115">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="55fc1-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="55fc1-116">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="55fc1-117">Um einen Speicherfehler zu vermeiden, verwenden Sie " [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) ", um den Arbeitsspeicher von \* *ppbpropertydata* freizugeben, wenn Sie die Informationen nicht mehr benötigen.</span><span class="sxs-lookup"><span data-stu-id="55fc1-117">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppbPropertyData* when you no longer need the information.</span></span>

 

<span data-ttu-id="55fc1-118">Zusätzlich zum Abrufen von anwendungsspezifischen Daten, die mit [**icontextnode:: AddPropertyData**](icontextnode-addpropertydata.md)hinzugefügt wurden, wird diese Methode verwendet, um allgemeine Eigenschaften abzurufen, die von den [Eigenschaften Konstanten für Kontext Knoten](context-node-properties.md) beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="55fc1-118">In addition to retrieving application-specific data that was added with [**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md), this method is used to retrieve common properties that are described by the [Context Node Properties](context-node-properties.md) constants.</span></span>

<span data-ttu-id="55fc1-119">Zu den Eigenschaften vom Typ "String" gehören:</span><span class="sxs-lookup"><span data-stu-id="55fc1-119">The string-type properties include:</span></span>

-   <span data-ttu-id="55fc1-120">GUID \_ CNP \_ erkenzedstring</span><span class="sxs-lookup"><span data-stu-id="55fc1-120">GUID\_CNP\_RECOGNIZEDSTRING</span></span>
-   <span data-ttu-id="55fc1-121">GUID \_ CNP \_ Shapename</span><span class="sxs-lookup"><span data-stu-id="55fc1-121">GUID\_CNP\_SHAPENAME</span></span>
-   <span data-ttu-id="55fc1-122">GUID \_ AHP \_ analysishintname</span><span class="sxs-lookup"><span data-stu-id="55fc1-122">GUID\_AHP\_ANALYSISHINTNAME</span></span>
-   <span data-ttu-id="55fc1-123">GUID \_ AHP \_ PrefixText</span><span class="sxs-lookup"><span data-stu-id="55fc1-123">GUID\_AHP\_PREFIXTEXT</span></span>
-   <span data-ttu-id="55fc1-124">GUID- \_ AHP- \_ SuffixText</span><span class="sxs-lookup"><span data-stu-id="55fc1-124">GUID\_AHP\_SUFFIXTEXT</span></span>
-   <span data-ttu-id="55fc1-125">GUID- \_ AHP- \_ Faktoid</span><span class="sxs-lookup"><span data-stu-id="55fc1-125">GUID\_AHP\_FACTOID</span></span>

<span data-ttu-id="55fc1-126">Der Rückgabewert ist \**WCHAR \**_. Wenn Sie den Parameter \_ *ppbpropertydata* in \**\* WCHAR* umwandeln,_ ist die zurückgegebene Länge `(length of the string + 1) _ sizeof(WCHAR)` .</span><span class="sxs-lookup"><span data-stu-id="55fc1-126">The return value is \**WCHAR\**_. If you cast the \_*ppbPropertyData* parameter to \**WCHAR\**_ its returned length is `(length of the string + 1) _ sizeof(WCHAR)`.</span></span>

<span data-ttu-id="55fc1-127">Die Eigenschaften des booleschen Typs umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="55fc1-127">The Boolean-type properties include:</span></span>

-   <span data-ttu-id="55fc1-128">GUID \_ AHP \_ overridelta anguageid</span><span class="sxs-lookup"><span data-stu-id="55fc1-128">GUID\_AHP\_OVERRIDELANGUAGEID</span></span>
-   <span data-ttu-id="55fc1-129">GUID \_ AHP \_ coercetofaktoid</span><span class="sxs-lookup"><span data-stu-id="55fc1-129">GUID\_AHP\_COERCETOFACTOID</span></span>
-   <span data-ttu-id="55fc1-130">GUID- \_ AHP- \_ wordmode</span><span class="sxs-lookup"><span data-stu-id="55fc1-130">GUID\_AHP\_WORDMODE</span></span>

<span data-ttu-id="55fc1-131">Der Rückgabewert ist **Variant \_ bool**.</span><span class="sxs-lookup"><span data-stu-id="55fc1-131">The return value is **VARIANT\_BOOL**.</span></span> <span data-ttu-id="55fc1-132">Wenn Sie den Parameter \* *ppbpropertydata* in \**Variant \_ \* bool* _ umwandeln, ist die zurückgegebene Länge `sizeof(VARIANT_BOOL)` .</span><span class="sxs-lookup"><span data-stu-id="55fc1-132">If you cast the \**ppbPropertyData* parameter to \**VARIANT\_BOOL\** _ its returned length is `sizeof(VARIANT_BOOL)`.</span></span>

<span data-ttu-id="55fc1-133">Der GUID- \_ AHP \_ -Leitfaden ist eine Eigenschaft vom Typ "Guide".</span><span class="sxs-lookup"><span data-stu-id="55fc1-133">GUID\_AHP\_GUIDE is a guide-type property.</span></span> <span data-ttu-id="55fc1-134">Der Rückgabewert ist _*inkanalysiserkentionguide \**_.</span><span class="sxs-lookup"><span data-stu-id="55fc1-134">The return value is _*InkAnalysisRecognitionGuide\**_.</span></span> <span data-ttu-id="55fc1-135">Wenn Sie den Parameter \_ *ppbpropertydata* in \**inkanalysiserkentionguide \** _ umwandeln, ist die zurückgegebene Länge `sizeof(InkAnalysisRecognitionGuide)` .</span><span class="sxs-lookup"><span data-stu-id="55fc1-135">If you cast the \_*ppbPropertyData* parameter to \**InkAnalysisRecognitionGuide\** _ its returned length is `sizeof(InkAnalysisRecognitionGuide)`.</span></span>

<span data-ttu-id="55fc1-136">Eigenschaften vom Typ "Integer" umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="55fc1-136">Integer-type properties include:</span></span>

-   <span data-ttu-id="55fc1-137">GUID \_ CNP \_ LineNumber</span><span class="sxs-lookup"><span data-stu-id="55fc1-137">GUID\_CNP\_LINENUMBER</span></span>
-   <span data-ttu-id="55fc1-138">GUID \_ CNP \_ PointsPerInch</span><span class="sxs-lookup"><span data-stu-id="55fc1-138">GUID\_CNP\_POINTSPERINCH</span></span>
-   <span data-ttu-id="55fc1-139">GUID \_ CNP \_ conficelevel</span><span class="sxs-lookup"><span data-stu-id="55fc1-139">GUID\_CNP\_CONFIDENCELEVEL</span></span>
-   <span data-ttu-id="55fc1-140">GUID \_ CNP- \_ Bestätigung</span><span class="sxs-lookup"><span data-stu-id="55fc1-140">GUID\_CNP\_CONFIRMATION</span></span>
-   <span data-ttu-id="55fc1-141">GUID \_ CNP \_ MaximumStrokeCount</span><span class="sxs-lookup"><span data-stu-id="55fc1-141">GUID\_CNP\_MAXIMUMSTROKECOUNT</span></span>
-   <span data-ttu-id="55fc1-142">GUID \_ CNP- \_ Segmentierung</span><span class="sxs-lookup"><span data-stu-id="55fc1-142">GUID\_CNP\_SEGMENTATION</span></span>
-   <span data-ttu-id="55fc1-143">GUID \_ CNP \_ alignmentlevel</span><span class="sxs-lookup"><span data-stu-id="55fc1-143">GUID\_CNP\_ALIGNMENTLEVEL</span></span>

<span data-ttu-id="55fc1-144">Der Rückgabewert ist _*Long \**_.</span><span class="sxs-lookup"><span data-stu-id="55fc1-144">The return value is _*LONG\**_.</span></span> <span data-ttu-id="55fc1-145">Wenn Sie den \_ *ppbpropertydata* -Parameter in \**Long \** _ umwandeln, ist die zurückgegebene Länge `sizeof(LONG)` .</span><span class="sxs-lookup"><span data-stu-id="55fc1-145">If you cast the \_*ppbPropertyData* parameter to \**LONG\** _ its returned length is `sizeof(LONG)`.</span></span>

<span data-ttu-id="55fc1-146">Linienmetriken: Typeigenschaften:</span><span class="sxs-lookup"><span data-stu-id="55fc1-146">Line metrics-type properties include:</span></span>

-   <span data-ttu-id="55fc1-147">GUID \_ CNP-Vorgänger \_</span><span class="sxs-lookup"><span data-stu-id="55fc1-147">GUID\_CNP\_ASCENDERS</span></span>
-   <span data-ttu-id="55fc1-148">GUID \_ CNP-Nachfolger \_</span><span class="sxs-lookup"><span data-stu-id="55fc1-148">GUID\_CNP\_DESCENDERS</span></span>
-   <span data-ttu-id="55fc1-149">GUID \_ CNP- \_ Baseline</span><span class="sxs-lookup"><span data-stu-id="55fc1-149">GUID\_CNP\_BASELINE</span></span>
-   <span data-ttu-id="55fc1-150">GUID \_ CNP- \_ Mittellinie</span><span class="sxs-lookup"><span data-stu-id="55fc1-150">GUID\_CNP\_MIDLINE</span></span>

<span data-ttu-id="55fc1-151">Der Rückgabewert ist _*Long \**_.</span><span class="sxs-lookup"><span data-stu-id="55fc1-151">The return value is _*LONG\**_.</span></span> <span data-ttu-id="55fc1-152">Wenn Sie den Parameter " \_ *ppbpropertydata* " in "\**Long \** _" umwandeln, ist die zurückgegebene Länge `sizeof(LONG)_4` . Dies bedeutet, dass (x, y) Werte für die Anfangspunkte, gefolgt von den (x, y)-Werten für die Endpunkte, dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="55fc1-152">If you cast the \_*ppbPropertyData* parameter to \**LONG\** _ its returned length is `sizeof(LONG)_4`, signifying the (x, y) values for the starting points followed by the (x, y) values for the ending points.</span></span>

<span data-ttu-id="55fc1-153">GUID \_ CNP \_ textrecognizerid ist eine **GUID** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="55fc1-153">GUID\_CNP\_TEXTRECOGNIZERID is a **GUID** property.</span></span> <span data-ttu-id="55fc1-154">Der Rückgabewert ist \**GUID \**_. Wenn Sie den Parameter \_ *ppbpropertydata* in \**\* GUID* umwandeln,_ ist die zurückgegebene Länge `sizeof(GUID)` .</span><span class="sxs-lookup"><span data-stu-id="55fc1-154">The return value is \**GUID\**_. If you cast the \_*ppbPropertyData* parameter to \**GUID\**_ its returned length is `sizeof(GUID)`.</span></span>

<span data-ttu-id="55fc1-155">GUID \_ CNP \_ rotatedboundingbox ist eine gedrehte Begrenzungsfeld Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="55fc1-155">GUID\_CNP\_ROTATEDBOUNDINGBOX is a rotated bounding box property.</span></span> <span data-ttu-id="55fc1-156">Der Rückgabewert ist _*Long \**_.</span><span class="sxs-lookup"><span data-stu-id="55fc1-156">The return value is _*LONG\**_.</span></span> <span data-ttu-id="55fc1-157">Beim Umwandeln des \_ *ppbpropertydata* -Parameters in \*\* \* Long\* _ ist die zurückgegebene Länge `sizeof(LONG)_8` . Dies bedeutet, dass (x, y) Werte für die vier Ecken des Felds gekennzeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="55fc1-157">If you cast the \_*ppbPropertyData* parameter to \**LONG\** _ its returned length is `sizeof(LONG)_8`, signifying the (x, y) values for the four corners of the box.</span></span>

<span data-ttu-id="55fc1-158">Der GUID \_ CNP- \_ Hotpoint ist eine Hot Point-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="55fc1-158">GUID\_CNP\_HOTPOINT is a hot point property.</span></span> <span data-ttu-id="55fc1-159">Der Rückgabewert ist \**Long \**_. Wenn Sie den \_ *ppbpropertydata* -Parameter in *\** \*_ zurück umwandeln, ist die zurückgegebene Länge `sizeof(LONG)_2` , die die (x, y)-Werte für den Punkt bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="55fc1-159">The return value is \**LONG\**_. If you cast the \_*ppbPropertyData* parameter to \**LONG\**_ its returned length is `sizeof(LONG)_2`, signifying the (x, y) values for the point.</span></span>

<span data-ttu-id="55fc1-160">GUID \_ AHP \_ WordList ist eine Word-Listen Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="55fc1-160">GUID\_AHP\_WORDLIST is a word list property.</span></span> <span data-ttu-id="55fc1-161">Der Rückgabewert ist \**WCHAR \**_. Wenn Sie den Parameter \_ *ppbpropertydata* in \**\* WCHAR*_ umwandeln, ist die zurückgegebene Länge `n _ sizeof(WCHAR)` , wobei `n` die Summe der Zeichen folgen Längen der Anzahl von Zeichen folgen in der Liste plus 1 für jedes **null** -Beendigungs Zeichen für jede Zeichenfolge ist.</span><span class="sxs-lookup"><span data-stu-id="55fc1-161">The return value is \**WCHAR\**_. If you cast the \_*ppbPropertyData* parameter to \**WCHAR\**_ its returned length is `n _ sizeof(WCHAR)`, where `n` is the sum of the string lengths of the number of strings in the list plus 1 for each **NULL** termination character for each string.</span></span>

## <a name="examples"></a><span data-ttu-id="55fc1-162">Beispiele</span><span class="sxs-lookup"><span data-stu-id="55fc1-162">Examples</span></span>

<span data-ttu-id="55fc1-163">Dieses Beispiel zeigt eine Methode, die auf die alignmentlevel-Kontext Knoten Eigenschaft eines Absatz Kontext-Knoten Typs zugreift.</span><span class="sxs-lookup"><span data-stu-id="55fc1-163">This example shows a method that accesses the AlignmentLevel context node property of a Paragraph context node type.</span></span>


```C++
// Checks a paragraph context node's alignment level property.
// Only paragraph type context nodes contain the alignment level property.
HRESULT CMyClass::ExploreParagraphNode(
    IContextNode *pParagraphNode)
{
    // Get the AlignmentLevel property data for the paragraph.
    LONG * alignmentLevel = NULL;
    ULONG ulDataLen = 0;

    HRESULT hr = pParagraphNode->GetPropertyData(
        (const GUID*)&GUID_CNP_ALIGNMENTLEVEL,
        &ulDataLen,
        (BYTE**)&alignmentLevel);

    if( FAILED(hr) ||
        ulDataLen != sizeof(LONG) ||
        alignmentLevel == NULL )
    {
        // Insert code that handles an error here.
    }
    else
    {
        // Insert code that uses the alignment level here.
    }

    // Free the memory allocated for the property data.
    ::CoTaskMemFree(alignmentLevel);

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="55fc1-164">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="55fc1-164">Requirements</span></span>



| <span data-ttu-id="55fc1-165">Anforderung</span><span class="sxs-lookup"><span data-stu-id="55fc1-165">Requirement</span></span> | <span data-ttu-id="55fc1-166">Wert</span><span class="sxs-lookup"><span data-stu-id="55fc1-166">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55fc1-167">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="55fc1-167">Minimum supported client</span></span><br/> | <span data-ttu-id="55fc1-168">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="55fc1-168">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="55fc1-169">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="55fc1-169">Minimum supported server</span></span><br/> | <span data-ttu-id="55fc1-170">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="55fc1-170">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="55fc1-171">Header</span><span class="sxs-lookup"><span data-stu-id="55fc1-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="55fc1-172"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="55fc1-172"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="55fc1-173">DLL</span><span class="sxs-lookup"><span data-stu-id="55fc1-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55fc1-174"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55fc1-174"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="55fc1-175">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55fc1-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55fc1-176">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="55fc1-176">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="55fc1-177">**Icontextnode:: AddPropertyData**</span><span class="sxs-lookup"><span data-stu-id="55fc1-177">**IContextNode::AddPropertyData**</span></span>](icontextnode-addpropertydata.md)
</dt> <dt>

[<span data-ttu-id="55fc1-178">**Icontextnode:: RemovePropertyData**</span><span class="sxs-lookup"><span data-stu-id="55fc1-178">**IContextNode::RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)
</dt> <dt>

[<span data-ttu-id="55fc1-179">**Icontextnode:: GetPropertyDataIds**</span><span class="sxs-lookup"><span data-stu-id="55fc1-179">**IContextNode::GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)
</dt> <dt>

[<span data-ttu-id="55fc1-180">**Icontextnode:: ContainsPropertyData**</span><span class="sxs-lookup"><span data-stu-id="55fc1-180">**IContextNode::ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)
</dt> <dt>

[<span data-ttu-id="55fc1-181">**Icontextnode:: loadpropertiesdata**</span><span class="sxs-lookup"><span data-stu-id="55fc1-181">**IContextNode::LoadPropertiesData**</span></span>](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="55fc1-182">**Icontextnode:: savepropertiesdata**</span><span class="sxs-lookup"><span data-stu-id="55fc1-182">**IContextNode::SavePropertiesData**</span></span>](icontextnode-savepropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="55fc1-183">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="55fc1-183">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

