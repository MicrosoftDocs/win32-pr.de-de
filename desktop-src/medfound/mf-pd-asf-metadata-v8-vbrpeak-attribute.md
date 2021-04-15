---
description: Gibt die höchste momentane Bitrate in einer (VBR) (VBR) Advanced Systems Format (ASF)-Datei an.
ms.assetid: a31f447d-b718-4f8d-b0d5-643497339557
title: MF_PD_ASF_METADATA_V8_VBRPEAK-Attribut (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62d987815fea919bb46bbe5758e48d6eb22dad8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529549"
---
# <a name="mf_pd_asf_metadata_v8_vbrpeak-attribute"></a><span data-ttu-id="945e4-103">MF \_ PD \_ ASF \_ Metadata, \_ V8 \_ vbrpeak-Attribut</span><span class="sxs-lookup"><span data-stu-id="945e4-103">MF\_PD\_ASF\_METADATA\_V8\_VBRPEAK attribute</span></span>

<span data-ttu-id="945e4-104">Gibt die höchste momentane Bitrate in einer (VBR) (VBR) Advanced Systems Format (ASF)-Datei an.</span><span class="sxs-lookup"><span data-stu-id="945e4-104">Specifies the highest momentary bit rate in a variable bit rate (VBR) Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="945e4-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="945e4-105">Data type</span></span>

<span data-ttu-id="945e4-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="945e4-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="945e4-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="945e4-107">Remarks</span></span>

<span data-ttu-id="945e4-108">Dieses Attribut gilt für Präsentations Deskriptoren für den ASF-Inhalt.</span><span class="sxs-lookup"><span data-stu-id="945e4-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="945e4-109">Die [**imfasf ContentInfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) -Methode generiert dieses Attribut.</span><span class="sxs-lookup"><span data-stu-id="945e4-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute.</span></span>

> [!Note]  
> <span data-ttu-id="945e4-110">Dieses Attribut gilt nur für Dateien, die von Version 8 des Windows Media Format SDK erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="945e4-110">This attribute applies only to files created by version 8 of the Windows Media Format SDK.</span></span> <span data-ttu-id="945e4-111">Sie entspricht dem **vbrpeak** -Attribut im Windows Media-Format-SDK.</span><span class="sxs-lookup"><span data-stu-id="945e4-111">It corresponds to the **VBRPeak** attribute in the Windows Media Format SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="945e4-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="945e4-112">Requirements</span></span>



| <span data-ttu-id="945e4-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="945e4-113">Requirement</span></span> | <span data-ttu-id="945e4-114">Wert</span><span class="sxs-lookup"><span data-stu-id="945e4-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="945e4-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="945e4-115">Minimum supported client</span></span><br/> | <span data-ttu-id="945e4-116">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="945e4-116">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="945e4-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="945e4-117">Minimum supported server</span></span><br/> | <span data-ttu-id="945e4-118">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="945e4-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="945e4-119">Header</span><span class="sxs-lookup"><span data-stu-id="945e4-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="945e4-120"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="945e4-120"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="945e4-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="945e4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="945e4-122">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="945e4-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="945e4-123">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="945e4-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="945e4-124">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="945e4-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="945e4-125">**IMF presentationdescriptor**</span><span class="sxs-lookup"><span data-stu-id="945e4-125">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="945e4-126">Präsentations deskriptorattribute</span><span class="sxs-lookup"><span data-stu-id="945e4-126">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="945e4-127">ASF-Header Objekt</span><span class="sxs-lookup"><span data-stu-id="945e4-127">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="945e4-128">Präsentations Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="945e4-128">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




