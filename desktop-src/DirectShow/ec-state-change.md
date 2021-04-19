---
description: Der Zustand des Filter Diagramms wurde geändert.
ms.assetid: f77b4c06-46a5-4912-adb0-0fa8cb7769aa
title: EC_STATE_CHANGE (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf64cc62ba15f77370e52821c3335f9a22f573d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360412"
---
# <a name="ec_state_change"></a><span data-ttu-id="14460-103">Änderung des EC- \_ Zustands \_</span><span class="sxs-lookup"><span data-stu-id="14460-103">EC\_STATE\_CHANGE</span></span>

<span data-ttu-id="14460-104">Der Zustand des Filter Diagramms wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="14460-104">The filter graph has changed state.</span></span>

## <a name="parameters"></a><span data-ttu-id="14460-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="14460-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14460-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="14460-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="14460-107">(**DWORD**) Member des Enumerationstyps des [**Filter \_ Zustands**](/windows/win32/api/strmif/ne-strmif-filter_state) , der den neuen Diagramm Zustand angibt.</span><span class="sxs-lookup"><span data-stu-id="14460-107">(**DWORD**) Member of the [**FILTER\_STATE**](/windows/win32/api/strmif/ne-strmif-filter_state) enumerated type, indicating the new graph state.</span></span>

</dd> <dt>

<span data-ttu-id="14460-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="14460-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="14460-109">Keinen.</span><span class="sxs-lookup"><span data-stu-id="14460-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="14460-110">Standardaktion</span><span class="sxs-lookup"><span data-stu-id="14460-110">Default Action</span></span>

<span data-ttu-id="14460-111">Keine Standardaktion.</span><span class="sxs-lookup"><span data-stu-id="14460-111">No default action.</span></span> <span data-ttu-id="14460-112">Das Ereignis wird nicht an die Anwendung gesendet.</span><span class="sxs-lookup"><span data-stu-id="14460-112">The event is not sent to the application.</span></span>

> [!Note]  
> <span data-ttu-id="14460-113">Dieses Ereignis kann auftreten, wenn das Diagramm heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="14460-113">This event can occur when the graph shuts down.</span></span> <span data-ttu-id="14460-114">Wenn Sie die Standardaktion überschreiben und auf dieses Ereignis lauschen, müssen Sie besonders darauf achten, dass Ereignisse nach der Freigabe des Filter-Graph-Managers nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="14460-114">If you override the default action and listen for this event, you must be especially careful not to process events after releasing the Filter Graph Manager.</span></span> <span data-ttu-id="14460-115">Andernfalls verweist die Anwendung möglicherweise auf einen ungültigen [**imediaevent**](/windows/desktop/api/Control/nn-control-imediaevent) -Zeiger und stürzt ab.</span><span class="sxs-lookup"><span data-stu-id="14460-115">Otherwise, your application might reference an invalid [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) pointer and crash.</span></span> <span data-ttu-id="14460-116">Weitere Informationen finden Sie unter [reagieren auf Ereignisse](responding-to-events.md).</span><span class="sxs-lookup"><span data-stu-id="14460-116">For more information, see [Responding to Events](responding-to-events.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="14460-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="14460-117">Requirements</span></span>



| <span data-ttu-id="14460-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="14460-118">Requirement</span></span> | <span data-ttu-id="14460-119">Wert</span><span class="sxs-lookup"><span data-stu-id="14460-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="14460-120">Header</span><span class="sxs-lookup"><span data-stu-id="14460-120">Header</span></span><br/> | <dl> <span data-ttu-id="14460-121"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="14460-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14460-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="14460-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14460-123">Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="14460-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="14460-124">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="14460-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




