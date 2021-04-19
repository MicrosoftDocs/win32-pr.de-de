---
description: 'Wird von einer Output Trust Authority (OTA) ausgelöst, wenn die IMF outputtrustauthority:: setpolicy-Methode asynchron abgeschlossen wird.'
ms.assetid: c5d8a88e-2864-45a0-97b7-051341116a4c
title: MEPolicySet-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 238af6cbd740e62825ae0b661769c1cf1bf880ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356605"
---
# <a name="mepolicyset-event"></a><span data-ttu-id="ec8e3-103">MEPolicySet-Ereignis</span><span class="sxs-lookup"><span data-stu-id="ec8e3-103">MEPolicySet event</span></span>

<span data-ttu-id="ec8e3-104">Wird von einer Output Trust Authority (OTA) ausgelöst, wenn die [**IMF outputtrustauthority:: setpolicy**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputtrustauthority-setpolicy) -Methode asynchron abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="ec8e3-104">Raised by an output trust authority (OTA) when the [**IMFOutputTrustAuthority::SetPolicy**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputtrustauthority-setpolicy) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="ec8e3-105">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="ec8e3-105">Event values</span></span>

<span data-ttu-id="ec8e3-106">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="ec8e3-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="ec8e3-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="ec8e3-107">VARTYPE</span></span>              | <span data-ttu-id="ec8e3-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ec8e3-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="ec8e3-109">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="ec8e3-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="ec8e3-110">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="ec8e3-110">No event data.</span></span><br/> <br/> |
| <span data-ttu-id="ec8e3-111">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="ec8e3-111">VT\_UI4</span></span><br/> | <span data-ttu-id="ec8e3-112">Ein Bezeichner, der für eine [IMF outputpolicy](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy) über das [MF_POLICY_ID](mf-policy-id.md) -Attribut festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="ec8e3-112">An identifier that can be set on an [IMFOutputPolicy](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy) through the [MF_POLICY_ID](mf-policy-id.md) attribute.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="ec8e3-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ec8e3-113">Requirements</span></span>



| <span data-ttu-id="ec8e3-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ec8e3-114">Requirement</span></span> | <span data-ttu-id="ec8e3-115">Wert</span><span class="sxs-lookup"><span data-stu-id="ec8e3-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec8e3-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ec8e3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ec8e3-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ec8e3-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ec8e3-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ec8e3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ec8e3-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ec8e3-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ec8e3-120">Header</span><span class="sxs-lookup"><span data-stu-id="ec8e3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec8e3-121"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ec8e3-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec8e3-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ec8e3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec8e3-123">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ec8e3-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




