---
description: Enthält eine Liste der in der aktuellen Präsentation verwendeten RFC 1766-Sprachen.
ms.assetid: 8853bd88-d51a-478c-8c78-cf69a260e295
title: MF_PD_ASF_LANGLIST_LEGACYORDER-Attribut (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f24abc714a7605800faa8ad66f8c0b888fba6f79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353607"
---
# <a name="mf_pd_asf_langlist_legacyorder-attribute"></a><span data-ttu-id="07cbf-103">MF \_ PD \_ ASF \_ langlist \_ legacyorder-Attribut</span><span class="sxs-lookup"><span data-stu-id="07cbf-103">MF\_PD\_ASF\_LANGLIST\_LEGACYORDER attribute</span></span>

<span data-ttu-id="07cbf-104">Enthält eine Liste der in der aktuellen Präsentation verwendeten RFC 1766-Sprachen.</span><span class="sxs-lookup"><span data-stu-id="07cbf-104">Contains a list of RFC 1766 languages used in the current presentation.</span></span>

## <a name="data-type"></a><span data-ttu-id="07cbf-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="07cbf-105">Data type</span></span>

<span data-ttu-id="07cbf-106">**Hobby \[\]**</span><span class="sxs-lookup"><span data-stu-id="07cbf-106">**BYTE \[\]**</span></span>

## <a name="getset"></a><span data-ttu-id="07cbf-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="07cbf-107">Get/set</span></span>

<span data-ttu-id="07cbf-108">Zum Abrufen dieses Attributs müssen Sie [**imfattributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="07cbf-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="07cbf-109">Um dieses Attribut festzulegen, müssen Sie [**imfattributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="07cbf-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="applies-to"></a><span data-ttu-id="07cbf-110">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="07cbf-110">Applies to</span></span>

[<span data-ttu-id="07cbf-111">**IMF presentationdescriptor**</span><span class="sxs-lookup"><span data-stu-id="07cbf-111">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a><span data-ttu-id="07cbf-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="07cbf-112">Remarks</span></span>

<span data-ttu-id="07cbf-113">Dieses Attribut gilt für Präsentations Deskriptoren, die durch einen Aufruf von [**imfasfcontentinfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)aus dem [Objekt "ASF ContentInfo](asf-contentinfo-object.md) " generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="07cbf-113">This attribute applies to presentation descriptors that were generated from the [ASF ContentInfo Object](asf-contentinfo-object.md) by a call to [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor).</span></span> <span data-ttu-id="07cbf-114">Das Bytearray weist das folgende Format auf:</span><span class="sxs-lookup"><span data-stu-id="07cbf-114">The format of the byte array is as follows:</span></span>



| <span data-ttu-id="07cbf-115">Feld "sprach Listen Objekt"</span><span class="sxs-lookup"><span data-stu-id="07cbf-115">Language List Object field</span></span> | <span data-ttu-id="07cbf-116">Datentyp</span><span class="sxs-lookup"><span data-stu-id="07cbf-116">Data type</span></span>    | <span data-ttu-id="07cbf-117">Size</span><span class="sxs-lookup"><span data-stu-id="07cbf-117">Size</span></span>    | <span data-ttu-id="07cbf-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07cbf-118">Description</span></span>                            |
|----------------------------|--------------|---------|----------------------------------------|
| <span data-ttu-id="07cbf-119">Anzahl der Sprach-ID-Einträge</span><span class="sxs-lookup"><span data-stu-id="07cbf-119">Language ID Records Count</span></span>  | <span data-ttu-id="07cbf-120">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="07cbf-120">**DWORD**</span></span>    | <span data-ttu-id="07cbf-121">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="07cbf-121">4 bytes</span></span> | <span data-ttu-id="07cbf-122">Anzahl von Sprachen</span><span class="sxs-lookup"><span data-stu-id="07cbf-122">Number of languages</span></span>                    |
| <span data-ttu-id="07cbf-123">Sprach-ID-Einträge</span><span class="sxs-lookup"><span data-stu-id="07cbf-123">Language ID Records</span></span>        | <span data-ttu-id="07cbf-124">**Hobby**\[\]</span><span class="sxs-lookup"><span data-stu-id="07cbf-124">**BYTE**\[\]</span></span> | <span data-ttu-id="07cbf-125">Varies</span><span class="sxs-lookup"><span data-stu-id="07cbf-125">Varies</span></span>  | <span data-ttu-id="07cbf-126">Array von sprach Zeichenfolgen (siehe unten).</span><span class="sxs-lookup"><span data-stu-id="07cbf-126">Array of language strings (see below).</span></span> |



 

<span data-ttu-id="07cbf-127">Der erste **DWORD** -Wert ist die Anzahl der Sprachen, gefolgt von einem Array von sprachbezeichnerzeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="07cbf-127">The first **DWORD** is the number of languages, followed by an array of language identifier strings.</span></span> <span data-ttu-id="07cbf-128">Jede Zeichenfolge weist das folgende Format auf:</span><span class="sxs-lookup"><span data-stu-id="07cbf-128">Each string has the following format:</span></span>



| <span data-ttu-id="07cbf-129">Feld "sprach Listen Objekt"</span><span class="sxs-lookup"><span data-stu-id="07cbf-129">Language List Object field</span></span> | <span data-ttu-id="07cbf-130">Datentyp</span><span class="sxs-lookup"><span data-stu-id="07cbf-130">Data type</span></span>     | <span data-ttu-id="07cbf-131">Size</span><span class="sxs-lookup"><span data-stu-id="07cbf-131">Size</span></span>    | <span data-ttu-id="07cbf-132">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07cbf-132">Description</span></span>                                                                               |
|----------------------------|---------------|---------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="07cbf-133">Länge der Sprach-ID</span><span class="sxs-lookup"><span data-stu-id="07cbf-133">Language ID Length</span></span>         | <span data-ttu-id="07cbf-134">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="07cbf-134">**DWORD**</span></span>     | <span data-ttu-id="07cbf-135">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="07cbf-135">4 bytes</span></span> | <span data-ttu-id="07cbf-136">Die Länge der Zeichenfolge in Bytes, einschließlich der Größe des nachfolgenden **null** Zeichens.</span><span class="sxs-lookup"><span data-stu-id="07cbf-136">The length of the string in bytes, including the size of the trailing **NULL** character.</span></span> |
| <span data-ttu-id="07cbf-137">Sprach-ID</span><span class="sxs-lookup"><span data-stu-id="07cbf-137">Language ID</span></span>                | <span data-ttu-id="07cbf-138">**WCHAR**\[\]</span><span class="sxs-lookup"><span data-stu-id="07cbf-138">**WCHAR**\[\]</span></span> | <span data-ttu-id="07cbf-139">Varies</span><span class="sxs-lookup"><span data-stu-id="07cbf-139">Varies</span></span>  | <span data-ttu-id="07cbf-140">Eine mit NULL endenden Zeichenfolge, die den Namen der RFC 1766-Sprache enthält.</span><span class="sxs-lookup"><span data-stu-id="07cbf-140">A null-terminated string containing the RFC 1766 language name.</span></span>                           |



 

<span data-ttu-id="07cbf-141">Jede Zeichenfolge ist ein sprach Kennzeichen, das mit RFC 1766 kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="07cbf-141">Each string is a language tag compliant with RFC 1766.</span></span>

<span data-ttu-id="07cbf-142">Verwenden Sie dieses Attribut nur aus Gründen der Abwärtskompatibilität mit der Enumerationsreihenfolge der [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4) -Schnittstelle im SDK des Windows Media-Formats.</span><span class="sxs-lookup"><span data-stu-id="07cbf-142">Use this attribute only for backward compatibility with the enumeration order of the [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4) interface in the Windows Media Format SDK.</span></span> <span data-ttu-id="07cbf-143">Die sprach Zeichenfolgen werden in einer anderen Reihenfolge als das MF-Attribut " [**\_ \_ ASF \_ langlist**](mf-pd-asf-langlist-attribute.md) " gespeichert.</span><span class="sxs-lookup"><span data-stu-id="07cbf-143">The language strings are stored in a different order in the [**MF\_PD\_ASF\_LANGLIST**](mf-pd-asf-langlist-attribute.md) attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="07cbf-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="07cbf-144">Requirements</span></span>



| <span data-ttu-id="07cbf-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="07cbf-145">Requirement</span></span> | <span data-ttu-id="07cbf-146">Wert</span><span class="sxs-lookup"><span data-stu-id="07cbf-146">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="07cbf-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="07cbf-147">Minimum supported client</span></span><br/> | <span data-ttu-id="07cbf-148">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="07cbf-148">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="07cbf-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="07cbf-149">Minimum supported server</span></span><br/> | <span data-ttu-id="07cbf-150">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="07cbf-150">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="07cbf-151">Header</span><span class="sxs-lookup"><span data-stu-id="07cbf-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="07cbf-152"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="07cbf-152"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07cbf-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07cbf-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07cbf-154">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="07cbf-154">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="07cbf-155">Präsentations deskriptorattribute</span><span class="sxs-lookup"><span data-stu-id="07cbf-155">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 
