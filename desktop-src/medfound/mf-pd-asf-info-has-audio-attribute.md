---
description: Gibt an, ob eine ASF-Datei (Advanced Systems Format) beliebige Audiostreams enthält.
ms.assetid: b7c5cd67-fd2a-49d8-8de5-61783a3b4577
title: MF_PD_ASF_INFO_HAS_AUDIO-Attribut (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5e2fbf9698e470af92cbd21fc5f26883dc5fd79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217027"
---
# <a name="mf_pd_asf_info_has_audio-attribute"></a><span data-ttu-id="4a799-103">MF \_ PD \_ \_ -ASF \_ -Info hat \_ audioattribut</span><span class="sxs-lookup"><span data-stu-id="4a799-103">MF\_PD\_ASF\_INFO\_HAS\_AUDIO attribute</span></span>

<span data-ttu-id="4a799-104">Gibt an, ob eine ASF-Datei (Advanced Systems Format) beliebige Audiostreams enthält.</span><span class="sxs-lookup"><span data-stu-id="4a799-104">Specifies whether an Advanced Systems Format (ASF) file contains any audio streams.</span></span>

## <a name="data-type"></a><span data-ttu-id="4a799-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="4a799-105">Data type</span></span>

<span data-ttu-id="4a799-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="4a799-106">**UINT32**</span></span>

<span data-ttu-id="4a799-107">Als booleschen Wert behandeln.</span><span class="sxs-lookup"><span data-stu-id="4a799-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a799-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4a799-108">Remarks</span></span>

<span data-ttu-id="4a799-109">Dieses Attribut gilt für Präsentations Deskriptoren für den ASF-Inhalt.</span><span class="sxs-lookup"><span data-stu-id="4a799-109">This attribute applies to presentation descriptors for ASF content.</span></span> <span data-ttu-id="4a799-110">Wenn der Wert **true** ist, enthält die Datei mindestens einen Audiodatenstrom.</span><span class="sxs-lookup"><span data-stu-id="4a799-110">If the value is **TRUE**, the file has at least one audio stream.</span></span> <span data-ttu-id="4a799-111">Andernfalls enthält die Datei keine Audiodatenströme.</span><span class="sxs-lookup"><span data-stu-id="4a799-111">Otherwise, the file does not contain any audio streams.</span></span>

<span data-ttu-id="4a799-112">Die [**imfasf ContentInfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) -Methode generiert dieses Attribut aus den ASF-Metadaten.</span><span class="sxs-lookup"><span data-stu-id="4a799-112">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a799-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4a799-113">Requirements</span></span>



| <span data-ttu-id="4a799-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4a799-114">Requirement</span></span> | <span data-ttu-id="4a799-115">Wert</span><span class="sxs-lookup"><span data-stu-id="4a799-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a799-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4a799-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4a799-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4a799-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4a799-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4a799-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4a799-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4a799-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4a799-120">Header</span><span class="sxs-lookup"><span data-stu-id="4a799-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a799-121"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a799-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a799-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a799-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a799-123">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="4a799-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4a799-124">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="4a799-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="4a799-125">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="4a799-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="4a799-126">**IMF presentationdescriptor**</span><span class="sxs-lookup"><span data-stu-id="4a799-126">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="4a799-127">Präsentations deskriptorattribute</span><span class="sxs-lookup"><span data-stu-id="4a799-127">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="4a799-128">ASF-Header Objekt</span><span class="sxs-lookup"><span data-stu-id="4a799-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




