---
description: Gibt an, ob sich ein Stream mit anderen Streams desselben Typs gegenseitig ausschließt.
ms.assetid: 00a426ae-297c-4fcb-8132-d9c538bc9f1a
title: MF_SD_MUTUALLY_EXCLUSIVE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24e3604eb9424bb646766f57261f745c57e18f3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352402"
---
# <a name="mf_sd_mutually_exclusive-attribute"></a><span data-ttu-id="44957-103">\_ \_ Gegenseitig \_ Ausschließendes MF-Attribut</span><span class="sxs-lookup"><span data-stu-id="44957-103">MF\_SD\_MUTUALLY\_EXCLUSIVE attribute</span></span>

<span data-ttu-id="44957-104">Gibt an, ob sich ein Stream mit anderen Streams desselben Typs gegenseitig ausschließt.</span><span class="sxs-lookup"><span data-stu-id="44957-104">Specifies whether a stream is mutually exclusive with other streams of the same type.</span></span>

## <a name="data-type"></a><span data-ttu-id="44957-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="44957-105">Data type</span></span>

<span data-ttu-id="44957-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="44957-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="44957-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="44957-107">Get/set</span></span>

<span data-ttu-id="44957-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="44957-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="44957-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="44957-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="44957-110">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="44957-110">Applies to</span></span>

[<span data-ttu-id="44957-111">**IMF-Deskriptor**</span><span class="sxs-lookup"><span data-stu-id="44957-111">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)

## <a name="remarks"></a><span data-ttu-id="44957-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="44957-112">Remarks</span></span>

<span data-ttu-id="44957-113">Wenn dieses Attribut **true** (ungleich null) ist, schließt sich der Stream mit anderen Streams desselben Typs, z. b. Audiodaten oder Videos, innerhalb derselben Präsentation gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="44957-113">If this attribute is **TRUE** (nonzero), the stream is mutually exclusive with other streams of the same type, such as audio or video, within the same presentation.</span></span> <span data-ttu-id="44957-114">Wenn eine AVI-Datei z. b. mehrere Audiostreams enthält, werden Sie als gegenseitig ausschließende Datenströme gekennzeichnet, da jeweils nur ein Audiostream abgespielt werden soll.</span><span class="sxs-lookup"><span data-stu-id="44957-114">For example, if an AVI file contains multiple audio streams, they are marked as mutually exclusive, because only one audio stream should be played at one time.</span></span>

<span data-ttu-id="44957-115">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="44957-115">The default value is **FALSE**.</span></span>

> [!Note]  
> <span data-ttu-id="44957-116">Dieses Attribut wird nicht für ASF-Dateien (Advanced Systems Format) verwendet, die eine anspruchsvollere Methode zur Darstellung von gegenseitigen Ausschlusskriterien aufweisen.</span><span class="sxs-lookup"><span data-stu-id="44957-116">This attribute is not used for Advanced Systems Format (ASF) files, which have a more sophisticated way to represent mutual exclusion criteria.</span></span> <span data-ttu-id="44957-117">Weitere Informationen finden Sie unter [**imfasf mutualexclusion**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion).</span><span class="sxs-lookup"><span data-stu-id="44957-117">For more information, see [**IMFASFMutualExclusion**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion).</span></span>

 

<span data-ttu-id="44957-118">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="44957-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="44957-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="44957-119">Requirements</span></span>



| <span data-ttu-id="44957-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="44957-120">Requirement</span></span> | <span data-ttu-id="44957-121">Wert</span><span class="sxs-lookup"><span data-stu-id="44957-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="44957-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="44957-122">Minimum supported client</span></span><br/> | <span data-ttu-id="44957-123">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="44957-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="44957-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="44957-124">Minimum supported server</span></span><br/> | <span data-ttu-id="44957-125">Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="44957-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="44957-126">Header</span><span class="sxs-lookup"><span data-stu-id="44957-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="44957-127"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="44957-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44957-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="44957-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44957-129">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="44957-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="44957-130">Streamdeskriptorattribute</span><span class="sxs-lookup"><span data-stu-id="44957-130">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> </dl>

 

 




