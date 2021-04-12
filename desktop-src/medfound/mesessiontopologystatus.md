---
description: Wird von der Medien Sitzung ausgelöst, wenn sich der Status einer Topologie ändert.
ms.assetid: b45fd598-ab1e-4b12-8d82-c88c96d1f770
title: Mesessiontopologystatus-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11948e27997037c1e875e192fd712a2f8a132b44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959301"
---
# <a name="mesessiontopologystatus-event"></a><span data-ttu-id="9e9bb-103">Mesessiontopologystatus-Ereignis</span><span class="sxs-lookup"><span data-stu-id="9e9bb-103">MESessionTopologyStatus event</span></span>

<span data-ttu-id="9e9bb-104">Wird von der Medien Sitzung ausgelöst, wenn sich der Status einer Topologie ändert.</span><span class="sxs-lookup"><span data-stu-id="9e9bb-104">Raised by the Media Session when the status of a topology changes.</span></span>

## <a name="event-values"></a><span data-ttu-id="9e9bb-105">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="9e9bb-105">Event values</span></span>

<span data-ttu-id="9e9bb-106">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="9e9bb-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="9e9bb-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="9e9bb-107">VARTYPE</span></span>                | <span data-ttu-id="9e9bb-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9e9bb-108">Description</span></span>                                                                                         |
|------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e9bb-109">VT \_ unbekannt</span><span class="sxs-lookup"><span data-stu-id="9e9bb-109">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="9e9bb-110">Ein Zeiger auf die [**imftopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) -Schnittstelle der Topologie.</span><span class="sxs-lookup"><span data-stu-id="9e9bb-110">Pointer to the [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) interface of the topology.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="9e9bb-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="9e9bb-111">Attributes</span></span>

<span data-ttu-id="9e9bb-112">Für dieses Ereignis sind die folgenden Attribute definiert:</span><span class="sxs-lookup"><span data-stu-id="9e9bb-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="9e9bb-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="9e9bb-113">Attribute</span></span>                                                                            | <span data-ttu-id="9e9bb-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9e9bb-114">Description</span></span>                                                      |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="9e9bb-115">**Status der MF- \_ Ereignis \_ Topologie \_**</span><span class="sxs-lookup"><span data-stu-id="9e9bb-115">**MF\_EVENT\_TOPOLOGY\_STATUS**</span></span>](mf-event-topology-status-attribute.md)<br/> | <span data-ttu-id="9e9bb-116">Gibt den neuen Status der Topologie an.</span><span class="sxs-lookup"><span data-stu-id="9e9bb-116">Specifies the new status of the topology.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="9e9bb-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9e9bb-117">Remarks</span></span>

<span data-ttu-id="9e9bb-118">Ein Codebeispiel, in dem der [**imftopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) -Zeiger aus dem-Ereignis abgerufen wird, finden Sie unter [mesessiontopologyset](mesessiontopologyset.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="9e9bb-118">For a code example that retrieves the [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) pointer from the event, see [MESessionTopologySet](mesessiontopologyset.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e9bb-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9e9bb-119">Requirements</span></span>



| <span data-ttu-id="9e9bb-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9e9bb-120">Requirement</span></span> | <span data-ttu-id="9e9bb-121">Wert</span><span class="sxs-lookup"><span data-stu-id="9e9bb-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e9bb-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9e9bb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9e9bb-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9e9bb-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9e9bb-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9e9bb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9e9bb-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9e9bb-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9e9bb-126">Header</span><span class="sxs-lookup"><span data-stu-id="9e9bb-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e9bb-127"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9e9bb-127"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e9bb-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9e9bb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e9bb-129">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9e9bb-129">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




