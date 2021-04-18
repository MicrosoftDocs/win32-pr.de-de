---
description: Die TAPI \_ -Line gatherdigits-Nachricht wird gesendet, wenn die aktuelle gepufferte Digit-Sammlungs Anforderung beendet oder abgebrochen wurde. Der Ziffern Puffer kann überprüft werden, nachdem diese Nachricht von der Anwendung empfangen wurde.
ms.assetid: 0d27904d-9743-44bf-a7bc-132459351e01
title: LINE_GATHERDIGITS Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f0c67c5a9bbd3f798a8f4343b36c311309633ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358060"
---
# <a name="line_gatherdigits-message"></a><span data-ttu-id="fc4ba-104">Zeile \_ gatherdigits-Meldung</span><span class="sxs-lookup"><span data-stu-id="fc4ba-104">LINE\_GATHERDIGITS message</span></span>

<span data-ttu-id="fc4ba-105">Die TAPI- **line \_ gatherdigits** -Nachricht wird gesendet, wenn die aktuelle gepufferte Digit-Sammlungs Anforderung beendet oder abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="fc4ba-105">The TAPI **LINE\_GATHERDIGITS** message is sent when the current buffered digit-gathering request has terminated or is canceled.</span></span> <span data-ttu-id="fc4ba-106">Der Ziffern Puffer kann überprüft werden, nachdem diese Nachricht von der Anwendung empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="fc4ba-106">The digit buffer can be examined after this message has been received by the application.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="fc4ba-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="fc4ba-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc4ba-108">*hdevice*</span><span class="sxs-lookup"><span data-stu-id="fc4ba-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="fc4ba-109">Ein Handle für den-Befehl.</span><span class="sxs-lookup"><span data-stu-id="fc4ba-109">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="fc4ba-110">*dwcallbackinstance*</span><span class="sxs-lookup"><span data-stu-id="fc4ba-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="fc4ba-111">Die beim Öffnen der Zeile angegebene Rückruf Instanz.</span><span class="sxs-lookup"><span data-stu-id="fc4ba-111">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="fc4ba-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="fc4ba-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="fc4ba-113">Der Grund, warum die Ziffern Erfassung beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="fc4ba-113">The reason why digit gathering was terminated.</span></span> <span data-ttu-id="fc4ba-114">Dieser Parameter darf nur eine der [**linegatherterm- \_ Konstanten**](linegatherterm--constants.md)sein.</span><span class="sxs-lookup"><span data-stu-id="fc4ba-114">This parameter must be one and only one of the [**LINEGATHERTERM\_ constants**](linegatherterm--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc4ba-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="fc4ba-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="fc4ba-116">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="fc4ba-116">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="fc4ba-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="fc4ba-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="fc4ba-118">Die "Takt Anzahl" (Anzahl der Millisekunden seit dem Start von Windows), bei der die Ziffern Erfassung abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="fc4ba-118">The "tick count" (number of milliseconds since Windows started) at which the digit gathering completed.</span></span> <span data-ttu-id="fc4ba-119">Für TAPI-Versionen vor 2,0 wird dieser Parameter nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="fc4ba-119">For TAPI versions earlier than 2.0, this parameter is unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc4ba-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fc4ba-120">Return value</span></span>

<span data-ttu-id="fc4ba-121">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="fc4ba-121">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc4ba-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fc4ba-122">Remarks</span></span>

<span data-ttu-id="fc4ba-123">Die Meldung " **line \_ gatherdigits** " wird nur an die Anwendung gesendet, die die Ziffern Erfassung für den-Befehl mithilfe von [**linegatherdigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits)initiiert hat.</span><span class="sxs-lookup"><span data-stu-id="fc4ba-123">The **LINE\_GATHERDIGITS** message is only sent to the application that initiated the digit gathering on the call using [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits).</span></span>

<span data-ttu-id="fc4ba-124">Wenn die [**linegatherdigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits) -Funktion verwendet wird, um eine vorherige Anforderung zum Erfassen von Ziffern abzubrechen, sendet TAPI eine **Zeile \_ gatherdigits** -Nachricht, bei der *dwParam1* auf linegatherterm Abbrechen festgelegt ist, \_ um anzugeben, dass der ursprünglich angegebene Puffer die Ziffern enthält, die für den Abbruch erfasst wurden.</span><span class="sxs-lookup"><span data-stu-id="fc4ba-124">If the [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits) function is used to cancel a previous request to gather digits, TAPI sends a **LINE\_GATHERDIGITS** message with *dwParam1* set to LINEGATHERTERM\_CANCEL to the application indicating that the originally specified buffer contains the digits gathered up to the cancellation.</span></span>

