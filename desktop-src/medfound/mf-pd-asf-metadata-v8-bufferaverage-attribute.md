---
description: Gibt die durchschnittliche Puffergröße an, die für eine (VBR) Advanced Systems Format (ASF)-Datei (Variable Bitrate) benötigt wird.
ms.assetid: 508d8670-5f5f-422b-9fa1-150115e2dbb8
title: MF_PD_ASF_METADATA_V8_BUFFERAVERAGE-Attribut (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3f1efcb464ee62a1f3838c1a684e3c87dc58227
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360099"
---
# <a name="mf_pd_asf_metadata_v8_bufferaverage-attribute"></a><span data-ttu-id="f3544-103">MF \_ PD \_ ASF \_ Metadata, \_ V8 \_ bufferaverage-Attribut</span><span class="sxs-lookup"><span data-stu-id="f3544-103">MF\_PD\_ASF\_METADATA\_V8\_BUFFERAVERAGE attribute</span></span>

<span data-ttu-id="f3544-104">Gibt die durchschnittliche Puffergröße an, die für eine (VBR) Advanced Systems Format (ASF)-Datei (Variable Bitrate) benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="f3544-104">Specifies the average buffer size needed for a variable bit rate (VBR) Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="f3544-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="f3544-105">Data type</span></span>

<span data-ttu-id="f3544-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f3544-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="f3544-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f3544-107">Remarks</span></span>

<span data-ttu-id="f3544-108">Dieses Attribut gilt für Präsentations Deskriptoren für den ASF-Inhalt.</span><span class="sxs-lookup"><span data-stu-id="f3544-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="f3544-109">Die [**imfasfcontentinfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) -Methode generiert dieses Attribut, das für den Präsentations Deskriptor für den ASF-Inhalt gilt.</span><span class="sxs-lookup"><span data-stu-id="f3544-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute that applies to the presentation descriptor for ASF content.</span></span>

> [!Note]  
> <span data-ttu-id="f3544-110">Dieses Attribut gilt nur für Dateien, die von Version 8 des Windows Media Format SDK erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="f3544-110">This attribute applies only to files created by version 8 of the Windows Media Format SDK.</span></span> <span data-ttu-id="f3544-111">Sie entspricht dem **bufferaverage** -Attribut im Windows Media-Format-SDK.</span><span class="sxs-lookup"><span data-stu-id="f3544-111">It corresponds to the **BufferAverage** attribute in the Windows Media Format SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f3544-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f3544-112">Requirements</span></span>



| <span data-ttu-id="f3544-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f3544-113">Requirement</span></span> | <span data-ttu-id="f3544-114">Wert</span><span class="sxs-lookup"><span data-stu-id="f3544-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3544-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f3544-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f3544-116">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f3544-116">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f3544-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f3544-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f3544-118">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f3544-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f3544-119">Header</span><span class="sxs-lookup"><span data-stu-id="f3544-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3544-120"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3544-120"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3544-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f3544-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3544-122">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="f3544-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f3544-123">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="f3544-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="f3544-124">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="f3544-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="f3544-125">**IMF presentationdescriptor**</span><span class="sxs-lookup"><span data-stu-id="f3544-125">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="f3544-126">Präsentations deskriptorattribute</span><span class="sxs-lookup"><span data-stu-id="f3544-126">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="f3544-127">ASF-Header Objekt</span><span class="sxs-lookup"><span data-stu-id="f3544-127">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="f3544-128">Präsentations Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="f3544-128">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




