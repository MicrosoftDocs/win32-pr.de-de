---
description: Die TAPI- \_ linienmonitordigits-Nachricht wird gesendet, wenn eine Ziffer erkannt wird. Das Senden dieser Nachricht wird mit der linemonitordigits-Funktion gesteuert.
ms.assetid: 1c1a729c-a6bb-4432-9617-4a892c76cb8d
title: LINE_MONITORDIGITS Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c6e85ed515d20c18c6e41cdb185b036312c54ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368440"
---
# <a name="line_monitordigits-message"></a><span data-ttu-id="82859-104">Zeile " \_ monitordigits"-Meldung</span><span class="sxs-lookup"><span data-stu-id="82859-104">LINE\_MONITORDIGITS message</span></span>

<span data-ttu-id="82859-105">Die TAPI **- \_ linienmonitordigits** -Nachricht wird gesendet, wenn eine Ziffer erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="82859-105">The TAPI **LINE\_MONITORDIGITS** message is sent when a digit is detected.</span></span> <span data-ttu-id="82859-106">Das Senden dieser Nachricht wird mit der [**linemonitordigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits) -Funktion gesteuert.</span><span class="sxs-lookup"><span data-stu-id="82859-106">The sending of this message is controlled with the [**lineMonitorDigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits) function.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="82859-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="82859-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82859-108">*hdevice*</span><span class="sxs-lookup"><span data-stu-id="82859-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="82859-109">Ein Handle für den-Befehl.</span><span class="sxs-lookup"><span data-stu-id="82859-109">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="82859-110">*dwcallbackinstance*</span><span class="sxs-lookup"><span data-stu-id="82859-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="82859-111">Die beim Öffnen der Zeile des Aufrufs angegebene Rückruf Instanz.</span><span class="sxs-lookup"><span data-stu-id="82859-111">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="82859-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="82859-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="82859-113">Das nieder wertige Byte enthält die letzte in einer Textdarstellung empfangene Ziffer.</span><span class="sxs-lookup"><span data-stu-id="82859-113">The low-order byte contains the last digit received in a text representation.</span></span>

</dd> <dt>

<span data-ttu-id="82859-114">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="82859-114">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="82859-115">Der Ziffern Modus, der erkannt wurde.</span><span class="sxs-lookup"><span data-stu-id="82859-115">The digit mode that was detected.</span></span> <span data-ttu-id="82859-116">Dieser Parameter darf nur eine der [**linedigitmode- \_ Konstanten**](linedigitmode--constants.md)sein.</span><span class="sxs-lookup"><span data-stu-id="82859-116">This parameter must be one and only one of the [**LINEDIGITMODE\_ constants**](linedigitmode--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="82859-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="82859-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="82859-118">Die "Takt Anzahl" (Anzahl der Millisekunden seit dem Start von Windows), bei der die angegebene Ziffer erkannt wurde.</span><span class="sxs-lookup"><span data-stu-id="82859-118">The "tick count" (number of milliseconds since Windows started) at which the specified digit was detected.</span></span> <span data-ttu-id="82859-119">Für TAPI-Versionen vor 2,0 wird dieser Parameter nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="82859-119">For TAPI versions earlier than 2.0, this parameter is unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82859-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="82859-120">Return value</span></span>

<span data-ttu-id="82859-121">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="82859-121">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="82859-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="82859-122">Remarks</span></span>

<span data-ttu-id="82859-123">Die Meldung **Zeile \_ monitordigits** wird an die Anwendung gesendet, in der die Ziffern Überwachung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="82859-123">The **LINE\_MONITORDIGITS** message is sent to the application that has enabled digit monitoring.</span></span>

<span data-ttu-id="82859-124">Da dieser Zeitstempel möglicherweise auf einem anderen Computer als dem erstellt wurde, auf dem die Anwendung ausgeführt wird, ist er nur für Vergleiche mit anderen gleichzeitig auf demselben Zeilen Gerät ( [**Zeilen \_ gatherziffern**](line-gatherdigits.md), [**Zeilen \_ Generierung**](line-generate.md), [**Zeilen \_**](line-monitormedia.md)Überwachung, Zeilen Überwachung) generierten Nachrichten nützlich, um deren relative zeitliche Steuerung (Trennung zwischen Ereignissen) zu bestimmen. [**\_**](line-monitortone.md)</span><span class="sxs-lookup"><span data-stu-id="82859-124">Because this timestamp may have been generated on a computer other than the one on which the application is executing, it is useful only for comparison to other similarly timestamped messages generated on the same line device ( [**LINE\_GATHERDIGITS**](line-gatherdigits.md), [**LINE\_GENERATE**](line-generate.md), [**LINE\_MONITORMEDIA**](line-monitormedia.md), [**LINE\_MONITORTONE**](line-monitortone.md)), in order to determine their relative timing (separation between events).</span></span> <span data-ttu-id="82859-125">Der Tick-Zähler kann nach ungefähr 49,7 Tagen umbrochen werden. Anwendungen müssen dies beim Durchführen von Berechnungen berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="82859-125">The tick count can "wrap around" after approximately 49.7 days; applications must take this into account when performing calculations.</span></span>

<span data-ttu-id="82859-126">Wenn der Dienstanbieter den Zeitstempel nicht generiert (z. b. wenn er mit einer früheren Version von TAPI erstellt wurde), gibt TAPI einen Zeitstempel an dem Punkt an, der dem Dienstanbieter am nächsten liegt, der das Ereignis generiert, sodass der erzeugte Zeitstempel so genau wie möglich ist.</span><span class="sxs-lookup"><span data-stu-id="82859-126">If the service provider does not generate the timestamp (for example, if it was created using an earlier version of TAPI), then TAPI provides a timestamp at the point closest to the service provider generating the event so that the synthesized timestamp is as accurate as possible.</span></span>

## <a name="requirements"></a><span data-ttu-id="82859-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="82859-127">Requirements</span></span>



| <span data-ttu-id="82859-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="82859-128">Requirement</span></span> | <span data-ttu-id="82859-129">Wert</span><span class="sxs-lookup"><span data-stu-id="82859-129">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="82859-130">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="82859-130">TAPI version</span></span><br/> | <span data-ttu-id="82859-131">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="82859-131">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="82859-132">Header</span><span class="sxs-lookup"><span data-stu-id="82859-132">Header</span></span><br/>       | <dl> <span data-ttu-id="82859-133"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="82859-133"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82859-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="82859-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82859-135">**Zeilen \_ gatherziffern**</span><span class="sxs-lookup"><span data-stu-id="82859-135">**LINE\_GATHERDIGITS**</span></span>](line-gatherdigits.md)
</dt> <dt>

[<span data-ttu-id="82859-136">**Zeilen \_ Generierung**</span><span class="sxs-lookup"><span data-stu-id="82859-136">**LINE\_GENERATE**</span></span>](line-generate.md)
</dt> <dt>

[<span data-ttu-id="82859-137">**Zeilen- \_ monitormedia**</span><span class="sxs-lookup"><span data-stu-id="82859-137">**LINE\_MONITORMEDIA**</span></span>](line-monitormedia.md)
</dt> <dt>

[<span data-ttu-id="82859-138">**\_linienmonitortone**</span><span class="sxs-lookup"><span data-stu-id="82859-138">**LINE\_MONITORTONE**</span></span>](line-monitortone.md)
</dt> <dt>

[<span data-ttu-id="82859-139">**linemonitordigits**</span><span class="sxs-lookup"><span data-stu-id="82859-139">**lineMonitorDigits**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits)
</dt> </dl>

 

 




