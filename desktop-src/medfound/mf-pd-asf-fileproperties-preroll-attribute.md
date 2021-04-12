---
description: Gibt die Zeitspanne (in Millisekunden) an, mit der Daten vor der Wiedergabe einer ASF-Datei (Advanced Systems Format) gepuffert werden.
ms.assetid: 6aebe1cf-bd45-4b02-a3c8-6599bb683d7c
title: MF_PD_ASF_FILEPROPERTIES_PREROLL-Attribut (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 502ba715cc2802f9710d579e0c7afd6477b83454
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217029"
---
# <a name="mf_pd_asf_fileproperties_preroll-attribute"></a><span data-ttu-id="fbad8-103">Das \_ Attribut "MF PD \_ ASF \_ File Properties \_ Preroll"</span><span class="sxs-lookup"><span data-stu-id="fbad8-103">MF\_PD\_ASF\_FILEPROPERTIES\_PREROLL attribute</span></span>

<span data-ttu-id="fbad8-104">Gibt die Zeitspanne (in Millisekunden) an, mit der Daten vor der Wiedergabe einer ASF-Datei (Advanced Systems Format) gepuffert werden.</span><span class="sxs-lookup"><span data-stu-id="fbad8-104">Specifies the amount of time, in milliseconds, to buffer data before playing an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="fbad8-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="fbad8-105">Data type</span></span>

<span data-ttu-id="fbad8-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="fbad8-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="fbad8-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fbad8-107">Remarks</span></span>

<span data-ttu-id="fbad8-108">Dieses Attribut gilt für Präsentations Deskriptoren für den ASF-Inhalt.</span><span class="sxs-lookup"><span data-stu-id="fbad8-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="fbad8-109">Die [**imfasf ContentInfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) -Methode generiert dieses Attribut aus den ASF-Metadaten.</span><span class="sxs-lookup"><span data-stu-id="fbad8-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbad8-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fbad8-110">Requirements</span></span>



| <span data-ttu-id="fbad8-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fbad8-111">Requirement</span></span> | <span data-ttu-id="fbad8-112">Wert</span><span class="sxs-lookup"><span data-stu-id="fbad8-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbad8-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fbad8-113">Minimum supported client</span></span><br/> | <span data-ttu-id="fbad8-114">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fbad8-114">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="fbad8-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fbad8-115">Minimum supported server</span></span><br/> | <span data-ttu-id="fbad8-116">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fbad8-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fbad8-117">Header</span><span class="sxs-lookup"><span data-stu-id="fbad8-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="fbad8-118"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbad8-118"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbad8-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fbad8-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbad8-120">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="fbad8-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="fbad8-121">**Imfattributes:: GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="fbad8-121">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="fbad8-122">**Imfattributes:: SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="fbad8-122">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="fbad8-123">**IMF presentationdescriptor**</span><span class="sxs-lookup"><span data-stu-id="fbad8-123">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="fbad8-124">Präsentations deskriptorattribute</span><span class="sxs-lookup"><span data-stu-id="fbad8-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="fbad8-125">ASF-Header Objekt</span><span class="sxs-lookup"><span data-stu-id="fbad8-125">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="fbad8-126">Präsentations Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="fbad8-126">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




