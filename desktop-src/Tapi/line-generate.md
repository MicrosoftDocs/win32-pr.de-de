---
description: Die TAPI-Zeile \_ zum Generieren der Nachricht wird gesendet, um die Anwendung zu benachrichtigen, dass die aktuelle Ziffern-oder Tongenerierung beendet wurde.
ms.assetid: 375823c5-22c2-4010-bfb4-5b8b46141c72
title: LINE_GENERATE Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b916dc95d1a6343b0f8ebc0eef9e589b04aa2112
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361381"
---
# <a name="line_generate-message"></a><span data-ttu-id="e8757-103">Zeile \_ generieren (Meldung)</span><span class="sxs-lookup"><span data-stu-id="e8757-103">LINE\_GENERATE message</span></span>

<span data-ttu-id="e8757-104">Die TAPI- **Zeile zum \_ generieren** der Nachricht wird gesendet, um die Anwendung zu benachrichtigen, dass die aktuelle Ziffern-oder Tongenerierung beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="e8757-104">The TAPI **LINE\_GENERATE** message is sent to notify the application that the current digit or tone generation has terminated.</span></span> <span data-ttu-id="e8757-105">Es kann immer nur eine solche Generierungs Anforderung für einen bestimmten Aufruf ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e8757-105">Only one such generation request can be in progress an a given call at any time.</span></span> <span data-ttu-id="e8757-106">Diese Meldung wird auch gesendet, wenn die Ziffern-oder Tongenerierung abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="e8757-106">This message is also sent when digit or tone generation is canceled.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="e8757-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8757-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8757-108">*hdevice*</span><span class="sxs-lookup"><span data-stu-id="e8757-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="e8757-109">Ein Handle für den-Befehl.</span><span class="sxs-lookup"><span data-stu-id="e8757-109">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="e8757-110">*dwcallbackinstance*</span><span class="sxs-lookup"><span data-stu-id="e8757-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="e8757-111">Die beim Öffnen der Zeile angegebene Rückruf Instanz.</span><span class="sxs-lookup"><span data-stu-id="e8757-111">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="e8757-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="e8757-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="e8757-113">Der Grund, warum die Ziffern-oder Tongenerierung beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="e8757-113">The reason why digit or tone generation was terminated.</span></span> <span data-ttu-id="e8757-114">Dieser Parameter darf nur eine der [**linegenerateterm- \_ Konstanten**](linegenerateterm--constants.md)sein.</span><span class="sxs-lookup"><span data-stu-id="e8757-114">This parameter must be one and only one of the [**LINEGENERATETERM\_ constants**](linegenerateterm--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="e8757-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="e8757-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="e8757-116">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="e8757-116">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="e8757-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="e8757-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="e8757-118">Die "Takt Anzahl" (Anzahl der Millisekunden seit dem Start von Windows), zu der die Ziffern-oder Tongenerierung abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="e8757-118">The "tick count" (number of milliseconds since Windows started) at which the digit or tone generation completed.</span></span> <span data-ttu-id="e8757-119">Bei API-Versionen vor 2,0 wird dieser Parameter nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="e8757-119">For API versions earlier than 2.0, this parameter is unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8757-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e8757-120">Return value</span></span>

<span data-ttu-id="e8757-121">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="e8757-121">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8757-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e8757-122">Remarks</span></span>

<span data-ttu-id="e8757-123">Die **Zeile Nachricht \_ generieren** wird nur an die Anwendung gesendet, die die Ziffern-oder Tongenerierung angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="e8757-123">The **LINE\_GENERATE** message is only sent to the application that requested the digit or tone generation.</span></span>

<span data-ttu-id="e8757-124">Da der durch *dwParam3* angegebene Zeitstempel möglicherweise auf einem anderen Computer als dem erstellt wurde, auf dem die Anwendung ausgeführt wird, ist er nur für den Vergleich mit anderen gleichzeitig auf demselben Zeilen Medium ( [**Zeilen \_ gatherziffern**](line-gatherdigits.md), [**Zeilen \_ monitorziffern**](line-monitordigits.md), [**line \_ monitormedia**](line-monitormedia.md), [**line \_ monitortone**](line-monitortone.md)) generierten Zeitstempel nützlich.</span><span class="sxs-lookup"><span data-stu-id="e8757-124">Because the timestamp specified by *dwParam3* may have been generated on a computer other than the one on which the application is executing, it is useful only for comparison to other similarly timestamped messages generated on the same line device ( [**LINE\_GATHERDIGITS**](line-gatherdigits.md), [**LINE\_MONITORDIGITS**](line-monitordigits.md), [**LINE\_MONITORMEDIA**](line-monitormedia.md), [**LINE\_MONITORTONE**](line-monitortone.md)), in order to determine their relative timing (separation between events).</span></span> <span data-ttu-id="e8757-125">Der Tick-Zähler kann nach ungefähr 49,7 Tagen umbrochen werden. Anwendungen müssen dies beim Durchführen von Berechnungen berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="e8757-125">The tick count can "wrap around" after approximately 49.7 days; applications must take this into account when performing calculations.</span></span>

<span data-ttu-id="e8757-126">Wenn der Dienstanbieter den Zeitstempel nicht generiert (z. b. wenn er mit einer früheren Version von TAPI erstellt wurde), gibt TAPI einen Zeitstempel an dem Punkt an, der dem Dienstanbieter am nächsten liegt, der das Ereignis generiert, sodass der erzeugte Zeitstempel so genau wie möglich ist.</span><span class="sxs-lookup"><span data-stu-id="e8757-126">If the service provider does not generate the timestamp (for example, if it was created using an earlier version of TAPI), then TAPI provides a timestamp at the point closest to the service provider generating the event so that the synthesized timestamp is as accurate as possible.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8757-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e8757-127">Requirements</span></span>



| <span data-ttu-id="e8757-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e8757-128">Requirement</span></span> | <span data-ttu-id="e8757-129">Wert</span><span class="sxs-lookup"><span data-stu-id="e8757-129">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e8757-130">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="e8757-130">TAPI version</span></span><br/> | <span data-ttu-id="e8757-131">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="e8757-131">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="e8757-132">Header</span><span class="sxs-lookup"><span data-stu-id="e8757-132">Header</span></span><br/>       | <dl> <span data-ttu-id="e8757-133"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8757-133"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8757-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8757-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8757-135">**Zeilen \_ gatherziffern**</span><span class="sxs-lookup"><span data-stu-id="e8757-135">**LINE\_GATHERDIGITS**</span></span>](line-gatherdigits.md)
</dt> <dt>

[<span data-ttu-id="e8757-136">**Zeilen \_ monitorziffern**</span><span class="sxs-lookup"><span data-stu-id="e8757-136">**LINE\_MONITORDIGITS**</span></span>](line-monitordigits.md)
</dt> <dt>

[<span data-ttu-id="e8757-137">**Zeilen- \_ monitormedia**</span><span class="sxs-lookup"><span data-stu-id="e8757-137">**LINE\_MONITORMEDIA**</span></span>](line-monitormedia.md)
</dt> <dt>

[<span data-ttu-id="e8757-138">**\_linienmonitortone**</span><span class="sxs-lookup"><span data-stu-id="e8757-138">**LINE\_MONITORTONE**</span></span>](line-monitortone.md)
</dt> </dl>

 

 




