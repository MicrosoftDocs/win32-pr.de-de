---
description: Gibt an, ob für eine ASF-Datei (Advanced Systems Format) die VBR-Codierung (Variable Bitrate) verwendet wird.
ms.assetid: 69888d66-8e96-4a20-b8c5-a01267ff3c05
title: MF_PD_ASF_METADATA_IS_VBR-Attribut (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5863d5366fd94e230040f81d3f67f4c75fd3fe3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362351"
---
# <a name="mf_pd_asf_metadata_is_vbr-attribute"></a><span data-ttu-id="3dc53-103">MF \_ PD, \_ ASF- \_ Metadaten \_ sind \_ VBR-Attribut</span><span class="sxs-lookup"><span data-stu-id="3dc53-103">MF\_PD\_ASF\_METADATA\_IS\_VBR attribute</span></span>

<span data-ttu-id="3dc53-104">Gibt an, ob für eine ASF-Datei (Advanced Systems Format) die VBR-Codierung (Variable Bitrate) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3dc53-104">Specifies whether an Advanced Systems Format (ASF) file uses variable bit rate (VBR) encoding.</span></span>

## <a name="data-type"></a><span data-ttu-id="3dc53-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="3dc53-105">Data type</span></span>

<span data-ttu-id="3dc53-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="3dc53-106">**UINT32**</span></span>

<span data-ttu-id="3dc53-107">Als booleschen Wert behandeln.</span><span class="sxs-lookup"><span data-stu-id="3dc53-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3dc53-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3dc53-108">Remarks</span></span>

<span data-ttu-id="3dc53-109">Dieses Attribut gilt für Präsentations Deskriptoren für den ASF-Inhalt.</span><span class="sxs-lookup"><span data-stu-id="3dc53-109">This attribute applies to presentation descriptors for ASF content.</span></span> <span data-ttu-id="3dc53-110">Wenn der Wert **true** ist, wurde die Datei mit VBR codiert.</span><span class="sxs-lookup"><span data-stu-id="3dc53-110">If the value is **TRUE**, the file was encoded using VBR.</span></span> <span data-ttu-id="3dc53-111">Wenn der Wert **false** ist oder das Attribut nicht vorhanden ist, wird die VBR-Codierung in der Datei nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="3dc53-111">If the value is **FALSE** or the attribute is not present, the file does not use VBR encoding.</span></span>

<span data-ttu-id="3dc53-112">Die [**imfasf ContentInfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) -Methode generiert dieses Attribut und legt es für den Präsentations Deskriptor fest.</span><span class="sxs-lookup"><span data-stu-id="3dc53-112">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute and sets it on the presentation descriptor.</span></span>

> [!Note]  
> <span data-ttu-id="3dc53-113">Dieses Attribut entspricht dem **isvbr** -Attribut im Windows Media-Format-SDK.</span><span class="sxs-lookup"><span data-stu-id="3dc53-113">This attribute corresponds to the **IsVBR** attribute in the Windows Media Format SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3dc53-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3dc53-114">Requirements</span></span>



| <span data-ttu-id="3dc53-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3dc53-115">Requirement</span></span> | <span data-ttu-id="3dc53-116">Wert</span><span class="sxs-lookup"><span data-stu-id="3dc53-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3dc53-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3dc53-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3dc53-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3dc53-118">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3dc53-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3dc53-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3dc53-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3dc53-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3dc53-121">Header</span><span class="sxs-lookup"><span data-stu-id="3dc53-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3dc53-122"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="3dc53-122"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3dc53-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3dc53-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dc53-124">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="3dc53-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3dc53-125">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="3dc53-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="3dc53-126">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="3dc53-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="3dc53-127">**IMF presentationdescriptor**</span><span class="sxs-lookup"><span data-stu-id="3dc53-127">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="3dc53-128">Präsentations deskriptorattribute</span><span class="sxs-lookup"><span data-stu-id="3dc53-128">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="3dc53-129">ASF-Header Objekt</span><span class="sxs-lookup"><span data-stu-id="3dc53-129">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="3dc53-130">Präsentations Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="3dc53-130">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




