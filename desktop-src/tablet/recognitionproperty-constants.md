---
description: Definiert Werte, die die Eigenschaften einer Erkennungs Alternative angeben. Die Tablet PC-API (Application Programming Interface) verwendet Global Unique Bezeichner (GUIDs), um Paket Eigenschaften zu identifizieren, die in Automation Konstante Zeichen folgen sind.
ms.assetid: 2bfb0cbf-73a3-4e83-a4e9-f0803bd3dee8
title: Erkentionproperty-Konstanten (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62971276b6348af3d8ac971851d70b03f7b003c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348638"
---
# <a name="recognitionproperty-constants"></a><span data-ttu-id="2bd07-104">Erkentionproperty-Konstanten</span><span class="sxs-lookup"><span data-stu-id="2bd07-104">RecognitionProperty Constants</span></span>

<span data-ttu-id="2bd07-105">Definiert Werte, die die Eigenschaften einer Erkennungs Alternative angeben.</span><span class="sxs-lookup"><span data-stu-id="2bd07-105">Defines values that specify the properties of a recognition alternate.</span></span> <span data-ttu-id="2bd07-106">Die Tablet PC-API (Application Programming Interface) verwendet Global Unique Bezeichner (GUIDs), um Paket Eigenschaften zu identifizieren, die in Automation Konstante Zeichen folgen sind.</span><span class="sxs-lookup"><span data-stu-id="2bd07-106">The Tablet PC application programming interface (API) uses globally unique identifiers (GUIDs) to identify packet properties, which in Automation are constant strings.</span></span>

<span data-ttu-id="2bd07-107">In der folgenden Tabelle sind die verfügbaren Eigenschaften der alternativen Erkennungs Eigenschaft Globally Unique Identifier (GUID) aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="2bd07-107">The following table lists the available recognition alternate property globally unique identifier (GUID) fields.</span></span> <span data-ttu-id="2bd07-108">Verwenden Sie diese GUIDs, um auf Eigenschaften eines [**iinkrecognitionalternate**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate) -Objekts zuzugreifen, indem Sie die [**GetPropertyValue**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-getpropertyvalue) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2bd07-108">Use these GUIDs to access properties of an [**IInkRecognitionAlternate**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate) object by calling the [**GetPropertyValue**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-getpropertyvalue) method.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="2bd07-109">Konstantenname</span><span class="sxs-lookup"><span data-stu-id="2bd07-109">Constant Name</span></span></th>
<th style="text-align: left;"><span data-ttu-id="2bd07-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2bd07-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_LINENUMBER_________"></span><span id="___________inkrecognitionproperty_linenumber_________"></span><dl> <span data-ttu-id="2bd07-111"><dt><strong>INKRECOGNITIONPROPERTY_LINENUMBER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2bd07-111"><dt> <strong>INKRECOGNITIONPROPERTY_LINENUMBER</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="2bd07-112">Der GUID, der die Eigenschaft für die Zeilennummer des <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>iinkrecognitionalternate</strong></a> -Objekts identifiziert.</span><span class="sxs-lookup"><span data-stu-id="2bd07-112">The GUID that identifies the property for the line number of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> object.</span></span> <br/> <span data-ttu-id="2bd07-113">LineNumber gibt die Alternativen zu einer bestimmten Zeilennummer an.</span><span class="sxs-lookup"><span data-stu-id="2bd07-113">LineNumber specifies the alternates with a particular line number.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="2bd07-114">Dieses Feld wird für Erkennungs Modul von ostasiatischen Zeichen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2bd07-114">This field is not supported for recognizers of East Asian characters.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_SEGMENTATION_________"></span><span id="___________inkrecognitionproperty_segmentation_________"></span><dl> <span data-ttu-id="2bd07-115"><dt><strong>INKRECOGNITIONPROPERTY_SEGMENTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2bd07-115"><dt> <strong>INKRECOGNITIONPROPERTY_SEGMENTATION</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="2bd07-116">Der GUID, der die Eigenschaft für die Segmentierung des <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>iinkrecognitionalternate</strong></a> -Objekts identifiziert.</span><span class="sxs-lookup"><span data-stu-id="2bd07-116">The GUID that identifies the property for the segmentation of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> object.</span></span> <br/> <span data-ttu-id="2bd07-117">Segmentierung gibt das grundlegende Freihand Fragment oder die Einheit an, die die Erkennung verwendet, um ein Erkennungs Ergebnis zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2bd07-117">Segmentation specifies the basic ink fragment or unit that the recognizer uses to produce a recognition result.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="2bd07-118">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="2bd07-118">Not implemented.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_HOTPOINT_________"></span><span id="___________inkrecognitionproperty_hotpoint_________"></span><dl> <span data-ttu-id="2bd07-119"><dt><strong>INKRECOGNITIONPROPERTY_HOTPOINT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2bd07-119"><dt> <strong>INKRECOGNITIONPROPERTY_HOTPOINT</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="2bd07-120">Der GUID, der die Eigenschaft für den Erkennungs-Hot Point des <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>iinkrecognitionalternate</strong></a> -Objekts identifiziert.</span><span class="sxs-lookup"><span data-stu-id="2bd07-120">The GUID that identifies the property for the recognition hot point of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> object.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_MAXIMUMSTROKECOUNT_________"></span><span id="___________inkrecognitionproperty_maximumstrokecount_________"></span><dl> <span data-ttu-id="2bd07-121"><dt><strong>INKRECOGNITIONPROPERTY_MAXIMUMSTROKECOUNT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2bd07-121"><dt> <strong>INKRECOGNITIONPROPERTY_MAXIMUMSTROKECOUNT</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="2bd07-122">Die GUID, die die Eigenschaft für die maximale Anzahl der Striche des Erkennungs Ergebnisses für das <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>iinkrecognitionalternate</strong></a> -Objekt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="2bd07-122">The GUID that identifies the property for the maximum stroke count of the recognition result for the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> object.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="2bd07-123">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="2bd07-123">Not implemented.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_POINTSPERINCH_________"></span><span id="___________inkrecognitionproperty_pointsperinch_________"></span><dl> <span data-ttu-id="2bd07-124"><dt><strong>INKRECOGNITIONPROPERTY_POINTSPERINCH</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2bd07-124"><dt> <strong>INKRECOGNITIONPROPERTY_POINTSPERINCH</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="2bd07-125">Die GUID, die die Eigenschaft für die Metrik "Punkte pro Zoll" des <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>iinkrecognitionalternate</strong></a> -Objekts identifiziert.</span><span class="sxs-lookup"><span data-stu-id="2bd07-125">The GUID that identifies the property for the points-per-inch metric of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> object.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="2bd07-126">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="2bd07-126">Not implemented.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_CONFIDENCELEVEL_________"></span><span id="___________inkrecognitionproperty_confidencelevel_________"></span><dl> <span data-ttu-id="2bd07-127"><dt><strong>INKRECOGNITIONPROPERTY_CONFIDENCELEVEL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2bd07-127"><dt> <strong>INKRECOGNITIONPROPERTY_CONFIDENCELEVEL</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="2bd07-128">Die GUID, die die Eigenschaft für die Vertrauens Ebene identifiziert, die die Erkennung im Erkennungs Ergebnis aufweist.</span><span class="sxs-lookup"><span data-stu-id="2bd07-128">The GUID that identifies the property for the level of confidence that the recognizer has in the recognition result.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="2bd07-129">Die vertrauensbewertung ist nur für USA Englisch und alle Gesten Erkennungs Tools in Microsoft Windows XP Tablet PC Edition und Windows Vista verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2bd07-129">Confidence evaluation is available only for United States English and all gesture recognizers in Microsoft Windows XP Tablet PC Edition and Windows Vista.</span></span> <span data-ttu-id="2bd07-130">Methoden, die die Eigenschaft Vertrauen für alle anderen Erkennungs Modul bereitstellen E_NOTIMPL zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="2bd07-130">Methods that provide the confidence property for any other recognizer return E_NOTIMPL.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_LINEMETRICS_________"></span><span id="___________inkrecognitionproperty_linemetrics_________"></span><dl> <span data-ttu-id="2bd07-131"><dt><strong>INKRECOGNITIONPROPERTY_LINEMETRICS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2bd07-131"><dt> <strong>INKRECOGNITIONPROPERTY_LINEMETRICS</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="2bd07-132">Die GUID, die die Eigenschaft für die linienmetriken des <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>iinkrecognitionalternate</strong></a> -Objekts identifiziert, d. h. die Zeile, für die Metriken abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2bd07-132">The GUID that identifies the property for the line metrics of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> object, which is the line for which to retrieve metrics.</span></span> <br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="2bd07-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2bd07-133">Remarks</span></span>

<span data-ttu-id="2bd07-134">In C++ können Sie auf diese Konstanten in der Header Datei "msink AUT. h" zugreifen, die sich im <systemdrive> \\ Verzeichnis "Programme \\ Microsoft SDKs \\ Windows \\ v 6.0 include" befindet, \\ Wenn Sie das SDK am Standard Speicherort installiert haben.</span><span class="sxs-lookup"><span data-stu-id="2bd07-134">In C++, you can access these constants in the Msinkaut.h header file, which is located in the <systemdrive>:\\Program Files\\Microsoft SDKs\\Windows\\v6.0\\Include directory if you installed the SDK in the default location.</span></span>

> [!Note]  
> <span data-ttu-id="2bd07-135">In C++ sind diese Konstanten WCHARs, nicht bstrins.</span><span class="sxs-lookup"><span data-stu-id="2bd07-135">In C++, these constants are WCHARs, not BSTRs.</span></span> <span data-ttu-id="2bd07-136">Konvertieren Sie diese vor der Verwendung in bstraus.</span><span class="sxs-lookup"><span data-stu-id="2bd07-136">Convert them into BSTRs before use.</span></span> <span data-ttu-id="2bd07-137">Weitere Informationen zum BSTR-Datentyp finden Sie unter [Verwenden der com-Bibliothek](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="2bd07-137">For more information about the BSTR data type, see [Using the COM Library](using-the-com-library.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2bd07-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2bd07-138">Requirements</span></span>



| <span data-ttu-id="2bd07-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2bd07-139">Requirement</span></span> | <span data-ttu-id="2bd07-140">Wert</span><span class="sxs-lookup"><span data-stu-id="2bd07-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bd07-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2bd07-141">Minimum supported client</span></span><br/> | <span data-ttu-id="2bd07-142">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2bd07-142">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="2bd07-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2bd07-143">Minimum supported server</span></span><br/> | <span data-ttu-id="2bd07-144">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2bd07-144">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="2bd07-145">Header</span><span class="sxs-lookup"><span data-stu-id="2bd07-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="2bd07-146"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="2bd07-146"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bd07-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2bd07-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bd07-148">**Alternativen Methode (Alternativen withconstantpropertyvalues-Methode)**</span><span class="sxs-lookup"><span data-stu-id="2bd07-148">**AlternatesWithConstantPropertyValues Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-alternateswithconstantpropertyvalues)
</dt> <dt>

[<span data-ttu-id="2bd07-149">**Conficealternativen-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="2bd07-149">**ConfidenceAlternates Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_confidencealternates)
</dt> <dt>

[<span data-ttu-id="2bd07-150">**Linealternativen (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="2bd07-150">**LineAlternates Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_linealternates)
</dt> <dt>

[<span data-ttu-id="2bd07-151">**Iinkrecognitionalternativen-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="2bd07-151">**IInkRecognitionAlternates Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates)
</dt> </dl>

 

 




