---
description: Die get \_ stopTime-Methode ruft den Endzeit Wert des NTP (Network Time Protocol)-Werts ab. Wenn die Endzeit 0 (null) ist, wird die Sitzung nicht gebunden.
ms.assetid: f18042c0-e41d-43b3-a75d-6ab161afde6e
title: 'Ittime:: get_StopTime-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b55ac03c4701884b5a4b7716cb2758887b6160bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356415"
---
# <a name="ittimeget_stoptime-method"></a><span data-ttu-id="71630-104">Ittime:: get \_ stopTime-Methode</span><span class="sxs-lookup"><span data-stu-id="71630-104">ITTime::get\_StopTime method</span></span>

<span data-ttu-id="71630-105">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="71630-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="71630-106">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="71630-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="71630-107">Die **get \_ stopTime** -Methode ruft den Endzeit Wert des NTP (Network Time Protocol)-Werts ab.</span><span class="sxs-lookup"><span data-stu-id="71630-107">The **get\_StopTime** method gets the NTP (Network Time Protocol) ending time value.</span></span> <span data-ttu-id="71630-108">Wenn die Endzeit 0 (null) ist, wird die Sitzung nicht gebunden.</span><span class="sxs-lookup"><span data-stu-id="71630-108">If the end time is zero, the session is not bounded.</span></span>

## <a name="syntax"></a><span data-ttu-id="71630-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="71630-109">Syntax</span></span>


```C++
HRESULT get_StopTime(
  [out] DOUBLE *pTime
);
```



## <a name="parameters"></a><span data-ttu-id="71630-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="71630-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71630-111">*PTIME* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="71630-111">*pTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="71630-112">Zeiger auf die Endzeit der Sitzung.</span><span class="sxs-lookup"><span data-stu-id="71630-112">Pointer to the stop time for the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71630-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="71630-113">Return value</span></span>

<span data-ttu-id="71630-114">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="71630-114">This method can return one of these values.</span></span>



| <span data-ttu-id="71630-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="71630-115">Return code</span></span>                                                                                   | <span data-ttu-id="71630-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="71630-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="71630-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="71630-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="71630-118">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="71630-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="71630-119"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="71630-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="71630-120">Der *PTIME* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="71630-120">The *pTime* parameter is not a valid pointer.</span></span><br/>        |
| <dl> <span data-ttu-id="71630-121"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="71630-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="71630-122">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="71630-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="71630-123"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="71630-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="71630-124">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="71630-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="71630-125"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="71630-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="71630-126">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="71630-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="71630-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="71630-127">Requirements</span></span>



| <span data-ttu-id="71630-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="71630-128">Requirement</span></span> | <span data-ttu-id="71630-129">Wert</span><span class="sxs-lookup"><span data-stu-id="71630-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="71630-130">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="71630-130">TAPI version</span></span><br/> | <span data-ttu-id="71630-131">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="71630-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="71630-132">Header</span><span class="sxs-lookup"><span data-stu-id="71630-132">Header</span></span><br/>       | <dl> <span data-ttu-id="71630-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="71630-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="71630-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="71630-134">Library</span></span><br/>      | <dl> <span data-ttu-id="71630-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="71630-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="71630-136">DLL</span><span class="sxs-lookup"><span data-stu-id="71630-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="71630-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71630-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71630-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="71630-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71630-139">**Ittime**</span><span class="sxs-lookup"><span data-stu-id="71630-139">**ITTime**</span></span>](ittime.md)
</dt> <dt>

[<span data-ttu-id="71630-140">**Ittime::p UT- \_ Stopp Zeit**</span><span class="sxs-lookup"><span data-stu-id="71630-140">**ITTime::put\_StopTime**</span></span>](ittime-put-stoptime.md)
</dt> </dl>

 

 




