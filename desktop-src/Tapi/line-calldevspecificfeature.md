---
description: Die TSPI-zeilige \_ calldevspecificfeature-Nachricht wird an die LineEvent-Rückruffunktion gesendet, um TAPI über gerätespezifische Ereignisse zu benachrichtigen, die in einer Zeile oder einer Adresse auftreten.
ms.assetid: bf470f5b-f7e5-4f98-9b60-12da599ebf26
title: LINE_CALLDEVSPECIFICFEATURE Meldung (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2891f019035f53be4dbc0a40de429e5c0d9dc567
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359770"
---
# <a name="line_calldevspecificfeature-message"></a><span data-ttu-id="84a0e-103">Zeile \_ calldevspecificfeature-Meldung</span><span class="sxs-lookup"><span data-stu-id="84a0e-103">LINE\_CALLDEVSPECIFICFEATURE message</span></span>

<span data-ttu-id="84a0e-104">Die TSPI- **zeilige \_ calldevspecificfeature** -Nachricht wird an die [**LineEvent**](/windows/win32/api/tspi/nc-tspi-lineevent) -Rückruffunktion gesendet, um TAPI über gerätespezifische Ereignisse zu benachrichtigen, die in einer Zeile oder einer Adresse auftreten.</span><span class="sxs-lookup"><span data-stu-id="84a0e-104">The TSPI **LINE\_CALLDEVSPECIFICFEATURE** message is sent to the [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) callback function to notify TAPI about device-specific events occurring on a line or address.</span></span> <span data-ttu-id="84a0e-105">Die Bedeutung der Nachricht und die Interpretation der Parameter *dwParam1* through *dwParam3* sind gerätespezifisch.</span><span class="sxs-lookup"><span data-stu-id="84a0e-105">The meaning of the message and the interpretation of the *dwParam1* through *dwParam3* parameters is device specific.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="84a0e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="84a0e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84a0e-107">*htline*</span><span class="sxs-lookup"><span data-stu-id="84a0e-107">*htLine*</span></span> 
</dt> <dd>

<span data-ttu-id="84a0e-108">Das nicht transparente TAPI-Objekt Handle für das liniengerät.</span><span class="sxs-lookup"><span data-stu-id="84a0e-108">The TAPI opaque object handle to the line device.</span></span>

</dd> <dt>

<span data-ttu-id="84a0e-109">*"htcall"*</span><span class="sxs-lookup"><span data-stu-id="84a0e-109">*htCall*</span></span> 
</dt> <dd>

<span data-ttu-id="84a0e-110">Das nicht transparente TAPI-Objekt Handle für das anrufgerät.</span><span class="sxs-lookup"><span data-stu-id="84a0e-110">The TAPI opaque object handle to the call device.</span></span>

</dd> <dt>

<span data-ttu-id="84a0e-111">*dwmsg*</span><span class="sxs-lookup"><span data-stu-id="84a0e-111">*dwMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="84a0e-112">Die Wert Zeile \_ calldevspecificfeature.</span><span class="sxs-lookup"><span data-stu-id="84a0e-112">The value LINE\_CALLDEVSPECIFICFEATURE.</span></span>

</dd> <dt>

<span data-ttu-id="84a0e-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="84a0e-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="84a0e-114">Gerätespezifisch.</span><span class="sxs-lookup"><span data-stu-id="84a0e-114">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="84a0e-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="84a0e-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="84a0e-116">Gerätespezifisch.</span><span class="sxs-lookup"><span data-stu-id="84a0e-116">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="84a0e-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="84a0e-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="84a0e-118">Gerätespezifisch.</span><span class="sxs-lookup"><span data-stu-id="84a0e-118">Device specific.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="84a0e-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="84a0e-119">Remarks</span></span>

<span data-ttu-id="84a0e-120">Die **Zeile \_ calldevspecificfeature** wird von einem Dienstanbieter in Verbindung mit der Funktion [**TSPI \_ linedevspecificfeature**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecificfeature) verwendet.</span><span class="sxs-lookup"><span data-stu-id="84a0e-120">The **LINE\_CALLDEVSPECIFICFEATURE** message is used by a service provider in conjunction with the [**TSPI\_lineDevSpecificFeature**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecificfeature) function.</span></span> <span data-ttu-id="84a0e-121">Seine Bedeutung ist gerätespezifisch.</span><span class="sxs-lookup"><span data-stu-id="84a0e-121">Its meaning is device specific.</span></span>

<span data-ttu-id="84a0e-122">TAPI sendet die [**Zeile \_ devspecificfeature**](/previous-versions/windows/desktop/legacy/ms725227(v=vs.85)) -Nachricht als Antwort auf den Empfang dieser Nachricht von einem Dienstanbieter an Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="84a0e-122">TAPI sends the [**LINE\_DEVSPECIFICFEATURE**](/previous-versions/windows/desktop/legacy/ms725227(v=vs.85)) message to applications in response to receiving this message from a service provider.</span></span> <span data-ttu-id="84a0e-123">Die Parameter " *htline* " und " *htcall"* werden als *hdevice* -Parameter auf der TAPI-Ebene in den entsprechenden *hcallcenter* übersetzt.</span><span class="sxs-lookup"><span data-stu-id="84a0e-123">The *htLine* and *htCall* parameters are translated to the appropriate *hCall* as the *hDevice* parameter at the TAPI level.</span></span> <span data-ttu-id="84a0e-124">Die Parameter *dwParam1*, *dwParam2* und *dwParam3* werden unverändert übermittelt.</span><span class="sxs-lookup"><span data-stu-id="84a0e-124">The *dwParam1*, *dwParam2*, and *dwParam3* parameters are passed through unmodified.</span></span>

<span data-ttu-id="84a0e-125">Es gibt keine direkt entsprechende Meldung auf der TAPI-Ebene, obwohl diese Meldung mit line \_ devspecificfeature sehr ähnlich ist.</span><span class="sxs-lookup"><span data-stu-id="84a0e-125">There is no directly corresponding message at the TAPI level, although this message is very similar to LINE\_DEVSPECIFICFEATURE.</span></span> <span data-ttu-id="84a0e-126">Auf der TSPI-Ebene werden die gerätespezifischen Funktions Meldungen zwischen den Berichterstattungs Ereignissen in Zeilen und Adressen und den Bericht Erstellungs Ereignissen bei Aufrufen aufgeteilt.</span><span class="sxs-lookup"><span data-stu-id="84a0e-126">At the TSPI level, the device-specific feature messages are split between those reporting events on lines and addresses, and those reporting events on calls.</span></span>

## <a name="requirements"></a><span data-ttu-id="84a0e-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="84a0e-127">Requirements</span></span>



| <span data-ttu-id="84a0e-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="84a0e-128">Requirement</span></span> | <span data-ttu-id="84a0e-129">Wert</span><span class="sxs-lookup"><span data-stu-id="84a0e-129">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="84a0e-130">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="84a0e-130">TAPI version</span></span><br/> | <span data-ttu-id="84a0e-131">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="84a0e-131">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="84a0e-132">Header</span><span class="sxs-lookup"><span data-stu-id="84a0e-132">Header</span></span><br/>       | <dl> <span data-ttu-id="84a0e-133"><dt>TSPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="84a0e-133"><dt>Tspi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84a0e-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="84a0e-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="84a0e-135">[**LINE \_ devspecificfeature**](/previous-versions/windows/desktop/legacy/ms725227(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="84a0e-135">[**LINE\_DEVSPECIFICFEATURE**](/previous-versions/windows/desktop/legacy/ms725227(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="84a0e-136">**TSPI \_ linedevspecificfeature**</span><span class="sxs-lookup"><span data-stu-id="84a0e-136">**TSPI\_lineDevSpecificFeature**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecificfeature)
</dt> </dl>

 

