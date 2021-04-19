---
description: Ein Filter empfängt nicht genügend Daten.
ms.assetid: c9cdfe46-02bb-4ea9-ac58-7d63e03c26d8
title: EC_STARVATION (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 988d550b93ecb9a3c2f78f2d07f50a3965be945d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371981"
---
# <a name="ec_starvation"></a><span data-ttu-id="88fdb-103">EC- \_ Hunger</span><span class="sxs-lookup"><span data-stu-id="88fdb-103">EC\_STARVATION</span></span>

<span data-ttu-id="88fdb-104">Ein Filter empfängt nicht genügend Daten.</span><span class="sxs-lookup"><span data-stu-id="88fdb-104">A filter is not receiving enough data.</span></span>

## <a name="parameters"></a><span data-ttu-id="88fdb-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="88fdb-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88fdb-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="88fdb-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="88fdb-107">Keinen.</span><span class="sxs-lookup"><span data-stu-id="88fdb-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="88fdb-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="88fdb-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="88fdb-109">Keinen.</span><span class="sxs-lookup"><span data-stu-id="88fdb-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="88fdb-110">Standardaktion</span><span class="sxs-lookup"><span data-stu-id="88fdb-110">Default Action</span></span>

<span data-ttu-id="88fdb-111">Das Ereignis wird nicht an die Anwendung gesendet.</span><span class="sxs-lookup"><span data-stu-id="88fdb-111">The event is not sent to the application.</span></span> <span data-ttu-id="88fdb-112">Wenn das Filter Diagramm ausgeführt wird, hält der Filter Diagramm-Manager das Diagramm an und wartet auf den Abschluss der Pause.</span><span class="sxs-lookup"><span data-stu-id="88fdb-112">If the filter graph is running, the filter graph manager pauses the graph and waits for the pause to complete.</span></span> <span data-ttu-id="88fdb-113">Anschließend wird das Diagramm erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="88fdb-113">Then it runs the graph again.</span></span> <span data-ttu-id="88fdb-114">Der Filter, der das Ereignis sendet, sollte seinen Übergang nicht beenden, um angehalten zu werden, bis genügend Daten zum Fortsetzen bereit stehen.</span><span class="sxs-lookup"><span data-stu-id="88fdb-114">The filter sending the event should not complete its transition to paused until it has enough data to resume.</span></span> <span data-ttu-id="88fdb-115">Wenn das Filter Diagramm nicht ausgeführt wird, ignoriert der Filter Graph-Manager dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="88fdb-115">If the filter graph is not running, the filter graph manager ignores this event.</span></span>

## <a name="remarks"></a><span data-ttu-id="88fdb-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="88fdb-116">Remarks</span></span>

<span data-ttu-id="88fdb-117">Wenn zu wenig Daten eintreffen, kann ein Parser oder Quell Filter dieses Ereignis senden.</span><span class="sxs-lookup"><span data-stu-id="88fdb-117">A parser or source filter can send this event if too little data is arriving.</span></span>

## <a name="requirements"></a><span data-ttu-id="88fdb-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="88fdb-118">Requirements</span></span>



| <span data-ttu-id="88fdb-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="88fdb-119">Requirement</span></span> | <span data-ttu-id="88fdb-120">Wert</span><span class="sxs-lookup"><span data-stu-id="88fdb-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="88fdb-121">Header</span><span class="sxs-lookup"><span data-stu-id="88fdb-121">Header</span></span><br/> | <dl> <span data-ttu-id="88fdb-122"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="88fdb-122"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88fdb-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88fdb-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88fdb-124">Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="88fdb-124">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="88fdb-125">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="88fdb-125">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




