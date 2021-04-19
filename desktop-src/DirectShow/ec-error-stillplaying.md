---
description: Ein asynchroner Befehl zum Ausführen des Diagramms ist fehlgeschlagen.
ms.assetid: 0bfcf4b4-b35a-4593-9956-8e1e8c9139cb
title: EC_ERROR_STILLPLAYING (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d1c99db8c6b332ad4531f04171d960c5cfa9824
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356346"
---
# <a name="ec_error_stillplaying"></a><span data-ttu-id="5866c-103">EC- \_ Fehler \_ beim Stillen</span><span class="sxs-lookup"><span data-stu-id="5866c-103">EC\_ERROR\_STILLPLAYING</span></span>

<span data-ttu-id="5866c-104">Ein asynchroner Befehl zum Ausführen des Diagramms ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="5866c-104">An asynchronous command to run the graph has failed.</span></span>

## <a name="parameters"></a><span data-ttu-id="5866c-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="5866c-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5866c-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="5866c-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="5866c-107">(**HRESULT**) Fehlercode des Vorgangs, bei dem ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="5866c-107">(**HRESULT**) Failure code of the operation that failed.</span></span>

</dd> <dt>

<span data-ttu-id="5866c-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="5866c-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="5866c-109">Keinen.</span><span class="sxs-lookup"><span data-stu-id="5866c-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="5866c-110">Standardaktion</span><span class="sxs-lookup"><span data-stu-id="5866c-110">Default Action</span></span>

<span data-ttu-id="5866c-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="5866c-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="5866c-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5866c-112">Remarks</span></span>

<span data-ttu-id="5866c-113">Wenn der Filter Graph-Manager einen asynchronen Run-Befehl ausgibt, der fehlschlägt, sendet er dieses Ereignis an die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="5866c-113">If the filter graph manager issues an asynchronous run command that fails, it sends this event to the application.</span></span> <span data-ttu-id="5866c-114">Das Diagramm verbleibt im Status "wird ausgeführt".</span><span class="sxs-lookup"><span data-stu-id="5866c-114">The graph remains in a running state.</span></span> <span data-ttu-id="5866c-115">Der Status der zugrunde liegenden Filter ist unbestimmt.</span><span class="sxs-lookup"><span data-stu-id="5866c-115">The state of the underlying filters is indeterminate.</span></span> <span data-ttu-id="5866c-116">Möglicherweise werden einige Filter ausgeführt, andere hingegen nicht.</span><span class="sxs-lookup"><span data-stu-id="5866c-116">Some filters might be running, others might not.</span></span>

## <a name="requirements"></a><span data-ttu-id="5866c-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5866c-117">Requirements</span></span>



| <span data-ttu-id="5866c-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5866c-118">Requirement</span></span> | <span data-ttu-id="5866c-119">Wert</span><span class="sxs-lookup"><span data-stu-id="5866c-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5866c-120">Header</span><span class="sxs-lookup"><span data-stu-id="5866c-120">Header</span></span><br/> | <dl> <span data-ttu-id="5866c-121"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="5866c-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5866c-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5866c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5866c-123">Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="5866c-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="5866c-124">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="5866c-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