<span data-ttu-id="fc4ba-125">Da der durch *dwParam3* angegebene Zeitstempel möglicherweise auf einem anderen Computer als dem erstellt wurde, auf dem die Anwendung ausgeführt wird, ist er nur für Vergleiche mit anderen auf demselben Zeilen Gerät ( [**Zeilen \_ Generierung**](line-generate.md), Zeilen Überwachung, [**Zeilen \_**](line-monitormedia.md)Überwachung, Zeilen Überwachung) generierten Nachrichten nützlich, um deren relative zeitliche Steuerung (Trennung zwischen [**Ereignissen) \_ zu**](line-monitortone.md)bestimmen. [**\_**](line-monitordigits.md)</span><span class="sxs-lookup"><span data-stu-id="fc4ba-125">Because the timestamp specified by *dwParam3* may have been generated on a computer other than the one on which the application is executing, it is useful only for comparison to other similarly timestamped messages generated on the same line device ( [**LINE\_GENERATE**](line-generate.md), [**LINE\_MONITORDIGITS**](line-monitordigits.md), [**LINE\_MONITORMEDIA**](line-monitormedia.md), [**LINE\_MONITORTONE**](line-monitortone.md)), in order to determine their relative timing (separation between events).</span></span> <span data-ttu-id="fc4ba-126">Der Tick-Zähler kann nach ungefähr 49,7 Tagen umbrochen werden. Anwendungen müssen dies beim Durchführen von Berechnungen berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="fc4ba-126">The tick count can "wrap around" after approximately 49.7 days; applications must take this into account when performing calculations.</span></span>

<span data-ttu-id="fc4ba-127">Wenn der Dienstanbieter den Zeitstempel nicht generiert (z. b. wenn er mit einer früheren Version von TAPI erstellt wurde), gibt TAPI einen Zeitstempel an dem Punkt an, der dem Dienstanbieter am nächsten liegt, der das Ereignis generiert, sodass der erzeugte Zeitstempel so genau wie möglich ist.</span><span class="sxs-lookup"><span data-stu-id="fc4ba-127">If the service provider does not generate the timestamp (for example, if it was created using an earlier version of TAPI), then TAPI provides a timestamp at the point closest to the service provider generating the event so that the synthesized timestamp is as accurate as possible.</span></span>

> [!Note]  
> <span data-ttu-id="fc4ba-128">Wenn eine Anwendung einen asynchronen Vorgang aufruft, mit dem Daten in den Anwendungs Speicher geschrieben werden, muss die Anwendung diesen Arbeitsspeicher für das Schreiben verfügbar halten, bis eine [**Zeilen \_ Antwort**](line-reply.md) oder eine **Zeile \_ gatherdigits** -Nachricht empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="fc4ba-128">When an application invokes any asynchronous operation that writes data back into application memory, the application must keep that memory available for writing until a [**LINE\_REPLY**](line-reply.md) or **LINE\_GATHERDIGITS** message is received.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fc4ba-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fc4ba-129">Requirements</span></span>



| <span data-ttu-id="fc4ba-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fc4ba-130">Requirement</span></span> | <span data-ttu-id="fc4ba-131">Wert</span><span class="sxs-lookup"><span data-stu-id="fc4ba-131">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="fc4ba-132">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="fc4ba-132">TAPI version</span></span><br/> | <span data-ttu-id="fc4ba-133">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="fc4ba-133">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="fc4ba-134">Header</span><span class="sxs-lookup"><span data-stu-id="fc4ba-134">Header</span></span><br/>       | <dl> <span data-ttu-id="fc4ba-135"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc4ba-135"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc4ba-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fc4ba-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc4ba-137">**Zeilen \_ Generierung**</span><span class="sxs-lookup"><span data-stu-id="fc4ba-137">**LINE\_GENERATE**</span></span>](line-generate.md)
</dt> <dt>

[<span data-ttu-id="fc4ba-138">**Zeilen \_ monitorziffern**</span><span class="sxs-lookup"><span data-stu-id="fc4ba-138">**LINE\_MONITORDIGITS**</span></span>](line-monitordigits.md)
</dt> <dt>

[<span data-ttu-id="fc4ba-139">**Zeilen- \_ monitormedia**</span><span class="sxs-lookup"><span data-stu-id="fc4ba-139">**LINE\_MONITORMEDIA**</span></span>](line-monitormedia.md)
</dt> <dt>

[<span data-ttu-id="fc4ba-140">**\_linienmonitortone**</span><span class="sxs-lookup"><span data-stu-id="fc4ba-140">**LINE\_MONITORTONE**</span></span>](line-monitortone.md)
</dt> <dt>

[<span data-ttu-id="fc4ba-141">**Zeilen \_ Antwort**</span><span class="sxs-lookup"><span data-stu-id="fc4ba-141">**LINE\_REPLY**</span></span>](line-reply.md)
</dt> <dt>

[<span data-ttu-id="fc4ba-142">**linegather-Ziffern**</span><span class="sxs-lookup"><span data-stu-id="fc4ba-142">**lineGatherDigits**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits)
</dt> </dl>

 

 




