---
description: Gibt an, ob die Audiodatenströme in einer Präsentation eine Variable Bitrate aufweisen.
ms.assetid: 2bd7eee1-5a93-4bde-8b58-80b6395a094e
title: MF_PD_AUDIO_ISVARIABLEBITRATE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a34d3dd64f9100050dc9aae37e811d00c9d58af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216879"
---
# <a name="mf_pd_audio_isvariablebitrate-attribute"></a><span data-ttu-id="e1928-103">MF \_ PD \_ - \_ audioattribut "isvariablebitrate"</span><span class="sxs-lookup"><span data-stu-id="e1928-103">MF\_PD\_AUDIO\_ISVARIABLEBITRATE attribute</span></span>

<span data-ttu-id="e1928-104">Gibt an, ob die Audiodatenströme in einer Präsentation eine Variable Bitrate aufweisen.</span><span class="sxs-lookup"><span data-stu-id="e1928-104">Specifies whether the audio streams in a presentation have a variable bit rate.</span></span>

## <a name="data-type"></a><span data-ttu-id="e1928-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="e1928-105">Data type</span></span>

<span data-ttu-id="e1928-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="e1928-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="e1928-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="e1928-107">Get/set</span></span>

<span data-ttu-id="e1928-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="e1928-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="e1928-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="e1928-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="e1928-110">Gilt für</span><span class="sxs-lookup"><span data-stu-id="e1928-110">Applies To</span></span>

[<span data-ttu-id="e1928-111">**IMF presentationdescriptor**</span><span class="sxs-lookup"><span data-stu-id="e1928-111">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a><span data-ttu-id="e1928-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e1928-112">Remarks</span></span>

<span data-ttu-id="e1928-113">Dies ist ein optionales Attribut für Präsentations Deskriptoren.</span><span class="sxs-lookup"><span data-stu-id="e1928-113">This is an optional attribute for presentation descriptors.</span></span> <span data-ttu-id="e1928-114">Wenn das Attribut **true** (ungleich null) ist, enthält die Präsentation mindestens einen Audiostream mit variabler Bitrate (VBR).</span><span class="sxs-lookup"><span data-stu-id="e1928-114">If the attribute is **TRUE** (nonzero), the presentation contains at least one variable-bit-rate (VBR) audio stream.</span></span> <span data-ttu-id="e1928-115">Wenn das Attribut **false** ist, haben alle Audiostreams eine Konstante Bitrate.</span><span class="sxs-lookup"><span data-stu-id="e1928-115">If the attribute is **FALSE**, all of the audio streams have a constant bit rate.</span></span>

<span data-ttu-id="e1928-116">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="e1928-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1928-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e1928-117">Requirements</span></span>



| <span data-ttu-id="e1928-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e1928-118">Requirement</span></span> | <span data-ttu-id="e1928-119">Wert</span><span class="sxs-lookup"><span data-stu-id="e1928-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e1928-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e1928-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e1928-121">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="e1928-121">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="e1928-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e1928-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e1928-123">Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="e1928-123">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="e1928-124">Header</span><span class="sxs-lookup"><span data-stu-id="e1928-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1928-125"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1928-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1928-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e1928-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1928-127">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="e1928-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e1928-128">Präsentations deskriptorattribute</span><span class="sxs-lookup"><span data-stu-id="e1928-128">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




