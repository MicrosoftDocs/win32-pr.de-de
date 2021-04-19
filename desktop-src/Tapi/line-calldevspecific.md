---
description: Die TSPI-zeilige \_ calldevspecific-Nachricht wird an die LineEvent-Rückruffunktion gesendet, um TAPI über gerätespezifische Ereignisse zu benachrichtigen, die bei einem Aufruf auftreten.
ms.assetid: accd753a-3be0-4c7d-bbc7-d294d1381144
title: LINE_CALLDEVSPECIFIC Meldung (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a48bf8a54a1f326fe7bb27c82349e5575c8bbf6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354169"
---
# <a name="line_calldevspecific-message"></a><span data-ttu-id="97f74-103">Zeile \_ calldevspecific Message</span><span class="sxs-lookup"><span data-stu-id="97f74-103">LINE\_CALLDEVSPECIFIC message</span></span>

<span data-ttu-id="97f74-104">Die TSPI- **zeilige \_ calldevspecific** -Nachricht wird an die [**LineEvent**](/windows/win32/api/tspi/nc-tspi-lineevent) -Rückruffunktion gesendet, um TAPI über gerätespezifische Ereignisse zu benachrichtigen, die bei einem Aufruf auftreten.</span><span class="sxs-lookup"><span data-stu-id="97f74-104">The TSPI **LINE\_CALLDEVSPECIFIC** message is sent to the [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) callback function to notify TAPI about device-specific events occurring on a call.</span></span> <span data-ttu-id="97f74-105">Die Bedeutung der Nachricht und die Interpretation der Parameter *dwParam1* through *dwParam3* sind gerätespezifisch.</span><span class="sxs-lookup"><span data-stu-id="97f74-105">The meaning of the message and the interpretation of the *dwParam1* through *dwParam3* parameters is device specific.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="97f74-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="97f74-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97f74-107">*htline*</span><span class="sxs-lookup"><span data-stu-id="97f74-107">*htLine*</span></span> 
</dt> <dd>

<span data-ttu-id="97f74-108">Das nicht transparente TAPI-Objekt Handle für das liniengerät.</span><span class="sxs-lookup"><span data-stu-id="97f74-108">The TAPI opaque object handle to the line device.</span></span>

</dd> <dt>

<span data-ttu-id="97f74-109">*"htcall"*</span><span class="sxs-lookup"><span data-stu-id="97f74-109">*htCall*</span></span> 
</dt> <dd>

<span data-ttu-id="97f74-110">Das nicht transparente TAPI-Objekt Handle für das anrufgerät.</span><span class="sxs-lookup"><span data-stu-id="97f74-110">The TAPI opaque object handle to the call device.</span></span>

</dd> <dt>

<span data-ttu-id="97f74-111">*dwmsg*</span><span class="sxs-lookup"><span data-stu-id="97f74-111">*dwMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="97f74-112">Die Wert Zeile \_ calldevspecific.</span><span class="sxs-lookup"><span data-stu-id="97f74-112">The value LINE\_CALLDEVSPECIFIC.</span></span>

</dd> <dt>

<span data-ttu-id="97f74-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="97f74-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="97f74-114">Gerätespezifisch.</span><span class="sxs-lookup"><span data-stu-id="97f74-114">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="97f74-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="97f74-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="97f74-116">Gerätespezifisch.</span><span class="sxs-lookup"><span data-stu-id="97f74-116">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="97f74-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="97f74-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="97f74-118">Gerätespezifisch.</span><span class="sxs-lookup"><span data-stu-id="97f74-118">Device specific.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="97f74-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="97f74-119">Remarks</span></span>

<span data-ttu-id="97f74-120">Die **line \_ calldevspecific** -Nachricht wird von einem Dienstanbieter in Verbindung mit der [**TSPI \_ linedevspecific**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific) -Funktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="97f74-120">The **LINE\_CALLDEVSPECIFIC** message is used by a service provider in conjunction with the [**TSPI\_lineDevSpecific**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific) function.</span></span> <span data-ttu-id="97f74-121">Seine Bedeutung ist gerätespezifisch.</span><span class="sxs-lookup"><span data-stu-id="97f74-121">Its meaning is device specific.</span></span>

<span data-ttu-id="97f74-122">TAPI sendet die [**\_ DevSpecific-Zeilen**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85)) Nachricht als Antwort auf den Empfang dieser Nachricht von einem Dienstanbieter an Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="97f74-122">TAPI sends the [**LINE\_DEVSPECIFIC**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85)) message to applications in response to receiving this message from a service provider.</span></span> <span data-ttu-id="97f74-123">Die Parameter " *htline* " und " *htcall"* werden als *hdevice* -Parameter auf der TAPI-Ebene in den entsprechenden *hcallcenter* übersetzt.</span><span class="sxs-lookup"><span data-stu-id="97f74-123">The *htLine* and *htCall* parameters are translated to the appropriate *hCall* as the *hDevice* parameter at the TAPI level.</span></span> <span data-ttu-id="97f74-124">Die Parameter *dwParam1*, *dwParam2* und *dwParam3* werden unverändert übermittelt.</span><span class="sxs-lookup"><span data-stu-id="97f74-124">The *dwParam1*, *dwParam2*, and *dwParam3* parameters are passed through unmodified.</span></span>

<span data-ttu-id="97f74-125">Es gibt keine direkt entsprechende Meldung auf der TAPI-Ebene, obwohl diese Meldung sehr ähnlich ist wie " [**line \_ DevSpecific**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85))".</span><span class="sxs-lookup"><span data-stu-id="97f74-125">There is no directly corresponding message at the TAPI level, although this message is very similar to [**LINE\_DEVSPECIFIC**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85)).</span></span> <span data-ttu-id="97f74-126">Auf der TSPI-Ebene werden die gerätespezifischen Nachrichten zwischen den Berichterstattungs Ereignissen in Zeilen und Adressen und den Bericht Erstellungs Ereignissen bei Aufrufen aufgeteilt.</span><span class="sxs-lookup"><span data-stu-id="97f74-126">At the TSPI level, the device-specific messages are split between those reporting events on lines and addresses, and those reporting events on calls.</span></span>

## <a name="requirements"></a><span data-ttu-id="97f74-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="97f74-127">Requirements</span></span>



| <span data-ttu-id="97f74-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="97f74-128">Requirement</span></span> | <span data-ttu-id="97f74-129">Wert</span><span class="sxs-lookup"><span data-stu-id="97f74-129">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="97f74-130">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="97f74-130">TAPI version</span></span><br/> | <span data-ttu-id="97f74-131">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="97f74-131">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="97f74-132">Header</span><span class="sxs-lookup"><span data-stu-id="97f74-132">Header</span></span><br/>       | <dl> <span data-ttu-id="97f74-133"><dt>TSPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="97f74-133"><dt>Tspi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97f74-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97f74-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="97f74-135">[**Linien- \_ DevSpecific**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="97f74-135">[**LINE\_DEVSPECIFIC**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="97f74-136">**LineEvent**</span><span class="sxs-lookup"><span data-stu-id="97f74-136">**LINEEVENT**</span></span>](/windows/win32/api/tspi/nc-tspi-lineevent)
</dt> <dt>

[<span data-ttu-id="97f74-137">**TSPI \_ linedevspecific**</span><span class="sxs-lookup"><span data-stu-id="97f74-137">**TSPI\_lineDevSpecific**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific)
</dt> </dl>

 

