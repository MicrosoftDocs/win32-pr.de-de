---
description: Gibt an, ob die Datei "Advanced Systems Format (ASF)" Streams enthält, die keine Audiodaten oder Videos enthalten.
ms.assetid: ccd61f50-29fb-4a50-80c9-d23d71d768f3
title: MF_PD_ASF_INFO_HAS_NON_AUDIO_VIDEO-Attribut (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12d1759427059494a8d0b84c64ac169ce640ab2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960191"
---
# <a name="mf_pd_asf_info_has_non_audio_video-attribute"></a><span data-ttu-id="4f840-103">MF \_ PD \_ \_ -ASF \_ -Info hat \_ nicht \_ \_ Audiovideo-Attribut</span><span class="sxs-lookup"><span data-stu-id="4f840-103">MF\_PD\_ASF\_INFO\_HAS\_NON\_AUDIO\_VIDEO attribute</span></span>

<span data-ttu-id="4f840-104">Gibt an, ob die Datei "Advanced Systems Format (ASF)" Streams enthält, die keine Audiodaten oder Videos enthalten.</span><span class="sxs-lookup"><span data-stu-id="4f840-104">Specifies whether an Advanced Systems Format (ASF) file contains any streams that are not audio or video.</span></span>

## <a name="data-type"></a><span data-ttu-id="4f840-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="4f840-105">Data type</span></span>

<span data-ttu-id="4f840-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="4f840-106">**UINT32**</span></span>

<span data-ttu-id="4f840-107">Als booleschen Wert behandeln.</span><span class="sxs-lookup"><span data-stu-id="4f840-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f840-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4f840-108">Remarks</span></span>

<span data-ttu-id="4f840-109">Dieses Attribut gilt für Präsentations Deskriptoren für den ASF-Inhalt.</span><span class="sxs-lookup"><span data-stu-id="4f840-109">This attribute applies to presentation descriptors for ASF content.</span></span> <span data-ttu-id="4f840-110">Wenn der Wert **true** ist, enthält die Datei mindestens einen Datenstrom, der weder Audiodaten noch Video enthält.</span><span class="sxs-lookup"><span data-stu-id="4f840-110">If the value is **TRUE**, the file has at least one stream that is not audio or video.</span></span> <span data-ttu-id="4f840-111">Beispiele hierfür sind Bild Datenströme, Skript Befehle und benutzerdefinierte beliebige Daten.</span><span class="sxs-lookup"><span data-stu-id="4f840-111">Examples include image streams, script commands, and custom arbitrary data.</span></span>

<span data-ttu-id="4f840-112">Die [**imfasf ContentInfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) -Methode generiert dieses Attribut aus den ASF-Metadaten.</span><span class="sxs-lookup"><span data-stu-id="4f840-112">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f840-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4f840-113">Requirements</span></span>



| <span data-ttu-id="4f840-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4f840-114">Requirement</span></span> | <span data-ttu-id="4f840-115">Wert</span><span class="sxs-lookup"><span data-stu-id="4f840-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f840-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4f840-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4f840-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4f840-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4f840-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4f840-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4f840-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4f840-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4f840-120">Header</span><span class="sxs-lookup"><span data-stu-id="4f840-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f840-121"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f840-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f840-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f840-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f840-123">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="4f840-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4f840-124">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="4f840-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="4f840-125">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="4f840-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="4f840-126">**IMF presentationdescriptor**</span><span class="sxs-lookup"><span data-stu-id="4f840-126">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="4f840-127">Präsentations deskriptorattribute</span><span class="sxs-lookup"><span data-stu-id="4f840-127">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="4f840-128">ASF-Header Objekt</span><span class="sxs-lookup"><span data-stu-id="4f840-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




