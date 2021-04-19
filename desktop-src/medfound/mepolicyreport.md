---
description: Wird von einer vertrauenswürdigen Ausgabe ausgelöst, um Statusinformationen zur Durchsetzung der Ausgabe Richtlinie zu senden.
ms.assetid: 4906f6c3-1570-421f-aef1-914bd338bb1f
title: Mepolicyreport-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a0053fb551a69b820beeb4237211cb9af446f97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372944"
---
# <a name="mepolicyreport-event"></a><span data-ttu-id="f75ae-103">Mepolicyreport-Ereignis</span><span class="sxs-lookup"><span data-stu-id="f75ae-103">MEPolicyReport event</span></span>

<span data-ttu-id="f75ae-104">Wird von einer vertrauenswürdigen Ausgabe ausgelöst, um Statusinformationen zur Durchsetzung der Ausgabe Richtlinie zu senden.</span><span class="sxs-lookup"><span data-stu-id="f75ae-104">Raised by a trusted output to send status information about the enforcement of the output policy.</span></span>

## <a name="event-values"></a><span data-ttu-id="f75ae-105">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="f75ae-105">Event values</span></span>

<span data-ttu-id="f75ae-106">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="f75ae-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="f75ae-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="f75ae-107">VARTYPE</span></span>              | <span data-ttu-id="f75ae-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f75ae-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="f75ae-109">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="f75ae-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="f75ae-110">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="f75ae-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="f75ae-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f75ae-111">Remarks</span></span>

<span data-ttu-id="f75ae-112">Die Attribute und Statuscodes für dieses Ereignis hängen von dem spezifischen Inhalts Schutzsystem ab, das von der vertrauenswürdigen Ausgabe erzwungen wird.</span><span class="sxs-lookup"><span data-stu-id="f75ae-112">Attributes and status codes for this event depend on the specific content protection system enforced by the trusted output.</span></span>

## <a name="requirements"></a><span data-ttu-id="f75ae-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f75ae-113">Requirements</span></span>



| <span data-ttu-id="f75ae-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f75ae-114">Requirement</span></span> | <span data-ttu-id="f75ae-115">Wert</span><span class="sxs-lookup"><span data-stu-id="f75ae-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f75ae-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f75ae-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f75ae-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f75ae-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f75ae-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f75ae-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f75ae-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f75ae-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f75ae-120">Header</span><span class="sxs-lookup"><span data-stu-id="f75ae-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f75ae-121"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f75ae-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f75ae-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f75ae-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f75ae-123">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f75ae-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




