---
description: Gibt an, ob der topologielader die Medientypen auflistet, die von der Medienquelle bereitgestellt werden.
ms.assetid: 2675ef16-2018-47e8-bb22-2fc0d62e6681
title: MF_TOPOLOGY_ENUMERATE_SOURCE_TYPES-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 015042bbf9994f81058c621239224196e6ec9ac8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343309"
---
# <a name="mf_topology_enumerate_source_types-attribute"></a><span data-ttu-id="72579-103">MF- \_ \_ topologieaufzählenden \_ Quell \_ Typen Attribut</span><span class="sxs-lookup"><span data-stu-id="72579-103">MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES attribute</span></span>

<span data-ttu-id="72579-104">Gibt an, ob der topologielader die Medientypen auflistet, die von der Medienquelle bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="72579-104">Specifies whether the topology loader enumerates the media types provided by the media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="72579-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="72579-105">Data type</span></span>

<span data-ttu-id="72579-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="72579-106">**UINT32**</span></span>

<span data-ttu-id="72579-107">Verwenden Sie einen der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="72579-107">Use one of the following values.</span></span>



| <span data-ttu-id="72579-108">Wert</span><span class="sxs-lookup"><span data-stu-id="72579-108">Value</span></span>                                                                                                                                    | <span data-ttu-id="72579-109">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="72579-109">Meaning</span></span>                                             |
|------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="FALSE"></span><span id="false"></span><dl> <span data-ttu-id="72579-110"><dt>FALSE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="72579-110"><dt>\*\*\*\*FALSE\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="72579-111">Zählen Sie nicht die Quell Medientypen auf.</span><span class="sxs-lookup"><span data-stu-id="72579-111">Do not enumerate the source media types.</span></span><br/> |
| <span id="TRUE"></span><span id="true"></span><dl> <span data-ttu-id="72579-112"><dt>TRUE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="72579-112"><dt>\*\*\*\*TRUE\*\*\*\*</dt></span></span> </dl>    | <span data-ttu-id="72579-113">Listet die Quell Medientypen auf.</span><span class="sxs-lookup"><span data-stu-id="72579-113">Enumerate the source media types.</span></span><br/>        |



 

## <a name="getset"></a><span data-ttu-id="72579-114">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="72579-114">Get/set</span></span>

<span data-ttu-id="72579-115">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="72579-115">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="72579-116">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="72579-116">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="72579-117">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="72579-117">Applies to</span></span>

