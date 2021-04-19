---
description: Der Startbefehl für die Stream-Steuerung wurde wirksam.
ms.assetid: e2f8d9a2-c96c-457c-8a88-7c86d4405928
title: EC_STREAM_CONTROL_STARTED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 984562fde9001de14067e5865d5583636b264852
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365982"
---
# <a name="ec_stream_control_started"></a><span data-ttu-id="b2f3d-103">EC- \_ Stream- \_ Steuerelement \_</span><span class="sxs-lookup"><span data-stu-id="b2f3d-103">EC\_STREAM\_CONTROL\_STARTED</span></span>

<span data-ttu-id="b2f3d-104">Der Startbefehl für die Stream-Steuerung wurde wirksam.</span><span class="sxs-lookup"><span data-stu-id="b2f3d-104">A stream-control start command has taken effect.</span></span>

## <a name="parameters"></a><span data-ttu-id="b2f3d-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2f3d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2f3d-106"><span id="pSender"></span><span id="psender"></span><span id="PSENDER"></span>*psender*</span><span class="sxs-lookup"><span data-stu-id="b2f3d-106"><span id="pSender"></span><span id="psender"></span><span id="PSENDER"></span>*pSender*</span></span>
</dt> <dd>

<span data-ttu-id="b2f3d-107">(**IUnknown** \* ) Ein Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der PIN, die den Stream gestartet hat.</span><span class="sxs-lookup"><span data-stu-id="b2f3d-107">(**IUnknown**\*) Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the pin that started the stream.</span></span>

</dd> <dt>

<span data-ttu-id="b2f3d-108"><span id="dwCookie"></span><span id="dwcookie"></span><span id="DWCOOKIE"></span>*dwCookie*</span><span class="sxs-lookup"><span data-stu-id="b2f3d-108"><span id="dwCookie"></span><span id="dwcookie"></span><span id="DWCOOKIE"></span>*dwCookie*</span></span>
</dt> <dd>

<span data-ttu-id="b2f3d-109">(**DWORD**) Benutzerdefinierter Wert.</span><span class="sxs-lookup"><span data-stu-id="b2f3d-109">(**DWORD**) User-defined value.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="b2f3d-110">Standardaktion</span><span class="sxs-lookup"><span data-stu-id="b2f3d-110">Default Action</span></span>

<span data-ttu-id="b2f3d-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="b2f3d-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2f3d-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b2f3d-112">Remarks</span></span>

<span data-ttu-id="b2f3d-113">Filter Senden dieses Ereignis als Antwort auf die [**iamstreamcontrol:: startat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) -Methode.</span><span class="sxs-lookup"><span data-stu-id="b2f3d-113">Filters send this event in response to the [**IAMStreamControl::StartAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) method.</span></span> <span data-ttu-id="b2f3d-114">Diese Methode gibt eine Bezugszeit für eine PIN an, um mit dem Streaming zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="b2f3d-114">This method specifies a reference time for a pin to begin streaming.</span></span> <span data-ttu-id="b2f3d-115">Wenn das Streaming beginnt, sendet der Filter dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="b2f3d-115">When streaming does begin, the filter sends this event.</span></span>

<span data-ttu-id="b2f3d-116">Der *psender* -Parameter gibt die PIN an, die den Startbefehl ausführt.</span><span class="sxs-lookup"><span data-stu-id="b2f3d-116">The *pSender* parameter specifies the pin that executes the start command.</span></span> <span data-ttu-id="b2f3d-117">Abhängig von der Implementierung ist es möglicherweise nicht die PIN, die den [**startat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) -Befehl empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="b2f3d-117">Depending on the implementation, it might not be the pin that received the [**StartAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) call.</span></span>

<span data-ttu-id="b2f3d-118">Der *dwCookie* -Parameter wird von der Anwendung in der [**startat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) -Methode angegeben.</span><span class="sxs-lookup"><span data-stu-id="b2f3d-118">The *dwCookie* parameter is specified by the application in the [**StartAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) method.</span></span> <span data-ttu-id="b2f3d-119">Dieser Parameter ermöglicht der Anwendung die Nachverfolgung mehrerer Aufrufe der-Methode.</span><span class="sxs-lookup"><span data-stu-id="b2f3d-119">This parameter enables the application to track multiple calls to the method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2f3d-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b2f3d-120">Requirements</span></span>



| <span data-ttu-id="b2f3d-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b2f3d-121">Requirement</span></span> | <span data-ttu-id="b2f3d-122">Wert</span><span class="sxs-lookup"><span data-stu-id="b2f3d-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b2f3d-123">Header</span><span class="sxs-lookup"><span data-stu-id="b2f3d-123">Header</span></span><br/> | <dl> <span data-ttu-id="b2f3d-124"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2f3d-124"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2f3d-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b2f3d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2f3d-126">Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="b2f3d-126">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="b2f3d-127">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="b2f3d-127">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




