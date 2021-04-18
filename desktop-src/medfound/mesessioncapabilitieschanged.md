---
description: Wird von der Medien Sitzung ausgelöst, wenn sich die Sitzungs Funktionen ändern.
ms.assetid: d59fd3a0-29db-434c-b6ba-d9beb33bd965
title: Mesessioncapabilitieschangi-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0612b705571c50a6adcbde4afe93b42a524a950
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357453"
---
# <a name="mesessioncapabilitieschanged-event"></a><span data-ttu-id="d12d6-103">Mesessioncapabilitieschangi-Ereignis</span><span class="sxs-lookup"><span data-stu-id="d12d6-103">MESessionCapabilitiesChanged event</span></span>

<span data-ttu-id="d12d6-104">Wird von der Medien Sitzung ausgelöst, wenn sich die Sitzungs Funktionen ändern.</span><span class="sxs-lookup"><span data-stu-id="d12d6-104">Raised by the Media Session when the session capabilities change.</span></span>

## <a name="event-values"></a><span data-ttu-id="d12d6-105">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="d12d6-105">Event values</span></span>

<span data-ttu-id="d12d6-106">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="d12d6-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="d12d6-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="d12d6-107">VARTYPE</span></span>              | <span data-ttu-id="d12d6-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d12d6-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="d12d6-109">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="d12d6-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="d12d6-110">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="d12d6-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="d12d6-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d12d6-111">Remarks</span></span>

<span data-ttu-id="d12d6-112">Das Ereignis enthält die folgenden Attribute.</span><span class="sxs-lookup"><span data-stu-id="d12d6-112">The event contains the following attributes.</span></span>



| <span data-ttu-id="d12d6-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="d12d6-113">Attribute</span></span>                                                                     | <span data-ttu-id="d12d6-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d12d6-114">Description</span></span>                                      |
|-------------------------------------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="d12d6-115">**MF- \_ Ereignis \_ sessioncaps**</span><span class="sxs-lookup"><span data-stu-id="d12d6-115">**MF\_EVENT\_SESSIONCAPS**</span></span>](mf-event-sessioncaps-attribute.md)              | <span data-ttu-id="d12d6-116">Neue sitzungsfunktions-Flags.</span><span class="sxs-lookup"><span data-stu-id="d12d6-116">New session capabilities flags.</span></span>                  |
| [<span data-ttu-id="d12d6-117">**\_Delta-Ereignis \_ sessioncaps- \_ Delta**</span><span class="sxs-lookup"><span data-stu-id="d12d6-117">**MF\_EVENT\_SESSIONCAPS\_DELTA**</span></span>](mf-event-sessioncaps-delta-attribute.md) | <span data-ttu-id="d12d6-118">Gibt an, welche Funktionen Flags geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="d12d6-118">Indicates which capabilities flags have changed.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="d12d6-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d12d6-119">Requirements</span></span>



| <span data-ttu-id="d12d6-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d12d6-120">Requirement</span></span> | <span data-ttu-id="d12d6-121">Wert</span><span class="sxs-lookup"><span data-stu-id="d12d6-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d12d6-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d12d6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d12d6-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d12d6-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d12d6-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d12d6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d12d6-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d12d6-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d12d6-126">Header</span><span class="sxs-lookup"><span data-stu-id="d12d6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d12d6-127"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d12d6-127"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d12d6-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d12d6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d12d6-129">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d12d6-129">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




