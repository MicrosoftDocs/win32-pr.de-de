---
description: Enthält Informationen über die Codecs und Formate, die zum Codieren des Inhalts in einer ASF-Datei (Advanced Systems Format) verwendet wurden. Dieses Attribut entspricht dem Codec List-Objekt im ASF-Header, das in der ASF-Spezifikation definiert ist.
ms.assetid: 6dde30d3-dbdc-469c-ad7e-5e670b7e0a64
title: MF_PD_ASF_CODECLIST-Attribut (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 402c53c082ae57fed444168c559f99718322f8a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366099"
---
# <a name="mf_pd_asf_codeclist-attribute"></a><span data-ttu-id="560e8-104">MF \_ PD, \_ ASF \_ codeclist-Attribut</span><span class="sxs-lookup"><span data-stu-id="560e8-104">MF\_PD\_ASF\_CODECLIST attribute</span></span>

<span data-ttu-id="560e8-105">Enthält Informationen über die Codecs und Formate, die zum Codieren des Inhalts in einer ASF-Datei (Advanced Systems Format) verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="560e8-105">Contains information about the codecs and formats that were used to encode the content in an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="560e8-106">Dieses Attribut entspricht dem Codec List-Objekt im ASF-Header, das in der ASF-Spezifikation definiert ist.</span><span class="sxs-lookup"><span data-stu-id="560e8-106">This attribute corresponds to the Codec List Object in the ASF header, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="560e8-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="560e8-107">Data type</span></span>

<span data-ttu-id="560e8-108">Bytearray</span><span class="sxs-lookup"><span data-stu-id="560e8-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="560e8-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="560e8-109">Remarks</span></span>

<span data-ttu-id="560e8-110">Dieses Attribut gilt für Präsentations Deskriptoren für den ASF-Inhalt.</span><span class="sxs-lookup"><span data-stu-id="560e8-110">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="560e8-111">Die [**imfasf ContentInfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) -Methode erstellt den Präsentations Deskriptor und generiert dieses Attribut aus dem Codec List-Objekt im ASF-Header.</span><span class="sxs-lookup"><span data-stu-id="560e8-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method creates the presentation descriptor and generates this attribute from the Codec List Object in the ASF header.</span></span> <span data-ttu-id="560e8-112">Eine Anwendung, die die [ASF-Medienquelle](asf-media-source.md) verwendet, kann dieses Attribut abrufen, indem [**imfmediasource:: createpresentationdescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) aufgerufen und anschließend das-Attribut aus dem Präsentations Deskriptor abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="560e8-112">An application that uses the [ASF Media Source](asf-media-source.md) can get this attribute by calling [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) and then getting the attribute from the presentation descriptor.</span></span>

<span data-ttu-id="560e8-113">In der folgenden Tabelle wird das Layout des Attribut-BLOBs gezeigt.</span><span class="sxs-lookup"><span data-stu-id="560e8-113">The following table shows the layout of the attribute blob.</span></span>



| <span data-ttu-id="560e8-114">Objektfeld für die Codec-Liste</span><span class="sxs-lookup"><span data-stu-id="560e8-114">Codec List Object field</span></span> | <span data-ttu-id="560e8-115">Datentyp</span><span class="sxs-lookup"><span data-stu-id="560e8-115">Data type</span></span>    | <span data-ttu-id="560e8-116">Size</span><span class="sxs-lookup"><span data-stu-id="560e8-116">Size</span></span>    | <span data-ttu-id="560e8-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="560e8-117">Description</span></span>                           |
|-------------------------|--------------|---------|---------------------------------------|
| <span data-ttu-id="560e8-118">Anzahl der Codec-Einträge</span><span class="sxs-lookup"><span data-stu-id="560e8-118">Codec Entries Count</span></span>     | <span data-ttu-id="560e8-119">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="560e8-119">**DWORD**</span></span>    | <span data-ttu-id="560e8-120">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="560e8-120">4 bytes</span></span> | <span data-ttu-id="560e8-121">Anzahl von Codecs</span><span class="sxs-lookup"><span data-stu-id="560e8-121">Number of codecs</span></span>                      |
| <span data-ttu-id="560e8-122">Codec-Einträge</span><span class="sxs-lookup"><span data-stu-id="560e8-122">Codec Entries</span></span>           | <span data-ttu-id="560e8-123">**Hobby**\[\]</span><span class="sxs-lookup"><span data-stu-id="560e8-123">**BYTE**\[\]</span></span> | <span data-ttu-id="560e8-124">Varies</span><span class="sxs-lookup"><span data-stu-id="560e8-124">Varies</span></span>  | <span data-ttu-id="560e8-125">Array von Codec-Informationsstrukturen</span><span class="sxs-lookup"><span data-stu-id="560e8-125">Array of codec information structures</span></span> |



 

<span data-ttu-id="560e8-126">Das Feld Code Einträge ist ein Array von-Strukturen.</span><span class="sxs-lookup"><span data-stu-id="560e8-126">The Code Entries field is an array of structures.</span></span> <span data-ttu-id="560e8-127">In der folgenden Tabelle wird das Format der einzelnen Einträge angezeigt:</span><span class="sxs-lookup"><span data-stu-id="560e8-127">The following table shows the format of each entry:</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="560e8-128">Objektfeld für die Codec-Liste</span><span class="sxs-lookup"><span data-stu-id="560e8-128">Codec List Object field</span></span></th>
<th><span data-ttu-id="560e8-129">Datentyp</span><span class="sxs-lookup"><span data-stu-id="560e8-129">Data type</span></span></th>
<th><span data-ttu-id="560e8-130">Size</span><span class="sxs-lookup"><span data-stu-id="560e8-130">Size</span></span></th>
<th><span data-ttu-id="560e8-131">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="560e8-131">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="560e8-132">type</span><span class="sxs-lookup"><span data-stu-id="560e8-132">Type</span></span></td>
<td><span data-ttu-id="560e8-133"><strong>DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="560e8-133"><strong>DWORD</strong></span></span></td>
<td><span data-ttu-id="560e8-134">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="560e8-134">4 bytes</span></span></td>
<td><span data-ttu-id="560e8-135">Der Codec-Typ.</span><span class="sxs-lookup"><span data-stu-id="560e8-135">Codec type.</span></span> <span data-ttu-id="560e8-136">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="560e8-136">This can be one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="560e8-137">0x0001: Audiocodec</span><span class="sxs-lookup"><span data-stu-id="560e8-137">0x0001: Audio codec</span></span></li>
<li><span data-ttu-id="560e8-138">0x0002: Videocodec</span><span class="sxs-lookup"><span data-stu-id="560e8-138">0x0002: Video codec</span></span></li>
<li><span data-ttu-id="560e8-139">0xFFFF: unbekannt</span><span class="sxs-lookup"><span data-stu-id="560e8-139">0xFFFF: Unknown</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="560e8-140">Länge des Codec-namens</span><span class="sxs-lookup"><span data-stu-id="560e8-140">Codec Name Length</span></span></td>
<td><span data-ttu-id="560e8-141"><strong>DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="560e8-141"><strong>DWORD</strong></span></span></td>
<td><span data-ttu-id="560e8-142">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="560e8-142">4 bytes</span></span></td>
<td><span data-ttu-id="560e8-143">Größe der Codec-namens Zeichenfolge in Bytes, einschließlich des <strong>null</strong> -Zeichens.</span><span class="sxs-lookup"><span data-stu-id="560e8-143">Size of the Codec Name string, in bytes, including the <strong>NULL</strong> character.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="560e8-144">Codec-Name</span><span class="sxs-lookup"><span data-stu-id="560e8-144">Codec Name</span></span></td>
<td><span data-ttu-id="560e8-145"><strong>WCHAR</strong>[]</span><span class="sxs-lookup"><span data-stu-id="560e8-145"><strong>WCHAR</strong>[]</span></span></td>
<td><span data-ttu-id="560e8-146">Varies</span><span class="sxs-lookup"><span data-stu-id="560e8-146">Varies</span></span></td>
<td><span data-ttu-id="560e8-147">Eine mit NULL beendete Unicode-Zeichenfolge, die den Namen des Codecs enthält, z &quot; . b. Windows Media Video 9 &quot; .</span><span class="sxs-lookup"><span data-stu-id="560e8-147">Null-terminated Unicode string that contains the name of the codec, such as &quot;Windows Media Video 9&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="560e8-148">Länge der Codec-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="560e8-148">Codec Description Length</span></span></td>
<td><span data-ttu-id="560e8-149"><strong>DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="560e8-149"><strong>DWORD</strong></span></span></td>
<td><span data-ttu-id="560e8-150">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="560e8-150">4 bytes</span></span></td>
<td><span data-ttu-id="560e8-151">Größe der Codec-Beschreibungs Zeichenfolge in Bytes, einschließlich des <strong>null</strong> -Zeichens.</span><span class="sxs-lookup"><span data-stu-id="560e8-151">Size of the Codec Description string, in bytes, including the <strong>NULL</strong> character.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="560e8-152">Codec-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="560e8-152">Codec Description</span></span></td>
<td><span data-ttu-id="560e8-153"><strong>WCHAR</strong>[]</span><span class="sxs-lookup"><span data-stu-id="560e8-153"><strong>WCHAR</strong>[]</span></span></td>
<td><span data-ttu-id="560e8-154">Varies</span><span class="sxs-lookup"><span data-stu-id="560e8-154">Varies</span></span></td>
<td><span data-ttu-id="560e8-155">Eine NULL-terminierte Unicode-Zeichenfolge, die eine Beschreibung des Codecs enthält.</span><span class="sxs-lookup"><span data-stu-id="560e8-155">A null-terminated Unicode string that contains a description of the codec.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="560e8-156">Länge der Codec-Informationen</span><span class="sxs-lookup"><span data-stu-id="560e8-156">Codec Information Length</span></span></td>
<td><span data-ttu-id="560e8-157"><strong>DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="560e8-157"><strong>DWORD</strong></span></span></td>
<td><span data-ttu-id="560e8-158">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="560e8-158">4 bytes</span></span></td>
<td><span data-ttu-id="560e8-159">Größe des Codec-Informations Felds in Bytes.</span><span class="sxs-lookup"><span data-stu-id="560e8-159">Size of the Codec Information field, in bytes.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="560e8-160">Codec-Informationen</span><span class="sxs-lookup"><span data-stu-id="560e8-160">Codec Information</span></span></td>
<td><span data-ttu-id="560e8-161"><strong>Byte</strong>[]</span><span class="sxs-lookup"><span data-stu-id="560e8-161"><strong>BYTE</strong>[]</span></span></td>
<td><span data-ttu-id="560e8-162">Varies</span><span class="sxs-lookup"><span data-stu-id="560e8-162">Varies</span></span></td>
<td><span data-ttu-id="560e8-163">Codec-Daten.</span><span class="sxs-lookup"><span data-stu-id="560e8-163">Codec data.</span></span> <span data-ttu-id="560e8-164">Die Bedeutung dieser Daten hängt vom Codec ab.</span><span class="sxs-lookup"><span data-stu-id="560e8-164">The meaning of this data depends on the codec.</span></span> <span data-ttu-id="560e8-165">In der Regel wird mit diesen Daten das Format angegeben.</span><span class="sxs-lookup"><span data-stu-id="560e8-165">Typically, this data indicates the format.</span></span></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="560e8-166">Das Layout des Attribut-BLOBs entspricht nicht exakt dem Layout des Codec-Listen Objekts im ASF-Header.</span><span class="sxs-lookup"><span data-stu-id="560e8-166">The layout of the attribute blob does not exactly match the layout of the Codec List Object in the ASF header.</span></span> <span data-ttu-id="560e8-167">Insbesondere werden Zeichen folgen Längen in Bytes angegeben und enthalten die Größe des **null** -Terminator.</span><span class="sxs-lookup"><span data-stu-id="560e8-167">In particular, string lengths are given in bytes and include the size of the **NULL** terminator.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="560e8-168">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="560e8-168">Requirements</span></span>



| <span data-ttu-id="560e8-169">Anforderung</span><span class="sxs-lookup"><span data-stu-id="560e8-169">Requirement</span></span> | <span data-ttu-id="560e8-170">Wert</span><span class="sxs-lookup"><span data-stu-id="560e8-170">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="560e8-171">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="560e8-171">Minimum supported client</span></span><br/> | <span data-ttu-id="560e8-172">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="560e8-172">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="560e8-173">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="560e8-173">Minimum supported server</span></span><br/> | <span data-ttu-id="560e8-174">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="560e8-174">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="560e8-175">Header</span><span class="sxs-lookup"><span data-stu-id="560e8-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="560e8-176"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="560e8-176"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="560e8-177">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="560e8-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="560e8-178">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="560e8-178">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="560e8-179">**Imfattributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="560e8-179">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="560e8-180">**Imfattributes:: setBlob**</span><span class="sxs-lookup"><span data-stu-id="560e8-180">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="560e8-181">**IMF presentationdescriptor**</span><span class="sxs-lookup"><span data-stu-id="560e8-181">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="560e8-182">Präsentations deskriptorattribute</span><span class="sxs-lookup"><span data-stu-id="560e8-182">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="560e8-183">ASF-Header Objekt</span><span class="sxs-lookup"><span data-stu-id="560e8-183">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="560e8-184">Präsentations Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="560e8-184">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




