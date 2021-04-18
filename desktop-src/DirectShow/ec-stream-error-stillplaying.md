---
description: In einem Stream ist ein Fehler aufgetreten, aber der Stream wird immer noch abgespielt.
ms.assetid: ff155c01-22ba-46dd-85b8-05eabf956908
title: EC_STREAM_ERROR_STILLPLAYING (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5db74a9f16a0ca01ce74e6d94df50cc402221aaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364913"
---
# <a name="ec_stream_error_stillplaying"></a><span data-ttu-id="cfd33-103">\_ \_ Fehler \_ beim Wiedergeben des EC-Stream</span><span class="sxs-lookup"><span data-stu-id="cfd33-103">EC\_STREAM\_ERROR\_STILLPLAYING</span></span>

<span data-ttu-id="cfd33-104">In einem Stream ist ein Fehler aufgetreten, aber der Stream wird immer noch abgespielt.</span><span class="sxs-lookup"><span data-stu-id="cfd33-104">An error occurred in a stream, but the stream is still playing.</span></span>

## <a name="parameters"></a><span data-ttu-id="cfd33-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="cfd33-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfd33-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="cfd33-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="cfd33-107">(**HRESULT**) Fehlercode des Vorgangs, bei dem ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="cfd33-107">(**HRESULT**) Failure code of the operation that failed.</span></span>

</dd> <dt>

<span data-ttu-id="cfd33-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="cfd33-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="cfd33-109">(**DWORD**) Kleinerer Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="cfd33-109">(**DWORD**) Minor error code.</span></span> <span data-ttu-id="cfd33-110">Dieser Wert ist normalerweise 0 (null).</span><span class="sxs-lookup"><span data-stu-id="cfd33-110">This value is usually zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="cfd33-111">Standardaktion</span><span class="sxs-lookup"><span data-stu-id="cfd33-111">Default Action</span></span>

<span data-ttu-id="cfd33-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="cfd33-112">None.</span></span> <span data-ttu-id="cfd33-113">Die Anwendung muss entscheiden, ob das Diagramm angehalten werden soll.</span><span class="sxs-lookup"><span data-stu-id="cfd33-113">The application must decide whether to stop the graph.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfd33-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cfd33-114">Requirements</span></span>



| <span data-ttu-id="cfd33-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cfd33-115">Requirement</span></span> | <span data-ttu-id="cfd33-116">Wert</span><span class="sxs-lookup"><span data-stu-id="cfd33-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cfd33-117">Header</span><span class="sxs-lookup"><span data-stu-id="cfd33-117">Header</span></span><br/> | <dl> <span data-ttu-id="cfd33-118"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfd33-118"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfd33-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cfd33-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfd33-120">Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="cfd33-120">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="cfd33-121">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="cfd33-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




