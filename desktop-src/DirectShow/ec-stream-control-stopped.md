---
description: Ein Befehl zum Abbrechen der Stream-Steuerung wurde wirksam.
ms.assetid: a2f7a959-fafd-47ff-9b3d-1a898fdb1f81
title: EC_STREAM_CONTROL_STOPPED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8c5488ba400d90623955c3e9adcba0dde07e04a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356430"
---
# <a name="ec_stream_control_stopped"></a><span data-ttu-id="c8d17-103">EC- \_ Stream- \_ Steuerelement \_ beendet</span><span class="sxs-lookup"><span data-stu-id="c8d17-103">EC\_STREAM\_CONTROL\_STOPPED</span></span>

<span data-ttu-id="c8d17-104">Ein Befehl zum Abbrechen der Stream-Steuerung wurde wirksam.</span><span class="sxs-lookup"><span data-stu-id="c8d17-104">A stream-control stop command has taken effect.</span></span>

## <a name="parameters"></a><span data-ttu-id="c8d17-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8d17-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8d17-106"><span id="pSender"></span><span id="psender"></span><span id="PSENDER"></span>*psender*</span><span class="sxs-lookup"><span data-stu-id="c8d17-106"><span id="pSender"></span><span id="psender"></span><span id="PSENDER"></span>*pSender*</span></span>
</dt> <dd>

<span data-ttu-id="c8d17-107">(**IUnknown** \* ) Ein Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der PIN, die den Stream beendet hat.</span><span class="sxs-lookup"><span data-stu-id="c8d17-107">(**IUnknown**\*) Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the pin that stopped the stream.</span></span>

</dd> <dt>

<span data-ttu-id="c8d17-108"><span id="dwCookie"></span><span id="dwcookie"></span><span id="DWCOOKIE"></span>*dwCookie*</span><span class="sxs-lookup"><span data-stu-id="c8d17-108"><span id="dwCookie"></span><span id="dwcookie"></span><span id="DWCOOKIE"></span>*dwCookie*</span></span>
</dt> <dd>

<span data-ttu-id="c8d17-109">(**DWORD**) Benutzerdefinierter Wert.</span><span class="sxs-lookup"><span data-stu-id="c8d17-109">(**DWORD**) User-defined value.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="c8d17-110">Standardaktion</span><span class="sxs-lookup"><span data-stu-id="c8d17-110">Default Action</span></span>

<span data-ttu-id="c8d17-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="c8d17-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8d17-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c8d17-112">Remarks</span></span>

<span data-ttu-id="c8d17-113">Filter Senden dieses Ereignis als Antwort auf die [**iamstreamcontrol:: STOPAT**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) -Methode.</span><span class="sxs-lookup"><span data-stu-id="c8d17-113">Filters send this event in response to the [**IAMStreamControl::StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) method.</span></span> <span data-ttu-id="c8d17-114">Die **STOPAT** -Methode gibt eine Bezugszeit für eine PIN zum Beenden des Streamings an.</span><span class="sxs-lookup"><span data-stu-id="c8d17-114">The **StopAt** method specifies a reference time for a pin to stop streaming.</span></span> <span data-ttu-id="c8d17-115">Wenn das Streaming angehalten wird, sendet der Filter dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="c8d17-115">When streaming does halt, the filter sends this event.</span></span>

<span data-ttu-id="c8d17-116">Der *psender* -Parameter gibt die PIN an, mit der der Befehl zum Abbrechen ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c8d17-116">The *pSender* parameter specifies the pin that executes the stop command.</span></span> <span data-ttu-id="c8d17-117">Abhängig von der Implementierung ist es möglicherweise nicht die PIN, die den [**Stop at**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) -Befehl empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="c8d17-117">Depending on the implementation, it might not be the pin that received the [**StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) call.</span></span>

<span data-ttu-id="c8d17-118">Der *dwCookie* -Parameter wird von der Anwendung in der [**STOPAT**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) -Methode angegeben.</span><span class="sxs-lookup"><span data-stu-id="c8d17-118">The *dwCookie* parameter is specified by the application in the [**StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) method.</span></span> <span data-ttu-id="c8d17-119">Dieser Parameter ermöglicht der Anwendung die Nachverfolgung mehrerer Aufrufe der-Methode.</span><span class="sxs-lookup"><span data-stu-id="c8d17-119">This parameter enables the application to track multiple calls to the method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8d17-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c8d17-120">Requirements</span></span>



| <span data-ttu-id="c8d17-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c8d17-121">Requirement</span></span> | <span data-ttu-id="c8d17-122">Wert</span><span class="sxs-lookup"><span data-stu-id="c8d17-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c8d17-123">Header</span><span class="sxs-lookup"><span data-stu-id="c8d17-123">Header</span></span><br/> | <dl> <span data-ttu-id="c8d17-124"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8d17-124"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8d17-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c8d17-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8d17-126">Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="c8d17-126">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="c8d17-127">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="c8d17-127">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




