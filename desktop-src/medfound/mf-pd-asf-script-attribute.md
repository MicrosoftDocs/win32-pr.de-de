---
description: Gibt eine Liste von Skript Befehlen und Parametern für eine ASF-Datei (Advanced Systems Format) an. Dieses Attribut entspricht dem Skript Befehls Objekt im ASF-Header, das in der ASF-Spezifikation definiert ist.
ms.assetid: c85c9da4-f0b5-4055-a645-2a71cabbe4a3
title: MF_PD_ASF_SCRIPT-Attribut (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03de86298d28183aa57cc80b451c4e46bb054de2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351782"
---
# <a name="mf_pd_asf_script-attribute"></a><span data-ttu-id="d35f8-104">MF \_ PD, \_ ASF- \_ Skript Attribut</span><span class="sxs-lookup"><span data-stu-id="d35f8-104">MF\_PD\_ASF\_SCRIPT attribute</span></span>

<span data-ttu-id="d35f8-105">Gibt eine Liste von Skript Befehlen und Parametern für eine ASF-Datei (Advanced Systems Format) an.</span><span class="sxs-lookup"><span data-stu-id="d35f8-105">Specifies a list of script commands and the parameters for an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="d35f8-106">Dieses Attribut entspricht dem Skript Befehls Objekt im ASF-Header, das in der ASF-Spezifikation definiert ist.</span><span class="sxs-lookup"><span data-stu-id="d35f8-106">This attribute corresponds to the Script Command Object in the ASF header, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="d35f8-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="d35f8-107">Data type</span></span>

<span data-ttu-id="d35f8-108">Bytearray</span><span class="sxs-lookup"><span data-stu-id="d35f8-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="d35f8-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d35f8-109">Remarks</span></span>

<span data-ttu-id="d35f8-110">Dieses Attribut gilt für Präsentations Deskriptoren für den ASF-Inhalt.</span><span class="sxs-lookup"><span data-stu-id="d35f8-110">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="d35f8-111">Die [**imfasf ContentInfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) -Methode erstellt den Präsentations Deskriptor und generiert dieses Attribut aus dem Objekt Header des Skript Befehls.</span><span class="sxs-lookup"><span data-stu-id="d35f8-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method creates the presentation descriptor and generates this attribute from the Script Command Object header.</span></span> <span data-ttu-id="d35f8-112">In der folgenden Tabelle wird das Format des BLOBs angezeigt:</span><span class="sxs-lookup"><span data-stu-id="d35f8-112">The following table shows the format of the blob:</span></span>



| <span data-ttu-id="d35f8-113">Objektfeld für Skript Befehl</span><span class="sxs-lookup"><span data-stu-id="d35f8-113">Script Command Object field</span></span> | <span data-ttu-id="d35f8-114">Datentyp</span><span class="sxs-lookup"><span data-stu-id="d35f8-114">Data type</span></span>    | <span data-ttu-id="d35f8-115">Size</span><span class="sxs-lookup"><span data-stu-id="d35f8-115">Size</span></span>    | <span data-ttu-id="d35f8-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d35f8-116">Description</span></span>               |
|-----------------------------|--------------|---------|---------------------------|
| <span data-ttu-id="d35f8-117">Anzahl von Befehlen</span><span class="sxs-lookup"><span data-stu-id="d35f8-117">Commands Count</span></span>              | <span data-ttu-id="d35f8-118">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="d35f8-118">**DWORD**</span></span>    | <span data-ttu-id="d35f8-119">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="d35f8-119">4 bytes</span></span> | <span data-ttu-id="d35f8-120">Anzahl von Skript Befehlen</span><span class="sxs-lookup"><span data-stu-id="d35f8-120">Number of script commands</span></span> |
| <span data-ttu-id="d35f8-121">Befehlstyp, Befehle</span><span class="sxs-lookup"><span data-stu-id="d35f8-121">Command Type, Commands</span></span>      | <span data-ttu-id="d35f8-122">**Hobby**\[\]</span><span class="sxs-lookup"><span data-stu-id="d35f8-122">**BYTE**\[\]</span></span> | <span data-ttu-id="d35f8-123">Varies</span><span class="sxs-lookup"><span data-stu-id="d35f8-123">Varies</span></span>  | <span data-ttu-id="d35f8-124">Array von Skript Befehlen</span><span class="sxs-lookup"><span data-stu-id="d35f8-124">Array of script commands</span></span>  |



 

<span data-ttu-id="d35f8-125">Der erste **DWORD** -Wert ist die Anzahl von Skript Befehlen, gefolgt von einem Array von Befehlen.</span><span class="sxs-lookup"><span data-stu-id="d35f8-125">The first **DWORD** is the number of script commands, followed by an array of commands.</span></span> <span data-ttu-id="d35f8-126">Jeder Skript Befehl weist das folgende Format auf:</span><span class="sxs-lookup"><span data-stu-id="d35f8-126">Each script command has the following format:</span></span>



| <span data-ttu-id="d35f8-127">Objektfeld für Skript Befehl</span><span class="sxs-lookup"><span data-stu-id="d35f8-127">Script Command Object field</span></span> | <span data-ttu-id="d35f8-128">Datentyp</span><span class="sxs-lookup"><span data-stu-id="d35f8-128">Data type</span></span>     | <span data-ttu-id="d35f8-129">Size</span><span class="sxs-lookup"><span data-stu-id="d35f8-129">Size</span></span>    | <span data-ttu-id="d35f8-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d35f8-130">Description</span></span>                                                              |
|-----------------------------|---------------|---------|--------------------------------------------------------------------------|
| <span data-ttu-id="d35f8-131">Länge des Befehlsnamens</span><span class="sxs-lookup"><span data-stu-id="d35f8-131">Command Name Length</span></span>         | <span data-ttu-id="d35f8-132">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="d35f8-132">**DWORD**</span></span>     | <span data-ttu-id="d35f8-133">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="d35f8-133">4 bytes</span></span> | <span data-ttu-id="d35f8-134">Größe der Befehls Zeichenfolge in Bytes, einschließlich des NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="d35f8-134">Size of the command string, in bytes, including the NULL character.</span></span>      |
| <span data-ttu-id="d35f8-135">Befehlsname</span><span class="sxs-lookup"><span data-stu-id="d35f8-135">Command Name</span></span>                | <span data-ttu-id="d35f8-136">**WCHAR**\[\]</span><span class="sxs-lookup"><span data-stu-id="d35f8-136">**WCHAR**\[\]</span></span> | <span data-ttu-id="d35f8-137">Varies</span><span class="sxs-lookup"><span data-stu-id="d35f8-137">Varies</span></span>  | <span data-ttu-id="d35f8-138">Eine auf NULL endenden Zeichenfolge, die den Skript Befehl enthält.</span><span class="sxs-lookup"><span data-stu-id="d35f8-138">Null-terminated string that contains the script command.</span></span>                 |
| <span data-ttu-id="d35f8-139">Länge des Befehls Typnamens</span><span class="sxs-lookup"><span data-stu-id="d35f8-139">Command Type Name Length</span></span>    | <span data-ttu-id="d35f8-140">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="d35f8-140">**DWORD**</span></span>     | <span data-ttu-id="d35f8-141">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="d35f8-141">4 bytes</span></span> | <span data-ttu-id="d35f8-142">Größe der Befehlstyp Zeichenfolge in Bytes, einschließlich des NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="d35f8-142">Size of the command type string, in bytes, including the NULL character.</span></span> |
| <span data-ttu-id="d35f8-143">Befehlstyp Name</span><span class="sxs-lookup"><span data-stu-id="d35f8-143">Command Type Name</span></span>           | <span data-ttu-id="d35f8-144">**WCHAR**\[\]</span><span class="sxs-lookup"><span data-stu-id="d35f8-144">**WCHAR**\[\]</span></span> | <span data-ttu-id="d35f8-145">Varies</span><span class="sxs-lookup"><span data-stu-id="d35f8-145">Varies</span></span>  | <span data-ttu-id="d35f8-146">Eine auf NULL endenden Zeichenfolge, die den Befehlstyp enthält.</span><span class="sxs-lookup"><span data-stu-id="d35f8-146">Null-terminated string that contains the command type.</span></span>                   |
| <span data-ttu-id="d35f8-147">Präsentationszeit</span><span class="sxs-lookup"><span data-stu-id="d35f8-147">Presentation Time</span></span>           | <span data-ttu-id="d35f8-148">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="d35f8-148">**DWORD**</span></span>     | <span data-ttu-id="d35f8-149">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="d35f8-149">4 bytes</span></span> | <span data-ttu-id="d35f8-150">Präsentationszeit des Befehls in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="d35f8-150">Presentation time of the command in milliseconds.</span></span>                        |



 

## <a name="requirements"></a><span data-ttu-id="d35f8-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d35f8-151">Requirements</span></span>



| <span data-ttu-id="d35f8-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d35f8-152">Requirement</span></span> | <span data-ttu-id="d35f8-153">Wert</span><span class="sxs-lookup"><span data-stu-id="d35f8-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d35f8-154">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d35f8-154">Minimum supported client</span></span><br/> | <span data-ttu-id="d35f8-155">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d35f8-155">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d35f8-156">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d35f8-156">Minimum supported server</span></span><br/> | <span data-ttu-id="d35f8-157">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d35f8-157">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d35f8-158">Header</span><span class="sxs-lookup"><span data-stu-id="d35f8-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="d35f8-159"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="d35f8-159"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d35f8-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d35f8-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d35f8-161">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="d35f8-161">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d35f8-162">**Imfattributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="d35f8-162">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="d35f8-163">**Imfattributes:: setBlob**</span><span class="sxs-lookup"><span data-stu-id="d35f8-163">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="d35f8-164">**IMF presentationdescriptor**</span><span class="sxs-lookup"><span data-stu-id="d35f8-164">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="d35f8-165">Präsentations deskriptorattribute</span><span class="sxs-lookup"><span data-stu-id="d35f8-165">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="d35f8-166">ASF-Header Objekt</span><span class="sxs-lookup"><span data-stu-id="d35f8-166">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="d35f8-167">Präsentations Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="d35f8-167">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




