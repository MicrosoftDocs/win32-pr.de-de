---
description: Die get \_ TTL-Methode ruft den Gültigkeitsbereich (Time to Live, TTL) für Übertragungen für die Adressen ab.
ms.assetid: ea3c22d8-476e-4b4b-98c6-f1075e704f3d
title: 'Itconnection:: get_Ttl-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88f4810eeefc19647e6ed5601b3a6b88870f1e9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366001"
---
# <a name="itconnectionget_ttl-method"></a><span data-ttu-id="9cc19-103">Itconnection:: get \_ TTL-Methode</span><span class="sxs-lookup"><span data-stu-id="9cc19-103">ITConnection::get\_Ttl method</span></span>

<span data-ttu-id="9cc19-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9cc19-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9cc19-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="9cc19-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="9cc19-106">Die **get \_ TTL** -Methode ruft den Gültigkeitsbereich ( [*Time to Live,*](t-tapgloss.md) TTL) für Übertragungen für die Adressen ab.</span><span class="sxs-lookup"><span data-stu-id="9cc19-106">The **get\_Ttl** method gets the [*time to live*](t-tapgloss.md) (TTL) scope for transmissions on the addresses.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cc19-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9cc19-107">Syntax</span></span>


```C++
HRESULT get_Ttl(
  [out] unsigned char *pTtl
);
```



## <a name="parameters"></a><span data-ttu-id="9cc19-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9cc19-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cc19-109">*PTTL* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9cc19-109">*pTtl* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9cc19-110">Gültigkeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="9cc19-110">TTL scope.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cc19-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9cc19-111">Return value</span></span>

<span data-ttu-id="9cc19-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="9cc19-112">This method can return one of these values.</span></span>



| <span data-ttu-id="9cc19-113">Wert</span><span class="sxs-lookup"><span data-stu-id="9cc19-113">Value</span></span>                                                                                         | <span data-ttu-id="9cc19-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9cc19-114">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="9cc19-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9cc19-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="9cc19-116">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="9cc19-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="9cc19-117"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="9cc19-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="9cc19-118">Der *PTTL* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="9cc19-118">The *pTtl* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="9cc19-119"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="9cc19-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="9cc19-120">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="9cc19-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="9cc19-121"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="9cc19-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="9cc19-122">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="9cc19-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="9cc19-123"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="9cc19-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="9cc19-124">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="9cc19-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="9cc19-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9cc19-125">Requirements</span></span>



| <span data-ttu-id="9cc19-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9cc19-126">Requirement</span></span> | <span data-ttu-id="9cc19-127">Wert</span><span class="sxs-lookup"><span data-stu-id="9cc19-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9cc19-128">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="9cc19-128">TAPI version</span></span><br/> | <span data-ttu-id="9cc19-129">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="9cc19-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="9cc19-130">Header</span><span class="sxs-lookup"><span data-stu-id="9cc19-130">Header</span></span><br/>       | <dl> <span data-ttu-id="9cc19-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="9cc19-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="9cc19-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9cc19-132">Library</span></span><br/>      | <dl> <span data-ttu-id="9cc19-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9cc19-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="9cc19-134">DLL</span><span class="sxs-lookup"><span data-stu-id="9cc19-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="9cc19-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9cc19-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9cc19-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9cc19-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cc19-137">**Itconnection**</span><span class="sxs-lookup"><span data-stu-id="9cc19-137">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

 




