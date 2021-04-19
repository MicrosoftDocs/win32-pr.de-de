---
description: Wird von einer vertrauenswürdigen Ausgabe ausgelöst, wenn beim Erzwingen der Ausgabe Richtlinie ein Fehler auftritt.
ms.assetid: 0cc62915-1ed6-4d1d-9600-0dac0b9034e3
title: Mepolicyerror-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b75083974ee0e76d7d8e21f0a2c83c2feee8d59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348518"
---
# <a name="mepolicyerror-event"></a><span data-ttu-id="27602-103">Mepolicyerror-Ereignis</span><span class="sxs-lookup"><span data-stu-id="27602-103">MEPolicyError event</span></span>

<span data-ttu-id="27602-104">Wird von einer vertrauenswürdigen Ausgabe ausgelöst, wenn beim Erzwingen der Ausgabe Richtlinie ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="27602-104">Raised by a trusted output if an error occurs while enforcing the output policy.</span></span>

<span data-ttu-id="27602-105">Wenn die Medien Sitzung dieses Ereignis empfängt, beendet Sie die Wiedergabe und leitet das Ereignis an die Anwendung weiter.</span><span class="sxs-lookup"><span data-stu-id="27602-105">If the Media Session receives this event, it stops playback and forwards the event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="27602-106">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="27602-106">Event values</span></span>

<span data-ttu-id="27602-107">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="27602-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="27602-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="27602-108">VARTYPE</span></span>              | <span data-ttu-id="27602-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="27602-109">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="27602-110">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="27602-110">VT\_EMPTY</span></span><br/> | <span data-ttu-id="27602-111">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="27602-111">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="27602-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="27602-112">Remarks</span></span>

<span data-ttu-id="27602-113">Mögliche Werte, die von [**imfmediaevent:: GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) abgerufen werden, sind die folgenden.</span><span class="sxs-lookup"><span data-stu-id="27602-113">Possible values retrieved from [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) include the following.</span></span>



| <span data-ttu-id="27602-114">Wert</span><span class="sxs-lookup"><span data-stu-id="27602-114">Value</span></span>                      | <span data-ttu-id="27602-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="27602-115">Description</span></span>                                                    |
|----------------------------|----------------------------------------------------------------|
| <span data-ttu-id="27602-116">MF \_ E- \_ Richtlinie \_ nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="27602-116">MF\_E\_POLICY\_UNSUPPORTED</span></span> | <span data-ttu-id="27602-117">Die vertrauenswürdige Ausgabe unterstützt die aktuelle Ausgabe Richtlinie nicht.</span><span class="sxs-lookup"><span data-stu-id="27602-117">The trusted output does not support the current output policy.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="27602-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="27602-118">Requirements</span></span>



| <span data-ttu-id="27602-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="27602-119">Requirement</span></span> | <span data-ttu-id="27602-120">Wert</span><span class="sxs-lookup"><span data-stu-id="27602-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27602-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="27602-121">Minimum supported client</span></span><br/> | <span data-ttu-id="27602-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="27602-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="27602-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="27602-123">Minimum supported server</span></span><br/> | <span data-ttu-id="27602-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="27602-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="27602-125">Header</span><span class="sxs-lookup"><span data-stu-id="27602-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="27602-126"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="27602-126"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27602-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="27602-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27602-128">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="27602-128">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




