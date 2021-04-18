---
description: Die TAPI- \_ linienmonitortone-Nachricht wird gesendet, wenn ein Ton erkannt wird. Das Senden dieser Nachricht wird mit der linemonitortones-Funktion gesteuert.
ms.assetid: ffdca615-5341-4f02-bb38-b8133cd9477d
title: LINE_MONITORTONE Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de88863111dc0d00ea32953eeac76d4b570b5848
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358762"
---
# <a name="line_monitortone-message"></a><span data-ttu-id="48f26-104">Zeile \_ monitortone-Meldung</span><span class="sxs-lookup"><span data-stu-id="48f26-104">LINE\_MONITORTONE message</span></span>

<span data-ttu-id="48f26-105">Die TAPI **- \_ linienmonitortone** -Nachricht wird gesendet, wenn ein Ton erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="48f26-105">The TAPI **LINE\_MONITORTONE** message is sent when a tone is detected.</span></span> <span data-ttu-id="48f26-106">Das Senden dieser Nachricht wird mit der [**linemonitortones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones) -Funktion gesteuert.</span><span class="sxs-lookup"><span data-stu-id="48f26-106">The sending of this message is controlled with the [**lineMonitorTones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones) function.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="48f26-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="48f26-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48f26-108">*hdevice*</span><span class="sxs-lookup"><span data-stu-id="48f26-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="48f26-109">Ein Handle für den-Befehl.</span><span class="sxs-lookup"><span data-stu-id="48f26-109">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="48f26-110">*dwcallbackinstance*</span><span class="sxs-lookup"><span data-stu-id="48f26-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="48f26-111">Die beim Öffnen der Zeile des Aufrufs angegebene Rückruf Instanz.</span><span class="sxs-lookup"><span data-stu-id="48f26-111">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="48f26-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="48f26-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="48f26-113">Der anwendungsspezifische **dwappspecific** -Member der [**linemonitortone**](/windows/desktop/api/Tapi/ns-tapi-linemonitortone) -Struktur für den erkannten Farbton.</span><span class="sxs-lookup"><span data-stu-id="48f26-113">The application-specific **dwAppSpecific** member of the [**LINEMONITORTONE**](/windows/desktop/api/Tapi/ns-tapi-linemonitortone) structure for the tone that was detected.</span></span>

</dd> <dt>

<span data-ttu-id="48f26-114">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="48f26-114">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="48f26-115">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="48f26-115">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="48f26-116">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="48f26-116">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="48f26-117">Die "Takt Anzahl" (Anzahl der Millisekunden seit dem Start von Windows), bei der der Ton erkannt wurde.</span><span class="sxs-lookup"><span data-stu-id="48f26-117">The "tick count" (number of milliseconds since Windows started) at which the tone was detected.</span></span> <span data-ttu-id="48f26-118">Bei API-Versionen vor 2,0 wird dieser Parameter nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="48f26-118">For API versions earlier than 2.0, this parameter is unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48f26-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="48f26-119">Return value</span></span>

<span data-ttu-id="48f26-120">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="48f26-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="48f26-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="48f26-121">Remarks</span></span>

<span data-ttu-id="48f26-122">Die **Zeile " \_ monitortone** " wird nur an die Anwendung gesendet, die den überwachten Ton angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="48f26-122">The **LINE\_MONITORTONE** message is only sent to the application that has requested the tone be monitored.</span></span>

<span data-ttu-id="48f26-123">Da dieser Zeitstempel möglicherweise auf einem anderen Computer als dem erstellt wurde, auf dem die Anwendung ausgeführt wird, ist er nur für Vergleiche mit anderen gleichzeitig auf demselben Zeilen Gerät ( [**Zeilen \_ gatherziffern**](line-gatherdigits.md), [**Zeilen \_ Generierung**](line-generate.md), [**Zeilen \_ Monitor Ziffern**](line-monitordigits.md), Zeilen Überwachung) generierten Nachrichten **nützlich \_**, um deren relative zeitliche Steuerung (Trennung zwischen Ereignissen) zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="48f26-123">Because this timestamp may have been generated on a computer other than the one on which the application is executing, it is useful only for comparison to other similarly timestamped messages generated on the same line device ( [**LINE\_GATHERDIGITS**](line-gatherdigits.md), [**LINE\_GENERATE**](line-generate.md), [**LINE\_MONITORDIGITS**](line-monitordigits.md), **LINE\_MONITORTONE**), in order to determine their relative timing (separation between events).</span></span> <span data-ttu-id="48f26-124">Der Tick-Zähler kann nach ungefähr 49,7 Tagen umbrochen werden. Anwendungen müssen dies beim Durchführen von Berechnungen berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="48f26-124">The tick count can "wrap around" after approximately 49.7 days; applications must take this into account when performing calculations.</span></span>

<span data-ttu-id="48f26-125">Wenn der Dienstanbieter den Zeitstempel nicht generiert (z. b. wenn er mit einer früheren Version von TAPI erstellt wurde), gibt TAPI einen Zeitstempel an dem Punkt an, der dem Dienstanbieter am nächsten liegt, der das Ereignis generiert, sodass der erzeugte Zeitstempel so genau wie möglich ist.</span><span class="sxs-lookup"><span data-stu-id="48f26-125">If the service provider does not generate the timestamp (for example, if it was created using an earlier version of TAPI), then TAPI provides a timestamp at the point closest to the service provider generating the event so that the synthesized timestamp is as accurate as possible.</span></span>

## <a name="requirements"></a><span data-ttu-id="48f26-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="48f26-126">Requirements</span></span>



| <span data-ttu-id="48f26-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="48f26-127">Requirement</span></span> | <span data-ttu-id="48f26-128">Wert</span><span class="sxs-lookup"><span data-stu-id="48f26-128">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="48f26-129">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="48f26-129">TAPI version</span></span><br/> | <span data-ttu-id="48f26-130">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="48f26-130">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="48f26-131">Header</span><span class="sxs-lookup"><span data-stu-id="48f26-131">Header</span></span><br/>       | <dl> <span data-ttu-id="48f26-132"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="48f26-132"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48f26-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48f26-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48f26-134">**Zeilen \_ gatherziffern**</span><span class="sxs-lookup"><span data-stu-id="48f26-134">**LINE\_GATHERDIGITS**</span></span>](line-gatherdigits.md)
</dt> <dt>

[<span data-ttu-id="48f26-135">**Zeilen \_ Generierung**</span><span class="sxs-lookup"><span data-stu-id="48f26-135">**LINE\_GENERATE**</span></span>](line-generate.md)
</dt> <dt>

[<span data-ttu-id="48f26-136">**Zeilen \_ monitorziffern**</span><span class="sxs-lookup"><span data-stu-id="48f26-136">**LINE\_MONITORDIGITS**</span></span>](line-monitordigits.md)
</dt> <dt>

[<span data-ttu-id="48f26-137">**Linemonitortone**</span><span class="sxs-lookup"><span data-stu-id="48f26-137">**LINEMONITORTONE**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linemonitortone)
</dt> <dt>

[<span data-ttu-id="48f26-138">**linemonitortones**</span><span class="sxs-lookup"><span data-stu-id="48f26-138">**lineMonitorTones**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemonitortones)
</dt> </dl>

 

 




