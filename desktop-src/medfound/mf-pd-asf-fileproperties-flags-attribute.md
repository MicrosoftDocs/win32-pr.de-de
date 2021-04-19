---
description: Gibt an, ob eine ASF-Datei (Advanced Systems Format) übertragen oder durchsuchbar ist. Dieser Wert entspricht dem Feld Flags des Dateieigenschaften Objekts, das in der ASF-Spezifikation definiert ist.
ms.assetid: 427f0dca-f945-4c89-a87a-a7c86291b1c5
title: MF_PD_ASF_FILEPROPERTIES_FLAGS-Attribut (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee294642188a0f2e22143feeca6791fea591cbb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348740"
---
# <a name="mf_pd_asf_fileproperties_flags-attribute"></a><span data-ttu-id="f3713-104">MF-Attribut für das "MF- \_ \_ \_ \_ Attribut"</span><span class="sxs-lookup"><span data-stu-id="f3713-104">MF\_PD\_ASF\_FILEPROPERTIES\_FLAGS attribute</span></span>

<span data-ttu-id="f3713-105">Gibt an, ob eine ASF-Datei (Advanced Systems Format) übertragen oder durchsuchbar ist.</span><span class="sxs-lookup"><span data-stu-id="f3713-105">Specifies whether an Advanced Systems Format (ASF) file is broadcast or seekable.</span></span> <span data-ttu-id="f3713-106">Dieser Wert entspricht dem Feld Flags des Dateieigenschaften Objekts, das in der ASF-Spezifikation definiert ist.</span><span class="sxs-lookup"><span data-stu-id="f3713-106">This value corresponds to the Flags field of the File Properties Object, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="f3713-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="f3713-107">Data type</span></span>

<span data-ttu-id="f3713-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f3713-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="f3713-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f3713-109">Remarks</span></span>

<span data-ttu-id="f3713-110">Dieses Attribut gilt für Präsentations Deskriptoren für den ASF-Inhalt.</span><span class="sxs-lookup"><span data-stu-id="f3713-110">This attribute applies to presentation descriptors for ASF content.</span></span> <span data-ttu-id="f3713-111">Der Wert des-Attributs ist ein bitweises OR der folgenden Flags:</span><span class="sxs-lookup"><span data-stu-id="f3713-111">The value of the attribute is a bitwise OR of the following flags:</span></span>



| <span data-ttu-id="f3713-112">Flag</span><span class="sxs-lookup"><span data-stu-id="f3713-112">Flag</span></span> | <span data-ttu-id="f3713-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3713-113">Description</span></span>                                                                                                                                                                                                                                                                                       |
|------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3713-114">0x01</span><span class="sxs-lookup"><span data-stu-id="f3713-114">0x01</span></span> | <span data-ttu-id="f3713-115">Broadcast-Flag.</span><span class="sxs-lookup"><span data-stu-id="f3713-115">Broadcast flag.</span></span> <span data-ttu-id="f3713-116">Die Datei wird gerade erstellt.</span><span class="sxs-lookup"><span data-stu-id="f3713-116">The file is in the process of being created.</span></span>                                                                                                                                                                                                                                      |
| <span data-ttu-id="f3713-117">0x02</span><span class="sxs-lookup"><span data-stu-id="f3713-117">0x02</span></span> | <span data-ttu-id="f3713-118">Suchbares Flag.</span><span class="sxs-lookup"><span data-stu-id="f3713-118">Seekable flag.</span></span> <span data-ttu-id="f3713-119">Die Datei ist suchbar.</span><span class="sxs-lookup"><span data-stu-id="f3713-119">The file is seekable.</span></span><br/> <span data-ttu-id="f3713-120">Eine Datei kann durchsuchbar sein, wenn ein Audiodatenstrom vorhanden ist und die maximale Datenpaket Größe der minimalen Datenpaket Größe entspricht.</span><span class="sxs-lookup"><span data-stu-id="f3713-120">A file is seekable if an audio stream is present and the maximum data packet size equals the minimum data packet size.</span></span> <span data-ttu-id="f3713-121">Sie kann auch durchsuchbar sein, wenn die Datei einen Audiostream und einen Videostream mit einem entsprechenden einfachen Index Objekt aufweist.</span><span class="sxs-lookup"><span data-stu-id="f3713-121">It can also be seekable if the file has an audio stream and a video stream with a matching Simple Index Object.</span></span><br/> |



 

<span data-ttu-id="f3713-122">Die [**imfasf ContentInfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) -Methode generiert dieses Attribut aus den ASF-Metadaten.</span><span class="sxs-lookup"><span data-stu-id="f3713-122">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

<span data-ttu-id="f3713-123">Wenn das Broadcast-Flag festgelegt ist, sind die folgenden Attribute im Präsentations Deskriptor ungültig:</span><span class="sxs-lookup"><span data-stu-id="f3713-123">If the broadcast flag is set, the following attributes in the presentation descriptor are not valid:</span></span>

-   [<span data-ttu-id="f3713-124">**Datei-ID für MF \_ PD \_ ASF \_ File Properties \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f3713-124">**MF\_PD\_ASF\_FILEPROPERTIES\_FILE\_ID**</span></span>](mf-pd-asf-fileproperties-file-id-attribute.md)
-   [<span data-ttu-id="f3713-125">**Zeitpunkt der Erstellung der MF \_ PD- \_ \_ Dateieigenschaften \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f3713-125">**MF\_PD\_ASF\_FILEPROPERTIES\_CREATION\_TIME**</span></span>](mf-pd-asf-fileproperties-creation-time-attribute.md)
-   [<span data-ttu-id="f3713-126">**MF-,-Paket- \_ \_ \_ Dateieigenschaften \_ Pakete**</span><span class="sxs-lookup"><span data-stu-id="f3713-126">**MF\_PD\_ASF\_FILEPROPERTIES\_PACKETS**</span></span>](mf-pd-asf-fileproperties-packets-attribute.md)
-   [<span data-ttu-id="f3713-127">**\_Dauer der \_ \_ \_ Wiedergabe \_ Dauer von MF PD ASF File Properties**</span><span class="sxs-lookup"><span data-stu-id="f3713-127">**MF\_PD\_ASF\_FILEPROPERTIES\_PLAY\_DURATION**</span></span>](mf-pd-asf-fileproperties-play-duration-attribute.md)
-   [<span data-ttu-id="f3713-128">**\_Dauer der \_ \_ \_ Sende \_ Dauer von MF PD ASF File Properties**</span><span class="sxs-lookup"><span data-stu-id="f3713-128">**MF\_PD\_ASF\_FILEPROPERTIES\_SEND\_DURATION**</span></span>](mf-pd-asf-fileproperties-send-duration-attribute.md)

<span data-ttu-id="f3713-129">Außerdem werden die Attributwerte für die [**\_ \_ \_ \_ Maximale \_ \_**](mf-pd-asf-fileproperties-max-packet-size-attribute.md) Paketgröße für das MF-Attribut und das Attribut "MF [**\_ PD \_ ASF \_ File Properties \_ Min \_ Packet \_ size**](mf-pd-asf-fileproperties-min-packet-size-attribute.md) " auf die tatsächliche Paketgröße festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f3713-129">In addition, the [**MF\_PD\_ASF\_FILEPROPERTIES\_MAX\_PACKET\_SIZE**](mf-pd-asf-fileproperties-max-packet-size-attribute.md) attribute and [**MF\_PD\_ASF\_FILEPROPERTIES\_MIN\_PACKET\_SIZE**](mf-pd-asf-fileproperties-min-packet-size-attribute.md) attribute values are set to the actual packet size.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3713-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f3713-130">Requirements</span></span>



| <span data-ttu-id="f3713-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f3713-131">Requirement</span></span> | <span data-ttu-id="f3713-132">Wert</span><span class="sxs-lookup"><span data-stu-id="f3713-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3713-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f3713-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f3713-134">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f3713-134">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f3713-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f3713-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f3713-136">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f3713-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f3713-137">Header</span><span class="sxs-lookup"><span data-stu-id="f3713-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3713-138"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3713-138"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3713-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f3713-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3713-140">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="f3713-140">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f3713-141">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="f3713-141">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="f3713-142">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="f3713-142">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="f3713-143">**IMF presentationdescriptor**</span><span class="sxs-lookup"><span data-stu-id="f3713-143">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="f3713-144">Präsentations deskriptorattribute</span><span class="sxs-lookup"><span data-stu-id="f3713-144">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="f3713-145">ASF-Header Objekt</span><span class="sxs-lookup"><span data-stu-id="f3713-145">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="f3713-146">Präsentations Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="f3713-146">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