[<span data-ttu-id="72579-118">**Imftopology**</span><span class="sxs-lookup"><span data-stu-id="72579-118">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="72579-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="72579-119">Remarks</span></span>

<span data-ttu-id="72579-120">Jeder Datenstrom in einer Medienquelle kann mehr als einen Medientyp anbieten.</span><span class="sxs-lookup"><span data-stu-id="72579-120">Each stream on a media source can offer more than one media type.</span></span> <span data-ttu-id="72579-121">Die Liste der Typen wird durch die [**imvmediatyethandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) -Schnittstelle auf dem Datenstrom Deskriptor aufgezählt.</span><span class="sxs-lookup"><span data-stu-id="72579-121">The list of types is enumerated through the [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) interface on the stream descriptor.</span></span>

<span data-ttu-id="72579-122">Die Reihenfolge, in der der topologielader versucht, die Medientypen einer Medienquelle zu steuern, wird durch zwei Attribute gesteuert:</span><span class="sxs-lookup"><span data-stu-id="72579-122">The order in which the topology loader tries a media source's media types is controlled by two attributes:</span></span>

-   <span data-ttu-id="72579-123">Die MF- \_ Topologie \_ listet das \_ Quell \_ Typen Attribut in der Topologie auf.</span><span class="sxs-lookup"><span data-stu-id="72579-123">The MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES attribute on the topology.</span></span>
-   <span data-ttu-id="72579-124">Das [**MF \_ toponode \_ Connect \_ method**](mf-toponode-connect-method-attribute.md) -Attribut auf dem Quellknoten.</span><span class="sxs-lookup"><span data-stu-id="72579-124">The [**MF\_TOPONODE\_CONNECT\_METHOD**](mf-toponode-connect-method-attribute.md) attribute on the source node.</span></span>

<span data-ttu-id="72579-125">Wenn das \_ Attribut für die MF-topologieenumeration \_ \_ Quell Typen auf \_ **false** festgelegt oder nicht festgelegt ist, verwendet das topologielader den aktuellen Medientyp des Streams.</span><span class="sxs-lookup"><span data-stu-id="72579-125">If the MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES attribute is **FALSE** or not set, the topology loader uses the stream's current media type.</span></span> <span data-ttu-id="72579-126">Die Liste der möglichen Typen wird nicht aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="72579-126">It does not enumerate the list of possible types.</span></span> <span data-ttu-id="72579-127">Wenn der aktuelle Medientyp nicht mit dem Knoten der Downstream-Topologie kompatibel ist und keine Kombination aus Decodern/Konvertern gefunden werden kann, tritt bei der topologieauflösung ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="72579-127">If the current media type is incompatible with the downstream topology node, and no combination of decoders/converters can be found, topology resolution fails.</span></span>

<span data-ttu-id="72579-128">Wenn das Attribut für die MF- \_ topologieaufzählenden \_ Quell Typen den Wert \_ \_ **true** hat, listet das topologielader die Medientypen der Quelle auf, bis ein kompatibler Typ gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="72579-128">If the MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES attribute is **TRUE**, the topology loader enumerates the source's media types until it finds a compatible type.</span></span> <span data-ttu-id="72579-129">In diesem Fall hängt die genaue Reihenfolge der Vorgänge davon ab, ob das [**MF \_ toponode \_ Connect \_ method**](mf-toponode-connect-method-attribute.md) -Attribut auf dem Quellknoten das **MF \_ Connect \_ Resolve \_ Independent \_ OutputTypes** -Flag enthält.</span><span class="sxs-lookup"><span data-stu-id="72579-129">In that case, the exact order of operations depends on the whether the [**MF\_TOPONODE\_CONNECT\_METHOD**](mf-toponode-connect-method-attribute.md) attribute on the source node includes the **MF\_CONNECT\_RESOLVE\_INDEPENDENT\_OUTPUTTYPES** flag.</span></span>

<span data-ttu-id="72579-130">Wenn die MF \_ -Topologie \_ aufzählenden \_ Quell \_ Typen auf **true** festgelegt ist und das **MF \_ Connect \_ Resolve \_ Independent \_ OutputTypes** -Flag festgelegt ist, werden die einzelnen Medientypen vom topologielader vor der Umstellung auf den nächsten in der folgenden Form erschöpft:</span><span class="sxs-lookup"><span data-stu-id="72579-130">If MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES is **TRUE** and the **MF\_CONNECT\_RESOLVE\_INDEPENDENT\_OUTPUTTYPES** flag is set, the topology loader exhausts each media type before moving to the next, as follows:</span></span>

``` syntax
foreach media type T
    connect directly using T
    if failed, connect with converters using T
    if failed, connect with decoders using T
```

<span data-ttu-id="72579-131">Wenn die MF- \_ Topologie " \_ true" aufzählt, \_ \_ aber **MF \_ Connect \_ \_ unabhängige \_ OutputTypes** nicht festgelegt ist, versucht das topologielader eine direkte Verbindung mit jedem Medientyp, versucht dann jeden Medientyp mit Konvertern zu versuchen und schließlich jeden Medientyp mit Decodern  zu versuchen:</span><span class="sxs-lookup"><span data-stu-id="72579-131">If MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES is **TRUE** but **MF\_CONNECT\_RESOLVE\_INDEPENDENT\_OUTPUTTYPES** is not set, the topology loader tries a direct connection with each media type, then tries each media type with converters, and finally tries each media type with decoders:</span></span>

``` syntax
foreach media type T
    connect directly using T
if failed,
    foreach media type T
        connect with converters using T
if failed
    foreach media type T
        connect with decoders using T
```

<span data-ttu-id="72579-132">Wenn die MF- \_ Topologie \_ aufzählenden \_ Quell \_ Typen den Wert **false** hat, wird das kennflag für die **MF \_ Connect \_ Resolve \_ Independent \_ OutputTypes** ignoriert.</span><span class="sxs-lookup"><span data-stu-id="72579-132">If MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES is **FALSE**, the **MF\_CONNECT\_RESOLVE\_INDEPENDENT\_OUTPUTTYPES** flag is ignored.</span></span>

<span data-ttu-id="72579-133">Der Standardwert der MF- \_ Topologie \_ Enumerate \_ Source \_ types ist **false**, um die Kompatibilität mit vorhandenen Anwendungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="72579-133">The default value of MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES is **FALSE**, for compatibility with existing applications.</span></span>

<span data-ttu-id="72579-134">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="72579-134">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

### <a name="example"></a><span data-ttu-id="72579-135">Beispiel</span><span class="sxs-lookup"><span data-stu-id="72579-135">Example</span></span>

<span data-ttu-id="72579-136">Im folgenden Beispiel wird das Flag " **MF \_ Connect \_ Resolve \_ Independent \_ OutputTypes** " veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="72579-136">Here is an example that illustrates the **MF\_CONNECT\_RESOLVE\_INDEPENDENT\_OUTPUTTYPES** flag.</span></span> <span data-ttu-id="72579-137">Angenommen, in der Topologie ist das Attribut für die MF- \_ Topologie \_ Enumerate \_ Source \_ types auf **true** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="72579-137">Assume the topology has the MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES attribute set to **TRUE**.</span></span>

<span data-ttu-id="72579-138">Die Medienquelle bietet die folgenden Typen:</span><span class="sxs-lookup"><span data-stu-id="72579-138">The media source offers the following types:</span></span>

-   <span data-ttu-id="72579-139">T1, T2, T3</span><span class="sxs-lookup"><span data-stu-id="72579-139">T1, T2, T3</span></span>

<span data-ttu-id="72579-140">Die Medien Senke akzeptiert die folgenden Typen:</span><span class="sxs-lookup"><span data-stu-id="72579-140">The media sink accepts the following types:</span></span>

-   <span data-ttu-id="72579-141">T3, T4</span><span class="sxs-lookup"><span data-stu-id="72579-141">T3, T4</span></span>

<span data-ttu-id="72579-142">Fall 1: das Flag " **MF \_ Connect \_ Resolve \_ Independent \_ OutputTypes** " wurde festgelegt.</span><span class="sxs-lookup"><span data-stu-id="72579-142">Case 1: The **MF\_CONNECT\_RESOLVE\_INDEPENDENT\_OUTPUTTYPES** flag is set.</span></span>

1.  <span data-ttu-id="72579-143">Das topologielader versucht, eine direkte Verbindung mit T1 herzustellen.</span><span class="sxs-lookup"><span data-stu-id="72579-143">The topology loader tries a direct connection with T1.</span></span> <span data-ttu-id="72579-144">Die Senke lehnt T1 ab.</span><span class="sxs-lookup"><span data-stu-id="72579-144">The sink rejects T1.</span></span>
2.  <span data-ttu-id="72579-145">Das topologielader fügt einen Decoder ein, der T1 annimmt und T4 ausgibt.</span><span class="sxs-lookup"><span data-stu-id="72579-145">The topology loader inserts a decoder that accepts T1 and outputs T4.</span></span> <span data-ttu-id="72579-146">Die Senke akzeptiert T4.</span><span class="sxs-lookup"><span data-stu-id="72579-146">The sink accepts T4.</span></span>
3.  <span data-ttu-id="72579-147">Die letzte Topologie enthält: Medienquelle → Decoder → Medien Senke.</span><span class="sxs-lookup"><span data-stu-id="72579-147">The final topology contains: media source → decoder → media sink.</span></span>

<span data-ttu-id="72579-148">Fall 2: das Flag ist nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="72579-148">Case 2: The flag is not set.</span></span>

1.  <span data-ttu-id="72579-149">Das topologielader versucht, eine direkte Verbindung mit T1 herzustellen.</span><span class="sxs-lookup"><span data-stu-id="72579-149">The topology loader tries a direct connection with T1.</span></span> <span data-ttu-id="72579-150">Die Senke lehnt T1 ab.</span><span class="sxs-lookup"><span data-stu-id="72579-150">The sink rejects T1.</span></span>
2.  <span data-ttu-id="72579-151">Das topologielader versucht, eine direkte Verbindung mit T2 herzustellen.</span><span class="sxs-lookup"><span data-stu-id="72579-151">The topology loader tries a direct connection with T2.</span></span> <span data-ttu-id="72579-152">Die Senke lehnt T2 ab.</span><span class="sxs-lookup"><span data-stu-id="72579-152">The sink rejects T2.</span></span>
3.  <span data-ttu-id="72579-153">Das topologielader versucht, eine direkte Verbindung mit T3 herzustellen.</span><span class="sxs-lookup"><span data-stu-id="72579-153">The topology loader tries a direct connection with T3.</span></span> <span data-ttu-id="72579-154">Die Senke akzeptiert T3.</span><span class="sxs-lookup"><span data-stu-id="72579-154">The sink accepts T3.</span></span>
4.  <span data-ttu-id="72579-155">Die letzte Topologie enthält: Medienquelle → Medien Senke.</span><span class="sxs-lookup"><span data-stu-id="72579-155">The final topology contains: media source → media sink.</span></span>

## <a name="requirements"></a><span data-ttu-id="72579-156">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="72579-156">Requirements</span></span>



| <span data-ttu-id="72579-157">Anforderung</span><span class="sxs-lookup"><span data-stu-id="72579-157">Requirement</span></span> | <span data-ttu-id="72579-158">Wert</span><span class="sxs-lookup"><span data-stu-id="72579-158">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="72579-159">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="72579-159">Minimum supported client</span></span><br/> | <span data-ttu-id="72579-160">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="72579-160">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="72579-161">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="72579-161">Minimum supported server</span></span><br/> | <span data-ttu-id="72579-162">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="72579-162">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="72579-163">Header</span><span class="sxs-lookup"><span data-stu-id="72579-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="72579-164"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="72579-164"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72579-165">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="72579-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72579-166">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="72579-166">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="72579-167">Topologieattribute</span><span class="sxs-lookup"><span data-stu-id="72579-167">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




