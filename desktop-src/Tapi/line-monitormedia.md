---
description: Die TAPI-LINE_MONITORMEDIA Nachricht wird gesendet, wenn eine Änderung im Medientyp "Aufrufe" erkannt wird. Das Senden dieser Nachricht wird mit der linemonitormedia-Funktion gesteuert.
ms.assetid: 1cfba455-9a15-45f3-8d56-74b8348e080e
title: LINE_MONITORMEDIA Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7b6e3d0d2928ab3256b844a27727657978dbe0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352972"
---
# <a name="line_monitormedia-message"></a><span data-ttu-id="65ca1-104">Zeile \_ monitormedia-Meldung</span><span class="sxs-lookup"><span data-stu-id="65ca1-104">LINE\_MONITORMEDIA message</span></span>

<span data-ttu-id="65ca1-105">Die TAPI **- \_ Linien** Überwachung wird gesendet, wenn eine Änderung im Medientyp des Aufrufes erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="65ca1-105">The TAPI **LINE\_MONITORMEDIA** message is sent when a change in the call's media type is detected.</span></span> <span data-ttu-id="65ca1-106">Das Senden dieser Nachricht wird mit der [**linemonitormedia**](/windows/desktop/api/Tapi/nf-tapi-linemonitormedia) -Funktion gesteuert.</span><span class="sxs-lookup"><span data-stu-id="65ca1-106">The sending of this message is controlled with the [**lineMonitorMedia**](/windows/desktop/api/Tapi/nf-tapi-linemonitormedia) function.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="65ca1-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="65ca1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65ca1-108">*hdevice*</span><span class="sxs-lookup"><span data-stu-id="65ca1-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="65ca1-109">Ein Handle für den-Befehl.</span><span class="sxs-lookup"><span data-stu-id="65ca1-109">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="65ca1-110">*dwcallbackinstance*</span><span class="sxs-lookup"><span data-stu-id="65ca1-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="65ca1-111">Die beim Öffnen der Zeile angegebene Rückruf Instanz.</span><span class="sxs-lookup"><span data-stu-id="65ca1-111">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="65ca1-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="65ca1-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="65ca1-113">Der neue Medientyp (oder-Modus).</span><span class="sxs-lookup"><span data-stu-id="65ca1-113">The new media type (or mode).</span></span> <span data-ttu-id="65ca1-114">Dieser Parameter darf nur eine der [**linemediamode- \_ Konstanten**](linemediamode--constants.md)sein.</span><span class="sxs-lookup"><span data-stu-id="65ca1-114">This parameter must be one and only one of the [**LINEMEDIAMODE\_ constants**](linemediamode--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="65ca1-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="65ca1-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="65ca1-116">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="65ca1-116">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="65ca1-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="65ca1-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="65ca1-118">Die "Takt Anzahl" (Anzahl der Millisekunden seit dem Start von Windows), an der das angegebene Medium erkannt wurde.</span><span class="sxs-lookup"><span data-stu-id="65ca1-118">The "tick count" (number of milliseconds since Windows started) at which the specified media was detected.</span></span> <span data-ttu-id="65ca1-119">Für TAPI-Versionen vor 2,0 wird dieser Parameter nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="65ca1-119">For TAPI versions earlier than 2.0, this parameter is unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65ca1-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="65ca1-120">Return value</span></span>

<span data-ttu-id="65ca1-121">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="65ca1-121">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="65ca1-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="65ca1-122">Remarks</span></span>

<span data-ttu-id="65ca1-123">Die **Zeile \_ monitormedia** -Nachricht wird an die Anwendung gesendet, die die Medienüberwachung für den erkannten Medientyp aktiviert hat.</span><span class="sxs-lookup"><span data-stu-id="65ca1-123">The **LINE\_MONITORMEDIA** message is sent to the application that has enabled media monitoring for the media type detected.</span></span>

