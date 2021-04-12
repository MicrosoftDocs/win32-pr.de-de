---
description: 'Wird von der Medien Sitzung ausgelöst, wenn die imfmediasession:: cleartopologien-Methode asynchron abgeschlossen wird.'
ms.assetid: 2017d13b-8dc2-48f9-a21e-7b826e174edf
title: Mesessiontopologieslöschte-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 551e98607a8d23d9333527337bbd7d038ed0b340
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130733"
---
# <a name="mesessiontopologiescleared-event"></a><span data-ttu-id="13af2-103">Mesessiontopologieslöschte-Ereignis</span><span class="sxs-lookup"><span data-stu-id="13af2-103">MESessionTopologiesCleared event</span></span>

<span data-ttu-id="13af2-104">Wird von der Medien Sitzung ausgelöst, wenn die [**imfmediasession:: cleartopologien**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-cleartopologies) -Methode asynchron abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="13af2-104">Raised by the Media Session when the [**IMFMediaSession::ClearTopologies**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-cleartopologies) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="13af2-105">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="13af2-105">Event values</span></span>

<span data-ttu-id="13af2-106">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="13af2-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="13af2-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="13af2-107">VARTYPE</span></span>              | <span data-ttu-id="13af2-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="13af2-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="13af2-109">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="13af2-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="13af2-110">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="13af2-110">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="13af2-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="13af2-111">Requirements</span></span>



| <span data-ttu-id="13af2-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="13af2-112">Requirement</span></span> | <span data-ttu-id="13af2-113">Wert</span><span class="sxs-lookup"><span data-stu-id="13af2-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13af2-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="13af2-114">Minimum supported client</span></span><br/> | <span data-ttu-id="13af2-115">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="13af2-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="13af2-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="13af2-116">Minimum supported server</span></span><br/> | <span data-ttu-id="13af2-117">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="13af2-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="13af2-118">Header</span><span class="sxs-lookup"><span data-stu-id="13af2-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="13af2-119"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="13af2-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13af2-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13af2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13af2-121">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="13af2-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




