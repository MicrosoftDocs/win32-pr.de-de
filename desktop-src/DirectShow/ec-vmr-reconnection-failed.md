---
description: Wird von VMR-7 und VMR-9 gesendet, wenn es nicht möglich war, ein dynamisches Format Change Request aus dem upstreamdecoder zu akzeptieren.
ms.assetid: 0c865853-2484-4833-9c92-3d6452b655f1
title: EC_VMR_RECONNECTION_FAILED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d29703d5ede068710966119f16c44a9e3637249
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366703"
---
# <a name="ec_vmr_reconnection_failed"></a><span data-ttu-id="b7b2a-103">Fehler beim \_ \_ erneuten Herstellen der Verbindung mit EC VMR \_</span><span class="sxs-lookup"><span data-stu-id="b7b2a-103">EC\_VMR\_RECONNECTION\_FAILED</span></span>

<span data-ttu-id="b7b2a-104">Wird von VMR-7 und VMR-9 gesendet, wenn es nicht möglich war, ein dynamisches Format Change Request aus dem upstreamdecoder zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-104">Sent by the VMR-7 and the VMR-9 when it was unable to accept a dynamic format change request from the upstream decoder.</span></span>

## <a name="parameters"></a><span data-ttu-id="b7b2a-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7b2a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7b2a-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="b7b2a-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="b7b2a-107">(**HRESULT**) Der von [**IPin:: receiveconnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) in der eingabepin von VMR zurückgegebene Status Code, bei dem die erneute Verbindung nicht hergestellt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-107">(**HRESULT**) Status code returned from [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) on the VMR's input pin that failed the reconnection.</span></span>

</dd> <dt>

<span data-ttu-id="b7b2a-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="b7b2a-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="b7b2a-109">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-109">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b7b2a-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b7b2a-110">Remarks</span></span>

<span data-ttu-id="b7b2a-111">Dieses Ereignis wird an Anwendungen weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-111">This event is forwarded to applications.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7b2a-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b7b2a-112">Requirements</span></span>



| <span data-ttu-id="b7b2a-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b7b2a-113">Requirement</span></span> | <span data-ttu-id="b7b2a-114">Wert</span><span class="sxs-lookup"><span data-stu-id="b7b2a-114">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b7b2a-115">Header</span><span class="sxs-lookup"><span data-stu-id="b7b2a-115">Header</span></span><br/> | <dl> <span data-ttu-id="b7b2a-116"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7b2a-116"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7b2a-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b7b2a-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7b2a-118">Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="b7b2a-118">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="b7b2a-119">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="b7b2a-119">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




