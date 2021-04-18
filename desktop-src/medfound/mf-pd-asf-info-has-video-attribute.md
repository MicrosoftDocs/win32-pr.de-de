---
description: Gibt an, ob eine ASF-Datei (Advanced Systems Format) mindestens einen Videostream enthält.
ms.assetid: 98411c75-519f-4ace-999f-1ea22457ed4a
title: MF_PD_ASF_INFO_HAS_VIDEO-Attribut (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c1a11f672ec4063d14131946ef4e1a820cc3ee7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347494"
---
# <a name="mf_pd_asf_info_has_video-attribute"></a><span data-ttu-id="8b183-103">MF \_ PD- \_ ASF- \_ Info \_ hat Video- \_ Attribut</span><span class="sxs-lookup"><span data-stu-id="8b183-103">MF\_PD\_ASF\_INFO\_HAS\_VIDEO attribute</span></span>

<span data-ttu-id="8b183-104">Gibt an, ob eine ASF-Datei (Advanced Systems Format) mindestens einen Videostream enthält.</span><span class="sxs-lookup"><span data-stu-id="8b183-104">Specifies whether an Advanced Systems Format (ASF) file contains at least one video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="8b183-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="8b183-105">Data type</span></span>

<span data-ttu-id="8b183-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="8b183-106">**UINT32**</span></span>

<span data-ttu-id="8b183-107">Als booleschen Wert behandeln.</span><span class="sxs-lookup"><span data-stu-id="8b183-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b183-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8b183-108">Remarks</span></span>

<span data-ttu-id="8b183-109">Dieses Attribut gilt für Präsentations Deskriptoren für den ASF-Inhalt.</span><span class="sxs-lookup"><span data-stu-id="8b183-109">This attribute applies to presentation descriptors for ASF content.</span></span> <span data-ttu-id="8b183-110">Wenn der Wert **true** ist, enthält die Datei mindestens einen Videostream.</span><span class="sxs-lookup"><span data-stu-id="8b183-110">If the value is **TRUE**, the file has at least one video stream.</span></span> <span data-ttu-id="8b183-111">Andernfalls enthält die Datei keine Videostreams.</span><span class="sxs-lookup"><span data-stu-id="8b183-111">Otherwise, the file does not contain any video streams.</span></span>

<span data-ttu-id="8b183-112">Die [**imfasf ContentInfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) -Methode generiert dieses Attribut aus den ASF-Metadaten.</span><span class="sxs-lookup"><span data-stu-id="8b183-112">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b183-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b183-113">Requirements</span></span>



| <span data-ttu-id="8b183-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8b183-114">Requirement</span></span> | <span data-ttu-id="8b183-115">Wert</span><span class="sxs-lookup"><span data-stu-id="8b183-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b183-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8b183-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8b183-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b183-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="8b183-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8b183-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8b183-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b183-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8b183-120">Header</span><span class="sxs-lookup"><span data-stu-id="8b183-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b183-121"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b183-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b183-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b183-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b183-123">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="8b183-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8b183-124">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="8b183-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="8b183-125">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="8b183-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="8b183-126">**IMF presentationdescriptor**</span><span class="sxs-lookup"><span data-stu-id="8b183-126">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="8b183-127">Präsentations deskriptorattribute</span><span class="sxs-lookup"><span data-stu-id="8b183-127">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="8b183-128">ASF-Header Objekt</span><span class="sxs-lookup"><span data-stu-id="8b183-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




