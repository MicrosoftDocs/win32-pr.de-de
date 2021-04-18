---
description: Benutzerdefinierter Ereignistyp.
ms.assetid: a54a446c-0e96-467b-90f6-0f64a7c1727d
title: Meextendedtype-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d5551110fc3637a40834a7bf9251826f151ec62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343783"
---
# <a name="meextendedtype-event"></a><span data-ttu-id="e0e52-103">Meextendedtype-Ereignis</span><span class="sxs-lookup"><span data-stu-id="e0e52-103">MEExtendedType event</span></span>

<span data-ttu-id="e0e52-104">Benutzerdefinierter Ereignistyp.</span><span class="sxs-lookup"><span data-stu-id="e0e52-104">Custom event type.</span></span> <span data-ttu-id="e0e52-105">Sie können diesen Ereignistyp verwenden, um benutzerdefinierte Ereignisse für die Komponente zu definieren.</span><span class="sxs-lookup"><span data-stu-id="e0e52-105">You can use this event type to define custom events for your component.</span></span> <span data-ttu-id="e0e52-106">Verwenden Sie den erweiterten Ereignistyp, um das Ereignis zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="e0e52-106">Use the extended event type to identify the event.</span></span> <span data-ttu-id="e0e52-107">Der Typ des erweiterten Ereignisses ist ein GUID-Wert, der dem Ereignis zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e0e52-107">The extended event type is a GUID value associated with the event.</span></span> <span data-ttu-id="e0e52-108">Weitere Informationen finden Sie unter [**IMF Media Event:: getextendedtype**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype).</span><span class="sxs-lookup"><span data-stu-id="e0e52-108">For more information, see [**IMFMediaEvent::GetExtendedType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype).</span></span>

## <a name="event-values"></a><span data-ttu-id="e0e52-109">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="e0e52-109">Event values</span></span>

<span data-ttu-id="e0e52-110">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="e0e52-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="e0e52-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="e0e52-111">VARTYPE</span></span>              | <span data-ttu-id="e0e52-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e0e52-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="e0e52-113">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="e0e52-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="e0e52-114">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="e0e52-114">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="e0e52-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e0e52-115">Requirements</span></span>



| <span data-ttu-id="e0e52-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e0e52-116">Requirement</span></span> | <span data-ttu-id="e0e52-117">Wert</span><span class="sxs-lookup"><span data-stu-id="e0e52-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0e52-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e0e52-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e0e52-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e0e52-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e0e52-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e0e52-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e0e52-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e0e52-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e0e52-122">Header</span><span class="sxs-lookup"><span data-stu-id="e0e52-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0e52-123"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e0e52-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0e52-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0e52-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0e52-125">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e0e52-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




