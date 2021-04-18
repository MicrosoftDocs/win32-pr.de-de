---
description: Die get \_ StartTime-Methode ruft den 32-Bit-NTP (Network Time Protocol)-Start Zeitwert ab. Die Sitzung gilt ab diesem Zeitpunkt als aktiv.
ms.assetid: 511e4486-4c73-4610-8e64-9c70acc98eab
title: 'Ittime:: get_StartTime-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 051096c6cbdab1960c67ddb2cbcaf57eccab9556
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351268"
---
# <a name="ittimeget_starttime-method"></a><span data-ttu-id="86e79-104">Ittime:: get \_ StartTime-Methode</span><span class="sxs-lookup"><span data-stu-id="86e79-104">ITTime::get\_StartTime method</span></span>

<span data-ttu-id="86e79-105">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="86e79-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="86e79-106">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="86e79-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="86e79-107">Die **get \_ StartTime** -Methode ruft den 32-Bit-NTP (Network Time Protocol)-Start Zeitwert ab.</span><span class="sxs-lookup"><span data-stu-id="86e79-107">The **get\_StartTime** method gets the 32-bit NTP (Network Time Protocol) starting time value.</span></span> <span data-ttu-id="86e79-108">Die Sitzung gilt ab diesem Zeitpunkt als aktiv.</span><span class="sxs-lookup"><span data-stu-id="86e79-108">The session is considered active from this time.</span></span>

## <a name="syntax"></a><span data-ttu-id="86e79-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="86e79-109">Syntax</span></span>


```C++
HRESULT get_StartTime(
  [out] DOUBLE *pTime
);
```



## <a name="parameters"></a><span data-ttu-id="86e79-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="86e79-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86e79-111">*PTIME* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="86e79-111">*pTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86e79-112">Zeiger auf die Startzeit der Sitzung.</span><span class="sxs-lookup"><span data-stu-id="86e79-112">Pointer to the start time for the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86e79-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="86e79-113">Return value</span></span>

<span data-ttu-id="86e79-114">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="86e79-114">This method can return one of these values.</span></span>



| <span data-ttu-id="86e79-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="86e79-115">Return code</span></span>                                                                                   | <span data-ttu-id="86e79-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="86e79-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="86e79-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="86e79-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="86e79-118">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="86e79-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="86e79-119"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="86e79-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="86e79-120">Der *PTIME* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="86e79-120">The *pTime* parameter is not a valid pointer.</span></span><br/>        |
| <dl> <span data-ttu-id="86e79-121"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="86e79-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="86e79-122">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="86e79-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="86e79-123"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="86e79-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="86e79-124">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="86e79-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="86e79-125"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="86e79-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="86e79-126">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="86e79-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="86e79-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="86e79-127">Requirements</span></span>



| <span data-ttu-id="86e79-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="86e79-128">Requirement</span></span> | <span data-ttu-id="86e79-129">Wert</span><span class="sxs-lookup"><span data-stu-id="86e79-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="86e79-130">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="86e79-130">TAPI version</span></span><br/> | <span data-ttu-id="86e79-131">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="86e79-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="86e79-132">Header</span><span class="sxs-lookup"><span data-stu-id="86e79-132">Header</span></span><br/>       | <dl> <span data-ttu-id="86e79-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="86e79-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="86e79-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="86e79-134">Library</span></span><br/>      | <dl> <span data-ttu-id="86e79-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="86e79-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="86e79-136">DLL</span><span class="sxs-lookup"><span data-stu-id="86e79-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="86e79-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86e79-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86e79-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="86e79-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86e79-139">**Ittime**</span><span class="sxs-lookup"><span data-stu-id="86e79-139">**ITTime**</span></span>](ittime.md)
</dt> <dt>

[<span data-ttu-id="86e79-140">**Ittime::p UT- \_ StartTime**</span><span class="sxs-lookup"><span data-stu-id="86e79-140">**ITTime::put\_StartTime**</span></span>](ittime-put-starttime.md)
</dt> </dl>

 

 