<span data-ttu-id="65ca1-124">Da dieser Zeitstempel möglicherweise auf einem anderen Computer als dem erstellt wurde, auf dem die Anwendung ausgeführt wird, ist er nur für Vergleiche mit anderen gleichzeitig auf demselben Zeilen Gerät ( [**Zeilen \_ gatherziffern**](line-gatherdigits.md), [**Zeilen \_ Generierung**](line-generate.md), [**Zeilen \_ Monitor Ziffern**](line-monitordigits.md), Zeilen Überwachung) generierten Nachrichten [**nützlich \_**](line-monitortone.md), um deren relative zeitliche Steuerung (Trennung zwischen Ereignissen) zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="65ca1-124">Because this timestamp may have been generated on a computer other than the one on which the application is executing, it is useful only for comparison to other similarly timestamped messages generated on the same line device ( [**LINE\_GATHERDIGITS**](line-gatherdigits.md), [**LINE\_GENERATE**](line-generate.md), [**LINE\_MONITORDIGITS**](line-monitordigits.md), [**LINE\_MONITORTONE**](line-monitortone.md)), in order to determine their relative timing (separation between events).</span></span> <span data-ttu-id="65ca1-125">Der Tick-Zähler kann nach ungefähr 49,7 Tagen umbrochen werden. Anwendungen müssen dies beim Durchführen von Berechnungen berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="65ca1-125">The tick count can "wrap around" after approximately 49.7 days; applications must take this into account when performing calculations.</span></span>

<span data-ttu-id="65ca1-126">Wenn der Dienstanbieter den Zeitstempel nicht generiert (z. b. wenn er mit einer früheren Version von TAPI erstellt wurde), gibt TAPI einen Zeitstempel an dem Punkt an, der dem Dienstanbieter am nächsten liegt, der das Ereignis generiert, sodass der erzeugte Zeitstempel so genau wie möglich ist.</span><span class="sxs-lookup"><span data-stu-id="65ca1-126">If the service provider does not generate the timestamp (for example, if it was created using an earlier version of TAPI), then TAPI provides a timestamp at the point closest to the service provider generating the event so that the synthesized timestamp is as accurate as possible.</span></span>

## <a name="requirements"></a><span data-ttu-id="65ca1-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="65ca1-127">Requirements</span></span>



| <span data-ttu-id="65ca1-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="65ca1-128">Requirement</span></span> | <span data-ttu-id="65ca1-129">Wert</span><span class="sxs-lookup"><span data-stu-id="65ca1-129">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="65ca1-130">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="65ca1-130">TAPI version</span></span><br/> | <span data-ttu-id="65ca1-131">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="65ca1-131">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="65ca1-132">Header</span><span class="sxs-lookup"><span data-stu-id="65ca1-132">Header</span></span><br/>       | <dl> <span data-ttu-id="65ca1-133"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="65ca1-133"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65ca1-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="65ca1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65ca1-135">**Zeilen \_ gatherziffern**</span><span class="sxs-lookup"><span data-stu-id="65ca1-135">**LINE\_GATHERDIGITS**</span></span>](line-gatherdigits.md)
</dt> <dt>

[<span data-ttu-id="65ca1-136">**Zeilen \_ Generierung**</span><span class="sxs-lookup"><span data-stu-id="65ca1-136">**LINE\_GENERATE**</span></span>](line-generate.md)
</dt> <dt>

[<span data-ttu-id="65ca1-137">**Zeilen \_ monitorziffern**</span><span class="sxs-lookup"><span data-stu-id="65ca1-137">**LINE\_MONITORDIGITS**</span></span>](line-monitordigits.md)
</dt> <dt>

[<span data-ttu-id="65ca1-138">**\_linienmonitortone**</span><span class="sxs-lookup"><span data-stu-id="65ca1-138">**LINE\_MONITORTONE**</span></span>](line-monitortone.md)
</dt> </dl>

 

 




