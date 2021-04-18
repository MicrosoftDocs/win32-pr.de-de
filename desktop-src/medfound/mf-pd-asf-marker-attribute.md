---
description: Gibt die Marker in einer ASF-Datei (Advanced Systems Format) an. Dieses Attribut entspricht dem Markerobjekt im ASF-Header, das in der ASF-Spezifikation definiert ist.
ms.assetid: 6458eb5f-72a2-4723-b26b-b63516aa2df3
title: MF_PD_ASF_MARKER-Attribut (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2ae9c5a6cfd79924b95a3b15a7146539d630aad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351529"
---
# <a name="mf_pd_asf_marker-attribute"></a><span data-ttu-id="73c64-104">MF-und- \_ \_ ASF- \_ Attribut Attribut</span><span class="sxs-lookup"><span data-stu-id="73c64-104">MF\_PD\_ASF\_MARKER attribute</span></span>

<span data-ttu-id="73c64-105">Gibt die Marker in einer ASF-Datei (Advanced Systems Format) an.</span><span class="sxs-lookup"><span data-stu-id="73c64-105">Specifies the markers in an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="73c64-106">Dieses Attribut entspricht dem Markerobjekt im ASF-Header, das in der ASF-Spezifikation definiert ist.</span><span class="sxs-lookup"><span data-stu-id="73c64-106">This attribute corresponds to the Marker Object in the ASF header, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="73c64-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="73c64-107">Data type</span></span>

<span data-ttu-id="73c64-108">Bytearray</span><span class="sxs-lookup"><span data-stu-id="73c64-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="73c64-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="73c64-109">Remarks</span></span>

<span data-ttu-id="73c64-110">Dieses Attribut gilt für Präsentations Deskriptoren für den ASF-Inhalt.</span><span class="sxs-lookup"><span data-stu-id="73c64-110">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="73c64-111">Die [**imfasf ContentInfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) -Methode erstellt den Präsentations Deskriptor und generiert dieses Attribut aus dem Markerobjekt.</span><span class="sxs-lookup"><span data-stu-id="73c64-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method creates the presentation descriptor and generates this attribute from the Marker Object.</span></span> <span data-ttu-id="73c64-112">In der folgenden Tabelle wird das Format des BLOBs angezeigt:</span><span class="sxs-lookup"><span data-stu-id="73c64-112">The following table shows the format of the blob:</span></span>



| <span data-ttu-id="73c64-113">Markerobjektfeld</span><span class="sxs-lookup"><span data-stu-id="73c64-113">Marker Object field</span></span> | <span data-ttu-id="73c64-114">Datentyp</span><span class="sxs-lookup"><span data-stu-id="73c64-114">Data type</span></span>    | <span data-ttu-id="73c64-115">Size</span><span class="sxs-lookup"><span data-stu-id="73c64-115">Size</span></span>    | <span data-ttu-id="73c64-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="73c64-116">Description</span></span>       |
|---------------------|--------------|---------|-------------------|
| <span data-ttu-id="73c64-117">Markeranzahl</span><span class="sxs-lookup"><span data-stu-id="73c64-117">Markers Count</span></span>       | <span data-ttu-id="73c64-118">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="73c64-118">**DWORD**</span></span>    | <span data-ttu-id="73c64-119">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="73c64-119">4 bytes</span></span> | <span data-ttu-id="73c64-120">Anzahl der Marker</span><span class="sxs-lookup"><span data-stu-id="73c64-120">Number of markers</span></span> |
| <span data-ttu-id="73c64-121">Marker</span><span class="sxs-lookup"><span data-stu-id="73c64-121">Markers</span></span>             | <span data-ttu-id="73c64-122">**Hobby**\[\]</span><span class="sxs-lookup"><span data-stu-id="73c64-122">**BYTE**\[\]</span></span> | <span data-ttu-id="73c64-123">Varies</span><span class="sxs-lookup"><span data-stu-id="73c64-123">Varies</span></span>  | <span data-ttu-id="73c64-124">Array von Markern</span><span class="sxs-lookup"><span data-stu-id="73c64-124">Array of markers</span></span>  |



 

<span data-ttu-id="73c64-125">Der erste **DWORD** -Wert ist die Anzahl der Marker, gefolgt von einem Array von Markern.</span><span class="sxs-lookup"><span data-stu-id="73c64-125">The first **DWORD** is the number of markers, followed by an array of markers.</span></span> <span data-ttu-id="73c64-126">Jeder Marker weist das folgende Format auf:</span><span class="sxs-lookup"><span data-stu-id="73c64-126">Each marker has the following format:</span></span>



| <span data-ttu-id="73c64-127">Markerobjektfeld</span><span class="sxs-lookup"><span data-stu-id="73c64-127">Marker Object field</span></span>       | <span data-ttu-id="73c64-128">Datentyp</span><span class="sxs-lookup"><span data-stu-id="73c64-128">Data type</span></span>     | <span data-ttu-id="73c64-129">Size</span><span class="sxs-lookup"><span data-stu-id="73c64-129">Size</span></span>    | <span data-ttu-id="73c64-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="73c64-130">Description</span></span>                                                                       |
|---------------------------|---------------|---------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="73c64-131">Markerbeschreibungs Länge</span><span class="sxs-lookup"><span data-stu-id="73c64-131">Marker Description Length</span></span> | <span data-ttu-id="73c64-132">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="73c64-132">**DWORD**</span></span>     | <span data-ttu-id="73c64-133">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="73c64-133">4 bytes</span></span> | <span data-ttu-id="73c64-134">Größe der Beschreibungs Zeichenfolge in Bytes, einschließlich des NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="73c64-134">Size of the description string, in bytes, including the NULL character.</span></span>           |
| <span data-ttu-id="73c64-135">Markerbeschreibung</span><span class="sxs-lookup"><span data-stu-id="73c64-135">Marker Description</span></span>        | <span data-ttu-id="73c64-136">**WCHAR**\[\]</span><span class="sxs-lookup"><span data-stu-id="73c64-136">**WCHAR**\[\]</span></span> | <span data-ttu-id="73c64-137">Varies</span><span class="sxs-lookup"><span data-stu-id="73c64-137">Varies</span></span>  | <span data-ttu-id="73c64-138">Eine mit NULL beendete Zeichenfolge, die den Marker beschreibt.</span><span class="sxs-lookup"><span data-stu-id="73c64-138">Null-terminated string that describes the marker.</span></span>                                 |
| <span data-ttu-id="73c64-139">Präsentationszeit</span><span class="sxs-lookup"><span data-stu-id="73c64-139">Presentation Time</span></span>         | <span data-ttu-id="73c64-140">**LONGLONG**</span><span class="sxs-lookup"><span data-stu-id="73c64-140">**LONGLONG**</span></span>  | <span data-ttu-id="73c64-141">8 Bytes</span><span class="sxs-lookup"><span data-stu-id="73c64-141">8 bytes</span></span> | <span data-ttu-id="73c64-142">Präsentationszeit des Markers in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="73c64-142">Presentation time of the marker, in 100-nanosecond units.</span></span>                         |
| <span data-ttu-id="73c64-143">Sendezeit</span><span class="sxs-lookup"><span data-stu-id="73c64-143">Send Time</span></span>                 | <span data-ttu-id="73c64-144">**LONGLONG**</span><span class="sxs-lookup"><span data-stu-id="73c64-144">**LONGLONG**</span></span>  | <span data-ttu-id="73c64-145">8 Bytes</span><span class="sxs-lookup"><span data-stu-id="73c64-145">8 bytes</span></span> | <span data-ttu-id="73c64-146">Sende Zeit des markereintrags in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="73c64-146">Send time of the marker entry, in milliseconds.</span></span>                                   |
| <span data-ttu-id="73c64-147">Offset</span><span class="sxs-lookup"><span data-stu-id="73c64-147">Offset</span></span>                    | <span data-ttu-id="73c64-148">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="73c64-148">**UINT64**</span></span>    | <span data-ttu-id="73c64-149">8 Bytes</span><span class="sxs-lookup"><span data-stu-id="73c64-149">8 bytes</span></span> | <span data-ttu-id="73c64-150">Offset (in Bytes) in das Datenobjekt, das die Position des Markts angibt.</span><span class="sxs-lookup"><span data-stu-id="73c64-150">Offset, in bytes, into the Data Object that specifies the position of the market.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="73c64-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="73c64-151">Requirements</span></span>



| <span data-ttu-id="73c64-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="73c64-152">Requirement</span></span> | <span data-ttu-id="73c64-153">Wert</span><span class="sxs-lookup"><span data-stu-id="73c64-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="73c64-154">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="73c64-154">Minimum supported client</span></span><br/> | <span data-ttu-id="73c64-155">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="73c64-155">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="73c64-156">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="73c64-156">Minimum supported server</span></span><br/> | <span data-ttu-id="73c64-157">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="73c64-157">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="73c64-158">Header</span><span class="sxs-lookup"><span data-stu-id="73c64-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="73c64-159"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="73c64-159"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73c64-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="73c64-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73c64-161">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="73c64-161">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="73c64-162">**Imfattributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="73c64-162">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="73c64-163">**Imfattributes:: setBlob**</span><span class="sxs-lookup"><span data-stu-id="73c64-163">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="73c64-164">**IMF presentationdescriptor**</span><span class="sxs-lookup"><span data-stu-id="73c64-164">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="73c64-165">Präsentations deskriptorattribute</span><span class="sxs-lookup"><span data-stu-id="73c64-165">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="73c64-166">ASF-Header Objekt</span><span class="sxs-lookup"><span data-stu-id="73c64-166">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="73c64-167">Präsentations Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="73c64-167">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




