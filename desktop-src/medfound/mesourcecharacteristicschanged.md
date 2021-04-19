---
description: Wird von einer Medienquelle ausgelöst, wenn sich die Merkmale der Quellen ändern.
ms.assetid: df7bb9a3-5949-4a4a-8835-c5b1d01b5cb3
title: Mesourcecharakteristicschangi-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 659e9eea0352d131aac4959b2952e8426ae408a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349107"
---
# <a name="mesourcecharacteristicschanged-event"></a><span data-ttu-id="c307c-103">Mesourcecharakteristicschge-Ereignis</span><span class="sxs-lookup"><span data-stu-id="c307c-103">MESourceCharacteristicsChanged event</span></span>

<span data-ttu-id="c307c-104">Wird von einer Medienquelle ausgelöst, wenn sich die Merkmale der Quelle ändern.</span><span class="sxs-lookup"><span data-stu-id="c307c-104">Raised by a media source when the source's characteristics change.</span></span>

## <a name="event-values"></a><span data-ttu-id="c307c-105">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="c307c-105">Event values</span></span>

<span data-ttu-id="c307c-106">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="c307c-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="c307c-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="c307c-107">VARTYPE</span></span>              | <span data-ttu-id="c307c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c307c-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="c307c-109">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="c307c-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="c307c-110">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="c307c-110">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="c307c-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="c307c-111">Attributes</span></span>

<span data-ttu-id="c307c-112">Für dieses Ereignis sind die folgenden Attribute definiert:</span><span class="sxs-lookup"><span data-stu-id="c307c-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="c307c-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="c307c-113">Attribute</span></span>                                                                                                   | <span data-ttu-id="c307c-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c307c-114">Description</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="c307c-115">**Eigenschaften der MF- \_ Ereignis \_ Quelle \_**</span><span class="sxs-lookup"><span data-stu-id="c307c-115">**MF\_EVENT\_SOURCE\_CHARACTERISTICS**</span></span>](mf-event-source-characteristics-attribute.md)<br/>          | <span data-ttu-id="c307c-116">Neue Merkmale der Medienquelle.</span><span class="sxs-lookup"><span data-stu-id="c307c-116">New characteristics of the media source.</span></span><br/> <br/>      |
| [<span data-ttu-id="c307c-117">**Eigenschaften der MF- \_ Ereignis \_ Quelle \_ \_ alt**</span><span class="sxs-lookup"><span data-stu-id="c307c-117">**MF\_EVENT\_SOURCE\_CHARACTERISTICS\_OLD**</span></span>](mf-event-source-characteristics-old-attribute.md)<br/> | <span data-ttu-id="c307c-118">Vorherige Merkmale der Medienquelle.</span><span class="sxs-lookup"><span data-stu-id="c307c-118">Previous characteristics of the media source.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="c307c-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c307c-119">Requirements</span></span>



| <span data-ttu-id="c307c-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c307c-120">Requirement</span></span> | <span data-ttu-id="c307c-121">Wert</span><span class="sxs-lookup"><span data-stu-id="c307c-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c307c-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c307c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c307c-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c307c-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c307c-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c307c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c307c-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c307c-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c307c-126">Header</span><span class="sxs-lookup"><span data-stu-id="c307c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c307c-127"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c307c-127"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c307c-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c307c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c307c-129">**Imfmediasource**</span><span class="sxs-lookup"><span data-stu-id="c307c-129">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
</dt> <dt>

[<span data-ttu-id="c307c-130">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c307c-130">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




