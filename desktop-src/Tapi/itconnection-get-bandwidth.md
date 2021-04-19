---
description: Die get \_ Bandwidth-Methode ruft den Bandbreitenwert ab.
ms.assetid: d9020443-d061-4a60-9d54-191144def110
title: 'Itconnection:: get_Bandwidth-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 563ff4d5902a3434839167ffd28fad2b7552e5c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364548"
---
# <a name="itconnectionget_bandwidth-method"></a><span data-ttu-id="ea8d8-103">Itconnection:: get- \_ Bandbreiten Methode</span><span class="sxs-lookup"><span data-stu-id="ea8d8-103">ITConnection::get\_Bandwidth method</span></span>

<span data-ttu-id="ea8d8-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ea8d8-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ea8d8-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="ea8d8-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="ea8d8-106">Die **get \_ Bandwidth** -Methode ruft den Bandbreitenwert ab.</span><span class="sxs-lookup"><span data-stu-id="ea8d8-106">The **get\_Bandwidth** method gets the bandwidth value.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea8d8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea8d8-107">Syntax</span></span>


```C++
HRESULT get_Bandwidth(
  [out] DOUBLE *pBandwidth
);
```



## <a name="parameters"></a><span data-ttu-id="ea8d8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea8d8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea8d8-109">*pbandwidth* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ea8d8-109">*pBandwidth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ea8d8-110">Bandbreitenwert.</span><span class="sxs-lookup"><span data-stu-id="ea8d8-110">Bandwidth value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea8d8-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ea8d8-111">Return value</span></span>

<span data-ttu-id="ea8d8-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="ea8d8-112">This method can return one of these values.</span></span>



| <span data-ttu-id="ea8d8-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="ea8d8-113">Return code</span></span>                                                                                   | <span data-ttu-id="ea8d8-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ea8d8-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="ea8d8-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ea8d8-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ea8d8-116">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="ea8d8-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="ea8d8-117"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="ea8d8-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="ea8d8-118">Der *pbandwidth* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="ea8d8-118">The *pBandwidth* parameter is not a valid pointer.</span></span><br/>   |
| <dl> <span data-ttu-id="ea8d8-119"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="ea8d8-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ea8d8-120">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ea8d8-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="ea8d8-121"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="ea8d8-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="ea8d8-122">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="ea8d8-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="ea8d8-123"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="ea8d8-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="ea8d8-124">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="ea8d8-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="ea8d8-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ea8d8-125">Requirements</span></span>



| <span data-ttu-id="ea8d8-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ea8d8-126">Requirement</span></span> | <span data-ttu-id="ea8d8-127">Wert</span><span class="sxs-lookup"><span data-stu-id="ea8d8-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ea8d8-128">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="ea8d8-128">TAPI version</span></span><br/> | <span data-ttu-id="ea8d8-129">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="ea8d8-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="ea8d8-130">Header</span><span class="sxs-lookup"><span data-stu-id="ea8d8-130">Header</span></span><br/>       | <dl> <span data-ttu-id="ea8d8-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea8d8-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="ea8d8-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ea8d8-132">Library</span></span><br/>      | <dl> <span data-ttu-id="ea8d8-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ea8d8-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="ea8d8-134">DLL</span><span class="sxs-lookup"><span data-stu-id="ea8d8-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="ea8d8-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea8d8-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea8d8-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ea8d8-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea8d8-137">**Itconnection**</span><span class="sxs-lookup"><span data-stu-id="ea8d8-137">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

 




