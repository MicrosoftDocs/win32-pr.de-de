---
description: Die Put \_ StartTime-Methode legt den Wert für den 32-Bit-NTP (Network Time Protocol)-Start Zeitwert fest. Die Sitzung gilt ab diesem Zeitpunkt als aktiv.
ms.assetid: c7c96265-4588-4f05-83b6-6ef54f02650b
title: Ittime::p ut_StartTime-Methode (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a5b574f7c90d7cc2f92204e3a045b33e6fb8480
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358341"
---
# <a name="ittimeput_starttime-method"></a><span data-ttu-id="28ef8-104">Ittime::p UT- \_ StartTime-Methode</span><span class="sxs-lookup"><span data-stu-id="28ef8-104">ITTime::put\_StartTime method</span></span>

<span data-ttu-id="28ef8-105">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="28ef8-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="28ef8-106">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="28ef8-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="28ef8-107">Die **Put \_ StartTime** -Methode legt den Wert für den 32-Bit-NTP (Network Time Protocol)-Start Zeitwert fest.</span><span class="sxs-lookup"><span data-stu-id="28ef8-107">The **put\_StartTime** method sets the 32-bit NTP (Network Time Protocol) starting time value.</span></span> <span data-ttu-id="28ef8-108">Die Sitzung gilt ab diesem Zeitpunkt als aktiv.</span><span class="sxs-lookup"><span data-stu-id="28ef8-108">The session is considered active from this time.</span></span>

## <a name="syntax"></a><span data-ttu-id="28ef8-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="28ef8-109">Syntax</span></span>


```C++
HRESULT put_StartTime(
  [in] DOUBLE Time
);
```



## <a name="parameters"></a><span data-ttu-id="28ef8-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="28ef8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28ef8-111">*Uhrzeit* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="28ef8-111">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28ef8-112">Startzeit für die Sitzung.</span><span class="sxs-lookup"><span data-stu-id="28ef8-112">Start time for the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28ef8-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="28ef8-113">Return value</span></span>

<span data-ttu-id="28ef8-114">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="28ef8-114">This method can return one of these values.</span></span>



| <span data-ttu-id="28ef8-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="28ef8-115">Return code</span></span>                                                                                   | <span data-ttu-id="28ef8-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="28ef8-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="28ef8-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="28ef8-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="28ef8-118">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="28ef8-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="28ef8-119"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="28ef8-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="28ef8-120">Der Parameter " *Tim* e" ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="28ef8-120">The *Tim* e parameter is not valid.</span></span><br/>                   |
| <dl> <span data-ttu-id="28ef8-121"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="28ef8-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="28ef8-122">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="28ef8-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="28ef8-123"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="28ef8-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="28ef8-124">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="28ef8-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="28ef8-125"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="28ef8-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="28ef8-126">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="28ef8-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="28ef8-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="28ef8-127">Remarks</span></span>

<span data-ttu-id="28ef8-128">Diese Funktion kann Daten in unverschlüsselter Form über das Netzwerk senden. aus diesem Grund kann ein Benutzer, der sich im Netzwerk befindet, möglicherweise die Daten lesen.</span><span class="sxs-lookup"><span data-stu-id="28ef8-128">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="28ef8-129">Das Sicherheitsrisiko, dass Daten im Klartext gesendet werden, sollte vor der Verwendung dieser Methode berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="28ef8-129">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="28ef8-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="28ef8-130">Requirements</span></span>



| <span data-ttu-id="28ef8-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="28ef8-131">Requirement</span></span> | <span data-ttu-id="28ef8-132">Wert</span><span class="sxs-lookup"><span data-stu-id="28ef8-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="28ef8-133">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="28ef8-133">TAPI version</span></span><br/> | <span data-ttu-id="28ef8-134">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="28ef8-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="28ef8-135">Header</span><span class="sxs-lookup"><span data-stu-id="28ef8-135">Header</span></span><br/>       | <dl> <span data-ttu-id="28ef8-136"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="28ef8-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="28ef8-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="28ef8-137">Library</span></span><br/>      | <dl> <span data-ttu-id="28ef8-138"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="28ef8-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="28ef8-139">DLL</span><span class="sxs-lookup"><span data-stu-id="28ef8-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="28ef8-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28ef8-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28ef8-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28ef8-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28ef8-142">**Ittime**</span><span class="sxs-lookup"><span data-stu-id="28ef8-142">**ITTime**</span></span>](ittime.md)
</dt> <dt>

[<span data-ttu-id="28ef8-143">**Ittime:: get \_ StartTime**</span><span class="sxs-lookup"><span data-stu-id="28ef8-143">**ITTime::get\_StartTime**</span></span>](ittime-get-starttime.md)
</dt> </dl>

 

 




