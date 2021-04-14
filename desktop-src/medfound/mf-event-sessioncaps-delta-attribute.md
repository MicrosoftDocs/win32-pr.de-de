---
description: Enthält Flags, die angeben, welche Funktionen in der Medien Sitzung basierend auf der aktuellen Präsentation geändert wurden.
ms.assetid: aa01d17f-f2ac-4504-b278-3edd90ab8a23
title: MF_EVENT_SESSIONCAPS_DELTA-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 284a31a8d3fc661c15e7de991972455468efbd40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393533"
---
# <a name="mf_event_sessioncaps_delta-attribute"></a><span data-ttu-id="da66a-103">\_Delta-Ereignis \_ sessioncaps- \_ Delta Attribut</span><span class="sxs-lookup"><span data-stu-id="da66a-103">MF\_EVENT\_SESSIONCAPS\_DELTA attribute</span></span>

<span data-ttu-id="da66a-104">Enthält Flags, die angeben, welche Funktionen in der Medien Sitzung basierend auf der aktuellen Präsentation geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="da66a-104">Contains flags that indicate which capabilities have changed in the Media Session, based on the current presentation.</span></span>

## <a name="data-type"></a><span data-ttu-id="da66a-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="da66a-105">Data type</span></span>

<span data-ttu-id="da66a-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="da66a-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="da66a-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="da66a-107">Remarks</span></span>

<span data-ttu-id="da66a-108">Dieses Attribut enthält eine Bitmaske, die angibt, welche Funktionen Flags geändert haben.</span><span class="sxs-lookup"><span data-stu-id="da66a-108">This attribute contains a bitmask indicating which capabilities flags have changed.</span></span> <span data-ttu-id="da66a-109">Eine Liste möglicher Flags finden Sie unter [**imfmediasession:: gezession-Funktionen**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities).</span><span class="sxs-lookup"><span data-stu-id="da66a-109">For a list of possible flags, see [**IMFMediaSession::GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities).</span></span> <span data-ttu-id="da66a-110">Bits werden aus folgenden Gründen in der Bitmaske auf 1 festgelegt:</span><span class="sxs-lookup"><span data-stu-id="da66a-110">Bits are set to 1 in the bitmask for any of the following reasons:</span></span>

-   <span data-ttu-id="da66a-111">Das entsprechende Funktionen-Bit wurde von 0 in 1 geändert.</span><span class="sxs-lookup"><span data-stu-id="da66a-111">The corresponding capabilities bit changed from 0 to 1.</span></span>
-   <span data-ttu-id="da66a-112">Das entsprechende Funktionen-Bit wurde von 1 in 0 geändert.</span><span class="sxs-lookup"><span data-stu-id="da66a-112">The corresponding capabilities bit changed from 1 to 0.</span></span>
-   <span data-ttu-id="da66a-113">Das entsprechende Funktionen-Bit blieb 1, aber die Details der Funktion wurden geändert.</span><span class="sxs-lookup"><span data-stu-id="da66a-113">The corresponding capabilities bit remained 1, but the details of the capability changed.</span></span> <span data-ttu-id="da66a-114">Beispielsweise wurde die maximale Wiedergabe Rate geändert.</span><span class="sxs-lookup"><span data-stu-id="da66a-114">For example, the maximum playback rate changed.</span></span>

<span data-ttu-id="da66a-115">Dieses Attribut wird mit dem [mesessioncapabilitieschge](mesessioncapabilitieschanged.md) -Ereignis verwendet.</span><span class="sxs-lookup"><span data-stu-id="da66a-115">This attribute is used with the [MESessionCapabilitiesChanged](mesessioncapabilitieschanged.md) event.</span></span>

<span data-ttu-id="da66a-116">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="da66a-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="da66a-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da66a-117">Requirements</span></span>



| <span data-ttu-id="da66a-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="da66a-118">Requirement</span></span> | <span data-ttu-id="da66a-119">Wert</span><span class="sxs-lookup"><span data-stu-id="da66a-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="da66a-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="da66a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="da66a-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="da66a-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="da66a-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="da66a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="da66a-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="da66a-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="da66a-124">Header</span><span class="sxs-lookup"><span data-stu-id="da66a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="da66a-125"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="da66a-125"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da66a-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da66a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da66a-127">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="da66a-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="da66a-128">Ereignisattribute</span><span class="sxs-lookup"><span data-stu-id="da66a-128">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="da66a-129">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="da66a-129">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="da66a-130">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="da66a-130">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




