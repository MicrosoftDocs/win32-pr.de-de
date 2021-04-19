---
description: Mit der Put \_ stopTime-Methode wird der Wert für die NTP-Endzeit (Netzwerk Zeitprotokoll) festgelegt. Wenn die Endzeit 0 (null) ist, wird die Sitzung nicht gebunden.
ms.assetid: 6f07054c-5fb2-4ee4-9025-3acf9b51ddbd
title: Ittime::p ut_StopTime-Methode (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53446ea1d7ee93589987c42b005d7a84e7e728ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366012"
---
# <a name="ittimeput_stoptime-method"></a><span data-ttu-id="df54b-104">Ittime::p UT \_ stopTime-Methode</span><span class="sxs-lookup"><span data-stu-id="df54b-104">ITTime::put\_StopTime method</span></span>

<span data-ttu-id="df54b-105">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="df54b-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="df54b-106">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="df54b-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="df54b-107">Mit der **Put \_ stopTime** -Methode wird der Wert für die NTP-Endzeit (Netzwerk Zeitprotokoll) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="df54b-107">The **put\_StopTime** method sets the NTP (Network Time Protocol) ending time value.</span></span> <span data-ttu-id="df54b-108">Wenn die Endzeit 0 (null) ist, wird die Sitzung nicht gebunden.</span><span class="sxs-lookup"><span data-stu-id="df54b-108">If the end time is zero, the session is not bounded.</span></span>

## <a name="syntax"></a><span data-ttu-id="df54b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="df54b-109">Syntax</span></span>


```C++
HRESULT put_StopTime(
  [in] DOUBLE Time
);
```



## <a name="parameters"></a><span data-ttu-id="df54b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="df54b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df54b-111">*Uhrzeit* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="df54b-111">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df54b-112">Endzeit für die Sitzung.</span><span class="sxs-lookup"><span data-stu-id="df54b-112">Stop time for the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df54b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="df54b-113">Return value</span></span>

<span data-ttu-id="df54b-114">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="df54b-114">This method can return one of these values.</span></span>



| <span data-ttu-id="df54b-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="df54b-115">Return code</span></span>                                                                                   | <span data-ttu-id="df54b-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="df54b-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="df54b-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="df54b-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="df54b-118">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="df54b-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="df54b-119"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="df54b-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="df54b-120">Der *Zeit* Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="df54b-120">The *Time* parameter is not valid.</span></span><br/>                   |
| <dl> <span data-ttu-id="df54b-121"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="df54b-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="df54b-122">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="df54b-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="df54b-123"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="df54b-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="df54b-124">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="df54b-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="df54b-125"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="df54b-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="df54b-126">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="df54b-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="df54b-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="df54b-127">Remarks</span></span>

<span data-ttu-id="df54b-128">Diese Funktion kann Daten in unverschlüsselter Form über das Netzwerk senden. aus diesem Grund kann ein Benutzer, der sich im Netzwerk befindet, möglicherweise die Daten lesen.</span><span class="sxs-lookup"><span data-stu-id="df54b-128">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="df54b-129">Das Sicherheitsrisiko, dass Daten im Klartext gesendet werden, sollte vor der Verwendung dieser Methode berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="df54b-129">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="df54b-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="df54b-130">Requirements</span></span>



| <span data-ttu-id="df54b-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="df54b-131">Requirement</span></span> | <span data-ttu-id="df54b-132">Wert</span><span class="sxs-lookup"><span data-stu-id="df54b-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="df54b-133">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="df54b-133">TAPI version</span></span><br/> | <span data-ttu-id="df54b-134">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="df54b-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="df54b-135">Header</span><span class="sxs-lookup"><span data-stu-id="df54b-135">Header</span></span><br/>       | <dl> <span data-ttu-id="df54b-136"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="df54b-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="df54b-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="df54b-137">Library</span></span><br/>      | <dl> <span data-ttu-id="df54b-138"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="df54b-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="df54b-139">DLL</span><span class="sxs-lookup"><span data-stu-id="df54b-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="df54b-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df54b-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df54b-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="df54b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df54b-142">**Ittime**</span><span class="sxs-lookup"><span data-stu-id="df54b-142">**ITTime**</span></span>](ittime.md)
</dt> <dt>

[<span data-ttu-id="df54b-143">**Ittime:: get \_ stopTime**</span><span class="sxs-lookup"><span data-stu-id="df54b-143">**ITTime::get\_StopTime**</span></span>](ittime-get-stoptime.md)
</dt> </dl>

 

 




