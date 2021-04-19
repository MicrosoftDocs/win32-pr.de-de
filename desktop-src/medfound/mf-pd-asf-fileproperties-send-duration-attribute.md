---
description: Gibt die Zeit in 100-Nanosekunden-Einheiten an, die zum Senden einer ASF-Datei (Advanced Systems Format) benötigt werden. Eine Sende Zeit für Pakete ist die Zeit, zu der das Paket über das Netzwerk übermittelt werden soll. Es handelt sich nicht um die Präsentationszeit des Pakets.
ms.assetid: 2bd427e2-106d-4997-86aa-fae221e429eb
title: MF_PD_ASF_FILEPROPERTIES_SEND_DURATION-Attribut (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: deed3f78208a0f0c7e555e8113f05ac0800cdb97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362607"
---
# <a name="mf_pd_asf_fileproperties_send_duration-attribute"></a><span data-ttu-id="de5e2-105">MF \_ PD \_ ASF \_ FileProperties \_ Send \_ Duration-Attribut</span><span class="sxs-lookup"><span data-stu-id="de5e2-105">MF\_PD\_ASF\_FILEPROPERTIES\_SEND\_DURATION attribute</span></span>

<span data-ttu-id="de5e2-106">Gibt die Zeit in 100-Nanosekunden-Einheiten an, die zum Senden einer ASF-Datei (Advanced Systems Format) benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="de5e2-106">Specifies the time, in 100-nanosecond units, needed to send an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="de5e2-107">Die *Sendezeit* eines Pakets ist die Zeit, zu der das Paket über das Netzwerk übermittelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="de5e2-107">A packet's *send time* is the time when the packet should be delivered over the network.</span></span> <span data-ttu-id="de5e2-108">Es handelt sich nicht um die Präsentationszeit des Pakets.</span><span class="sxs-lookup"><span data-stu-id="de5e2-108">It is not the presentation time of the packet.</span></span>

## <a name="data-type"></a><span data-ttu-id="de5e2-109">Datentyp</span><span class="sxs-lookup"><span data-stu-id="de5e2-109">Data type</span></span>

<span data-ttu-id="de5e2-110">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="de5e2-110">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="de5e2-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="de5e2-111">Remarks</span></span>

<span data-ttu-id="de5e2-112">Dieses Attribut gilt für Präsentations Deskriptoren für den ASF-Inhalt.</span><span class="sxs-lookup"><span data-stu-id="de5e2-112">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="de5e2-113">Die [**imfasf ContentInfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) -Methode generiert dieses Attribut aus den ASF-Metadaten.</span><span class="sxs-lookup"><span data-stu-id="de5e2-113">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="de5e2-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de5e2-114">Requirements</span></span>



| <span data-ttu-id="de5e2-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de5e2-115">Requirement</span></span> | <span data-ttu-id="de5e2-116">Wert</span><span class="sxs-lookup"><span data-stu-id="de5e2-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="de5e2-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="de5e2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="de5e2-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de5e2-118">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="de5e2-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="de5e2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="de5e2-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de5e2-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="de5e2-121">Header</span><span class="sxs-lookup"><span data-stu-id="de5e2-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="de5e2-122"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="de5e2-122"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de5e2-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de5e2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de5e2-124">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="de5e2-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="de5e2-125">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="de5e2-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="de5e2-126">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="de5e2-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="de5e2-127">**IMF presentationdescriptor**</span><span class="sxs-lookup"><span data-stu-id="de5e2-127">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="de5e2-128">Präsentations deskriptorattribute</span><span class="sxs-lookup"><span data-stu-id="de5e2-128">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="de5e2-129">ASF-Header Objekt</span><span class="sxs-lookup"><span data-stu-id="de5e2-129">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="de5e2-130">Präsentations Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="de5e2-130">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




