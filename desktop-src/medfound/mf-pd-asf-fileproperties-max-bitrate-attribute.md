---
description: Gibt die maximale sofortige Bitrate in Bits pro Sekunde für eine ASF-Datei (Advanced Systems Format) an.
ms.assetid: 07e94448-13a9-4ea5-9ac7-a1e35668e0a0
title: MF_PD_ASF_FILEPROPERTIES_MAX_BITRATE-Attribut (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14b2c4d8b3061a0865bf3b2f3c2a4c1597c2c76f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864975"
---
# <a name="mf_pd_asf_fileproperties_max_bitrate-attribute"></a><span data-ttu-id="874fb-103">MF \_ PD \_ ASF \_ File Properties \_ Maximales \_ Bitrate-Attribut</span><span class="sxs-lookup"><span data-stu-id="874fb-103">MF\_PD\_ASF\_FILEPROPERTIES\_MAX\_BITRATE attribute</span></span>

<span data-ttu-id="874fb-104">Gibt die maximale sofortige Bitrate in Bits pro Sekunde für eine ASF-Datei (Advanced Systems Format) an.</span><span class="sxs-lookup"><span data-stu-id="874fb-104">Specifies the maximum instantaneous bit rate, in bits per second, for an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="874fb-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="874fb-105">Data type</span></span>

<span data-ttu-id="874fb-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="874fb-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="874fb-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="874fb-107">Remarks</span></span>

<span data-ttu-id="874fb-108">Dieses Attribut gilt für Präsentations Deskriptoren für den ASF-Inhalt.</span><span class="sxs-lookup"><span data-stu-id="874fb-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="874fb-109">Die [**imfasf ContentInfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) -Methode generiert dieses Attribut aus den ASF-Metadaten.</span><span class="sxs-lookup"><span data-stu-id="874fb-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="874fb-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="874fb-110">Requirements</span></span>



| <span data-ttu-id="874fb-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="874fb-111">Requirement</span></span> | <span data-ttu-id="874fb-112">Wert</span><span class="sxs-lookup"><span data-stu-id="874fb-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="874fb-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="874fb-113">Minimum supported client</span></span><br/> | <span data-ttu-id="874fb-114">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="874fb-114">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="874fb-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="874fb-115">Minimum supported server</span></span><br/> | <span data-ttu-id="874fb-116">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="874fb-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="874fb-117">Header</span><span class="sxs-lookup"><span data-stu-id="874fb-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="874fb-118"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="874fb-118"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="874fb-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="874fb-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="874fb-120">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="874fb-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="874fb-121">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="874fb-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="874fb-122">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="874fb-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="874fb-123">**IMF presentationdescriptor**</span><span class="sxs-lookup"><span data-stu-id="874fb-123">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="874fb-124">Präsentations deskriptorattribute</span><span class="sxs-lookup"><span data-stu-id="874fb-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="874fb-125">ASF-Header Objekt</span><span class="sxs-lookup"><span data-stu-id="874fb-125">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="874fb-126">Präsentations Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="874fb-126">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




