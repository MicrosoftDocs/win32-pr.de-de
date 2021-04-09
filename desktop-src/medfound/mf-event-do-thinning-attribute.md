---
description: Wenn eine Medienquelle eine neue Wiedergabe Rate anfordert, gibt dieses Attribut an, ob die Quelle auch eine Verdünnung anfordert. Eine Definition der Verdünnung finden Sie unter Informationen zur Raten Kontrolle.
ms.assetid: 42b6d0b3-e5af-4a48-969c-53628d1b7c31
title: MF_EVENT_DO_THINNING-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a08807413881a13789c50dbf2d063693e7e4539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959048"
---
# <a name="mf_event_do_thinning-attribute"></a><span data-ttu-id="5d5de-104">MF-Ereignis, das das \_ \_ Attribut durch \_ dünden</span><span class="sxs-lookup"><span data-stu-id="5d5de-104">MF\_EVENT\_DO\_THINNING attribute</span></span>

<span data-ttu-id="5d5de-105">Wenn eine Medienquelle eine neue Wiedergabe Rate anfordert, gibt dieses Attribut an, ob die Quelle auch eine Verdünnung anfordert.</span><span class="sxs-lookup"><span data-stu-id="5d5de-105">When a media source requests a new playback rate, this attribute specifies whether the source also requests thinning.</span></span> <span data-ttu-id="5d5de-106">Eine Definition der Verdünnung finden Sie unter [Informationen zur Raten Kontrolle](about-rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="5d5de-106">For a definition of thinning, see [About Rate Control](about-rate-control.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="5d5de-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5d5de-107">Data type</span></span>

<span data-ttu-id="5d5de-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="5d5de-108">**UINT32**</span></span>

<span data-ttu-id="5d5de-109">Als booleschen Wert behandeln.</span><span class="sxs-lookup"><span data-stu-id="5d5de-109">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d5de-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5d5de-110">Remarks</span></span>

<span data-ttu-id="5d5de-111">Dieses Attribut wird mit dem [mesourceratechangerequused](mesourceratechangerequested.md) -Ereignis verwendet.</span><span class="sxs-lookup"><span data-stu-id="5d5de-111">This attribute is used with the [MESourceRateChangeRequested](mesourceratechangerequested.md) event.</span></span> <span data-ttu-id="5d5de-112">Wenn der Wert **true** ist, fordert die Medienquelle einen Switch zur dünnen Wiedergabe an.</span><span class="sxs-lookup"><span data-stu-id="5d5de-112">If the value is **TRUE**, the media source is requesting a switch to thinned playback.</span></span>

<span data-ttu-id="5d5de-113">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="5d5de-113">The default value is **FALSE**.</span></span>

<span data-ttu-id="5d5de-114">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="5d5de-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d5de-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5d5de-115">Requirements</span></span>



| <span data-ttu-id="5d5de-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5d5de-116">Requirement</span></span> | <span data-ttu-id="5d5de-117">Wert</span><span class="sxs-lookup"><span data-stu-id="5d5de-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5d5de-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5d5de-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5d5de-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5d5de-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5d5de-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5d5de-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5d5de-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5d5de-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5d5de-122">Header</span><span class="sxs-lookup"><span data-stu-id="5d5de-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d5de-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d5de-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d5de-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5d5de-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d5de-125">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="5d5de-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5d5de-126">Ereignisattribute</span><span class="sxs-lookup"><span data-stu-id="5d5de-126">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="5d5de-127">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="5d5de-127">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="5d5de-128">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="5d5de-128">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




